---

 

copyright:

  years: 2016

 

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock:.codeblock}
{:screen:.screen}
{:pre: .pre}

# {{site.data.keyword.openwhisk_short}} system details
{: #openwhisk_reference}
*Last updated: 14 April 2016*

The following sections provide more details about the {{site.data.keyword.openwhisk}} system.
{: shortdesc}

## {{site.data.keyword.openwhisk_short}} entities
{: #openwhisk_entities}

### Namespaces and packages

{{site.data.keyword.openwhisk_short}} actions, triggers, and rules belong in a namespace, and optionally a package.

Packages can contain actions and feeds. A package cannot contain another package, so package nesting is not allowed. Also, entities do not have to be contained in a package.

In Bluemix, an organization+space pair corresponds to a {{site.data.keyword.openwhisk_short}} namespace. For example, the organization `BobsOrg` and space `dev` would correspond to the {{site.data.keyword.openwhisk_short}} namespace `/BobsOrg_dev`.

You can create your own namespaces if you're entitled to do so. The `/whisk.system` namespace is reserved for entities that are distributed with the {{site.data.keyword.openwhisk_short}} system.


### Fully qualified names

The fully qualified name of an entity is
`/namespaceName[/packageName]/entityName`. Notice that `/` is used to delimit
namespaces, packages, and entities. Also namespaces must be prefixed with a `/`.

For convenience the namespace can be left off if it is the user's *default
namespace*.

For example, consider a user whose default namespace is `/myOrg`. Here are
examples of the fully qualified names of a number of entities and their aliases.

| Fully qualified name | Alias | Namespace | Package | Name |
| --- | --- | --- | --- | --- |
| `/whisk.system/cloudant/read` | - | `/whisk.system` | `cloudant` | `read` |
| `/myOrg/video/transcode` | `video/transcode` | `/myOrg` | `video` | `transcode` |
| `/myOrg/filter` | `filter` | `/myOrg` | - | `filter` |

You will be using this naming scheme when you use the {{site.data.keyword.openwhisk_short}} CLI, among other places.

### Entity names

The names of all entities including actions, triggers, rules, packages, and namespaces are a sequence of characters that follow the following format:

* The first character must be an alphanumeric character, a digit, or an underscore.
* The subsequent characters can be alphanumeric, digits, spaces, or any of the following: `_`, `@`, `.`, `-`.
* The last character can't be a space.

More precisely, a name must match the following regular expression (expressed using Java metacharacter syntax): `\A([\w]|[\w][\w@ .-]*[\w@.-]+)\z`.


## Action semantics
{: #openwhisk_semantics}

The following sections describe details about {{site.data.keyword.openwhisk_short}} actions.

### Statelessness

Action implementations should be stateless, or *idempotent*. While the system does not enforce this property, there is no guarantee that any state maintained by an action will be available across invocations.

Moreover, multiple instantiations of an action might exist, with each instantiation having its own state. An action invocation might be dispatched to any of these instantiations.

### Invocation input and output

The input to and output from an action is a dictionary of key-value pairs. The key is a string, and the value a valid JSON value.

### Invocation ordering of actions
{: #openwhisk_ordering}

Invocations of an action are not ordered. If the user invokes an action twice from the command-line or the REST API, the second invocation might run before the first. If the actions have side effects, they might be observed in any order.

Additionally, there is no guarantee of actions executing atomically. Two actions can run concurrently and their side effects can be interleaved. Any concurrency side effects will be implementation dependent.

### At most once semantics
{: #openwhisk_atmostonce}

The system supports at most one invocation of actions.

When an invocation request is received, the system records the request, and
dispatches an activation.

The system returns an activation ID (in the case of a nonblocking invoke) to
confirm that the invocation has been received. Note that even in the absence of
this response (perhaps due to a broken network connection), it is possible
that the invocation was received.

The system attempts to invoke the action once, resulting in one of the following four outcomes:
- *success*: the action invocation completed successfully.
- *application error*: the action invocation was successful, but the action returned an error value on purpose, for instance because a precondition on the arguments was not met.
- *action developer error*: the action was invoked, but it completed abnormally, for instance the action did not catch an exception, or a syntax error existed.
- *whisk internal error*: the system was unable to invoke the action.
The outcome is recorded in the `status` field of the activation record, as document in a following section.

Every invocation that is successfully received, and that the
user might be billed for, will eventually have an activation record.


## Activation record
{: #openwhisk_ref_activation}

Each action invocation and trigger firing results in an activation record.

An activation record contains the following fields:

- *activationId*: The activation ID.
- *start* and *end*: Timestamps recording the start and end of the activation. The values are in [UNIX time format](http://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap04.html#tag_04_15).
- *namespace* and `name`: The namespace and name of the entity.
- *logs*: An array of strings with the logs produced by the action during its activation. Each array element corresponds to a line output to stdout or stderr by the action, and includes the time and stream of the log output. The structure is as follows: ```TIMESTAMP STREAM: LOG_OUTPUT```.
- *response*: A dictionary defining the keys `success`, `status`, and `result`:
  - *status*: The activation result, which might be one of the following values: "success", "application error", "action developer error", "whisk internal error".
  - *success*: Is `true` if and only if the status is `"success"`
- *result*: A dictionary that contains the activation result. If the activation was successful, this contains the value returned by the action. If the activation was unsuccessful, `result` is guaranteed to contain the `error` key, generally with an explanation of the failure.


## JavaScript actions
{: #openwhisk_ref_javascript}

### Function prototype

{{site.data.keyword.openwhisk_short}} JavaScript actions run in a Node.js runtime, currently version 0.12.9.

Actions written in JavaScript must be confined to a single file. The file can contain multiple functions but by convention a function called `main` must exist and is the one called when the action is invoked. For example, the following is an example of an action with multiple functions.

```
function main() {
    return { payload: helper() }
}

function helper() {
    return new Date();
}
```
{: codeblock}

The action input parameters are passed as a JSON object as a parameter to the `main` function. The result of a successful activation is also a JSON object but is returned differently depending on whether the action is synchronous or asynchronous as described in the following section.


### Synchronous and asynchronous behavior

It is common for JavaScript functions to continue execution in a callback function even after returning. To accomodate this, an activation of a JavaScript action can be *synchronous* or *asynchronous*.

A JavaScript action's activation is **synchronous** if the main function exits under one of the following conditions:

- The main function exits without executing a ```return``` statement.
- The main function exits by executing a ```return``` statement that returns any value *except* ```whisk.async()```.

Here are two examples of synchronous actions.

```
// a synchronous action
function main() {
  return {payload: 'Hello, World!'};
}
```
{: codeblock}

```
// an action in which each path results in a synchronous activation
function main(params) {
  if (params.payload == 0) {
     return;
  } else if (params.payload == 1) {
     return whisk.done();    // indicates normal completion
  } else if (params.payload == 2) {
    return whisk.error();   // indicates abnormal completion
  }
}
```
{: codeblock}

A JavaScript action's activation is **asynchronous** if the main function exits by calling ```return whisk.async();```.  In this case the system assumes that the action is still running, until the action executes one of the following:
- ```return whisk.done();```
- ```return whisk.error();```

Here is an example of an action that executes asynchronously.

```
function main() {
    setTimeout(function() {
        return whisk.done({done: true});
    }, 100);
    return whisk.async();
}
```
{: codeblock}

It is possible for an action is synchronous on some inputs and asynchronous on others. Here is an example.

```
  function main(params) {
      if (params.payload) {
         setTimeout(function() {
            return whisk.done({done: true});
         }, 100);
         return whisk.async();  // asynchronous activation
      }  else {
         return whisk.done();   // synchronous activation
      }
  }
```
{: codeblock}

- In this case, the `main` function should return `whisk.async()`. When the activation result is available, the `whisk.done()` function should be called with the result passed as a JSON object. This is referred to as an *asynchronous* activation.

Note that regardless of whether an activation is synchronous or asynchronous, the invocation of the action can be blocking or non-blocking.

### Additional SDK methods

The `whisk.invoke()` function invokes another action. It takes as an argument a dictionary defining the following parameters:

- *name*: The fully qualified name of the action to invoke,
- *parameters*: A JSON object representing the input to the invoked action. If omitted, defaults to an empty object.
- *apiKey*: The authorization key with which to invoke the action. Defaults to `whisk.getAuthKey()`. 
- *blocking*: Whether the action should be invoked in blocking or non-blocking mode. Defaults to `false`, indicating a non-blocking invocation.
- *next*: An optional callback function to be executed when the invocation completes.

The signature for `next` is `function(error, activation)`, where:

- `error` is `false` if the invocation succeeded, and a truthy value if it failed, usually a string describing the error.
- On errors, `activation` might be undefined, depending on the failure mode.
- When defined, `activation` is a dictionary with the following fields:
  - *activationId*: The activation ID:
  - *result*: If the action was invoked in blocking mode: The action result as a JSON object, else `undefined`.

The `whisk.trigger()` function fires a trigger. It takes as an argument a JSON object with the following parameters:

- *name*: The fully qualified name of trigger to invoke.
- *parameters*: A JSON object representing the input to the trigger. If omitted, defaults to an empty object.
- *apiKey*: The authorization key with which to fire the trigger. Defaults to `whisk.getAuthKey()`.
- *next*: An optional callback to be executed when the firing completes.

The signature for `next` is `function(error, activation)`, where:

- `error` is `false` if the firing succeeded, and a truthy value if it failed, usually a string describing the error.
- On errors, `activation` might be undefined, depending on the failure mode.
- When defined, `activation` is a dictionary with an `activationId` field containing the activation ID.

The `whisk.getAuthKey()` function returns the authorization key under which the action is running. Usually, you do not need to invoke this function directly, because it is used implicitly by the `whisk.invoke()` and `whisk.trigger()` functions.

### Runtime environment
{: #openwhisk_ref_runtime_environment}

JavaScript actions are executed in a Node.js version 0.12.9 environment with the following packages available to be used by the action:

- apn
- async
- body-parser
- btoa
- cloudant
- commander
- consul
- cookie-parser
- cradle
- errorhandler
- express
- express-session
- jade
- log4js
- merge
- moment
- mustache
- nano
- node-uuid
- oauth2-server
- process
- request
- rimraf
- semver
- serve-favicon
- socket.io
- superagent
- swagger-tools
- tmp
- watson-developer-cloud
- when
- xml2js
- xmlhttprequest
- yauzl


## Docker actions
{: #openwhisk_ref_docker}

Docker actions run a user-supplied binary in a Docker container. The binary runs in a Docker image based on Ubuntu 14.04 LTD, so the binary must be compatible with this distribution.

The action input "payload" parameter is passed as a positional argument to the binary program, and the standard output from the execution of the program is returned in the "result" parameter.

The Docker skeleton is a convenient way to build {{site.data.keyword.openwhisk_short}}-compatible Docker images. You can install the skeleton with the `wsk sdk install docker` CLI command.

The main binary program should be copied to the `dockerSkeleton/client/clientApp` file. Any companion files or library can reside in the `dockerSkeleton/client` directory.

You can also include any compilation steps or dependencies by modifying the `dockerSkeleton/Dockerfile`. For example you can install Python if your action is a Python script.


## System limits
{: #openwhisk_syslimits}

{{site.data.keyword.openwhisk_short}} has a few system limits, including how much memory an action uses and how many action invocations are allowed per hour. The following table lists the default limits.

| limit | description | configurable | unit | default |
| ----- | ----------- | ------------ | -----| ------- |
| timeout | a container is not allowed to run longer than N milliseconds | per action |  milliseconds | 60000 |
| memory | a container is not allowed to allocate more than N MB of memory | per action | MB | 256 |
| concurrent | it's not allowed to have more than N concurrent activations per namespace | per namespace | number | 100 |
| minuteRate | a user cannot invoke more than this many actions per minute | per user | number | 120 |
| hourRate | a user cannot invoke more than this many actions per hour | per user | number | 3600 |

### Per action timeout (ms) (Default: 60s)
* The timeout limit N is in the range [100ms..300000ms] and is set per action in milliseconds.
* A user can change the limit when creating the action.
* A container that runs longer than N milliseconds is terminated.

### Per action memory (MB) (Default: 256MB)
* The memory limit M is in the range from [128MB..512MB] and is set per action in MB.
* A user can change the limit when creating the action.
* A container cannot have more memory allocated than the limit.

### Per namespace #Concurrent Invocation (#) (Default: 100)
* The number of activations that are currently processed for a namespace cannot exceed 100.
* The default limit can be statically configured by whisk in consul kvstore.
* A user is currently not able to change the limits.


### Invocations per minute/hour (#) (Fixed: 120/3600)
* The rate limit N is set to 120/3600 and limits the number of action invocations in one minute/hour windows.
* A user cannot change this limit when creating the action.
* A CLI call that exceeds this limit receives an error code corresponding to TOO_MANY_REQUESTS.
