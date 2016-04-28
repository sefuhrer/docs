---

 

copyright:

  years: 2016

 

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# Using {{site.data.keyword.openwhisk_short}}-enabled services 
{: #openwhisk_ecosystem}
*Last updated: 28 March 2016*

In {{site.data.keyword.openwhisk}}, a catalog of packages gives you an easy way to enhance your app with useful capabilities, and to access external services in the ecosystem. Examples of external services that are {{site.data.keyword.openwhisk_short}}-enabled include Cloudant, The Weather Company, Slack, and GitHub.
{: shortdesc}

The catalog is available as packages in the `/whisk.system` namespace. See [Browsing packages](./openwhisk_packages.html#openwhisk_packagedisplay) for information about how to browse the catalog by using the command line tool.

The topics that follow document some of the packages in the catalog.

## Using the Cloudant package
{: #openwhisk_catalog_cloudant}
The `/whisk.system/cloudant` package enables you to work with a Cloudant database. It includes the following actions and feeds.

| Entity | Type | Parameters | Description |
| --- | --- | --- | --- |
| `/whisk.system/cloudant` | package | {{site.data.keyword.Bluemix_notm}}ServiceName, host, username, password, dbname, includeDoc, overwrite | Work with a Cloudant database |
| `/whisk.system/cloudant/read` | action | dbname, includeDoc, id | Read a document from a database |
| `/whisk.system/cloudant/write` | action | dbname, overwrite, doc | Write a document to a database |
| `/whisk.system/cloudant/changes` | feed | dbname, includeDoc | Fire trigger events on changes to a database |

The following topics walk through setting up a Cloudant database, configuring an associated package, and using the actions and feeds in the `/whisk.system/cloudant` package.

### Setting up a Cloudant database in {{site.data.keyword.Bluemix_notm}}

If you're using {{site.data.keyword.openwhisk_short}} from {{site.data.keyword.Bluemix}}, {{site.data.keyword.openwhisk_short}} automatically creates package bindings for your {{site.data.keyword.Bluemix_notm}} Cloudant service instances. If you're not using {{site.data.keyword.openwhisk_short}} and Cloudant from {{site.data.keyword.Bluemix_notm}}, skip to the next step.

1. Create a Cloudant service instance in your {{site.data.keyword.Bluemix_notm}} [dashboard](http://console.ng.{{site.data.keyword.Bluemix_notm}}.net).

  Be sure to remember the name of the service instance and the {{site.data.keyword.Bluemix_notm}} organization and space you're in.

2. Make sure your {{site.data.keyword.openwhisk_short}} CLI is in the namespace corresponding to the {{site.data.keyword.Bluemix_notm}} organization and space that you used in the previous step.

  ```
  wsk property set --namespace my{{site.data.keyword.Bluemix_notm}}Org_my{{site.data.keyword.Bluemix_notm}}Space
  ```
  {: pre}

  Alternatively, you can use `wsk property set --namespace` to set a namespace from a list of those accessible to you.

3. Refresh the packages in your namespace. The refresh automatically creates a package binding for the Cloudant service instance that you created.

  ```
  wsk package refresh
  ```
  {: pre}
  ```
  created bindings:
  {{site.data.keyword.Bluemix_notm}}_testCloudant_Credentials-1
  ```
  {: screen}

  ```
  wsk package list
  ```
  {: pre}
  ```
  packages
  /my{{site.data.keyword.Bluemix_notm}}Org_my{{site.data.keyword.Bluemix_notm}}Space/{{site.data.keyword.Bluemix_notm}}_testCloudant_Credentials-1 private binding
  ```
  {: screen}

  You should see the fully qualified name of the package binding that corresponds to your {{site.data.keyword.Bluemix_notm}} Cloudant service instance.

4. Check to see that the package binding created previously is configured with your Cloudant {{site.data.keyword.Bluemix_notm}} service instance host and credentials.

  ```
  wsk package get /my{{site.data.keyword.Bluemix_notm}}Org_my{{site.data.keyword.Bluemix_notm}}Space/{{site.data.keyword.Bluemix_notm}}_testCloudant_Credentials-1
  ```
  {: pre}
  ```
  ok: got package /my{{site.data.keyword.Bluemix_notm}}Org_my{{site.data.keyword.Bluemix_notm}}Space/{{site.data.keyword.Bluemix_notm}}_testCloudant_Credentials-1, projecting parameters
  [
      ...
      {
          "key": "username",
          "value": "cdb18832-2bbb-4df2-b7b1-{{site.data.keyword.Bluemix_notm}}"
      },
      {
          "key": "host",
          "value": "cdb18832-2bbb-4df2-b7b1-{{site.data.keyword.Bluemix_notm}}.cloudant.com"
      },
      {
          "key": "password",
          "value": "c9088667484a9ac827daf8884972737"
      }
      ...
  ]
  ```
  {: screen}

### Setting up a Cloudant database outside {{site.data.keyword.Bluemix_notm}}

If you're not using {{site.data.keyword.openwhisk_short}} in {{site.data.keyword.Bluemix_notm}} or if you want to set up your Cloudant database outside of {{site.data.keyword.Bluemix_notm}}, you must manually create a package binding for your Cloudant account. You need the Cloudant account hostname, user name, and password.

1. Create a package binding configured for your Cloudant account.

  ```
  wsk package bind /whisk.system/cloudant myCloudant -p username 'MYUSERNAME' -p password 'MYPASSWORD' -p host 'MYCLOUDANTACCOUNT.cloudant.com'
  ```
  {: pre}

2. Verify that the package binding exists.

  ```
  wsk package list
  ```
  {: pre}
  ```
  packages
  /myNamespace/myCloudant private binding
  ```
  {: screen}


### Listening for changes to a Cloudant database

You can use the `changes` feed to configure a service to fire a trigger on every change to your Cloudant database.

1. Create a trigger with the `changes` feed in the package binding that you created previously. Be sure to replace `/myNamespace/myCloudant` with your package name.

  ```
  wsk trigger create myCloudantTrigger --feed /myNamespace/myCloudant/changes --param dbname testdb --param includeDocs true
  ```
  {: pre}
  ```
  ok: created trigger feed myCloudantTrigger
  ```
  {: screen}

2. Poll for activations.

  ```
  wsk activation poll
  ```
  {: pre}

3. In your Cloudant dashboard, either modify an existing document or create a new one.

4. Observe new activations for the `myCloudantTrigger` trigger for each document change.

**Note**: If you are unable to observe new activations, see the subsequent sections on reading from and writing to a Cloudant database. Testing the reading and writing steps below will help verify that your Cloudant credentials are correct.

You can now create rules and associate them to actions to react to the document updates.

The content of the generated events depends on the value of the value of the `includeDocs` parameter when creating the trigger. If set to true, each trigger event that is fired includes the modified Cloudant document. For example, consider the following modified document:

  ```
  {
    "_id": "6ca436c44074c4c2aa6a40c9a188b348",
    "_rev": "3-bc4960fc13aa368afca8c8427a1c18a8",
    "name": "Heisenberg"
  }
  ```
  {: screen}

The code in this example generates a trigger event with the corresponding `_id`, `_rev` and `name` parameters. In fact, the JSON representation of the trigger event is identical to the document.

Otherwise, if `includeDocs` is false, the events include the following parameters:

- `id`: The document ID.
- `seq`: The sequence identifier generated by Cloudant.
- `changes`: An array of objects, each of which has a `rev` field that contains the revision ID of the document.

The JSON representation of the trigger event is as follows:

  ```
  {
      "id": "6ca436c44074c4c2aa6a40c9a188b348",
      "seq": "2-g1AAAAL9aJyV-GJCaEuqx4-BktQkYp_dmIfC",
      "changes": [
          {
              "rev": "2-da3f80848a480379486fb4a2ad98fa16"
          }
      ]
  }
  ```


### Writing to a Cloudant database

You can use an action to store a document in a Cloudant database called `testdb`. Make sure that this database exists in your Cloudant account.

1. Store a document by using the `write` action in the package binding you created previously. Be sure to replace `/myNamespace/myCloudant` with your package name.

  ```
  wsk action invoke /myNamespace/myCoudant/write --blocking --result --param dbname testdb --param doc '{"_id":"heisenberg", "name":"Walter White"}'
  ```
  {: pre}
  ```
  ok: invoked /myNamespace/myCoudant/write with id 62bf696b38464fd1bcaff216a68b8287
  response:
  {
    "id": "heisenberg",
    "ok": true,
    "rev": "1-9a94fb93abc88d8863781a248f63c8c3"
  }
  ```
  {: screen}

2. Verify that the document exists by browsing for it in your Cloudant dashboard.

  The dashboard URL for the `testdb` database looks something like the following: `https://MYCLOUDANTACCOUNT.cloudant.com/dashboard.html#database/testdb/_all_docs?limit=100`.


### Reading from a Cloudant database

You can use an action to fetch a document from a Cloudant database called `testdb`. Make sure that this database exists in your Cloudant account.

1. Fetch a document by using the `read` action in the package binding that you created previously. Be sure to replace `/myNamespace/myCloudant` with your package name.

  ```
  wsk action invoke /myNamespace/myCoudant/read --blocking --result --param dbname testdb --param id heisenberg
  ```
  {: pre}
  ```
  {
    "_id": "heisenberg",
    "_rev": "1-9a94fb93abc88d8863781a248f63c8c3"
    "name": "Walter White"
  }
  ```
  {: screen}


## Using the Alarm package
{: #openwhisk_catalog_alarm}

The `/whisk.system/alarms` package can be used to fire a triggers at a specified frequency. This is useful to setup recurring jobs or tasks, such as invoking a system backup action every hour.

The package includes the following feed.

| Entity | Type | Parameters | Description |
| --- | --- | --- | --- |
| `/whisk.system/alarms` | package | - | Alarms and periodic utility |
| `/whisk.system/alarms/alarm` | feed | cron, trigger_payload, maxTriggers | Fire trigger event periodically |


### Firing a trigger event periodically

The `/whisk.system/alarms/alarm` feed configures the Alarm service to fire a trigger event at a specified frequency. The parameters are as follows:

- `cron`: A string, based on the Unix crontab syntax, that indicates when to fire the trigger in Coordinated Universal Time (UTC). The string is a sequence of six fields separated by spaces: `X X X X X X `. For more details on using cron syntax, see: https://github.com/ncb000gt/node-cron.

- `trigger_payload`: The value of this parameter becomes the content of the trigger every time the trigger is fired.

- `maxTriggers`: Stop firing triggers when this limit is reached. Defaults to 1000.

Here is an example of creating a trigger that will be fired once every 20 seconds with `name` and `place` values in the trigger event.

  ```
  wsk trigger create periodic --feed /whisk.system/alarms/alarm --param cron '/20 * * * * *' --param trigger_payload '{"name":"Odin","place":"Asgard"}'
  ```
  {: pre}

Each generated event will include as parameters the properties specified in the `trigger_payload` value. In this case, each trigger event will have parameters `name=Odin` and `place=Asgard`.


## Using the Weather package
{: #openwhisk_catalog_weather}

The `/whisk.system/weather` package offers a convenient way to call The Weather Company API.

The package includes the following action.

| Entity | Type | Parameters | Description |
| --- | --- | --- | --- |
| `/whisk.system/weather` | package | apiKey | Services from The Weather Company |
| `/whisk.system/weather/forecast` | action | apiKey, latitude, longitude | Weather.com 10-day forecast |

While not required, it's suggested that you create a package binding with the `apiKey` value. This way you don't need to specify the key every time you invoke the actions in the package.

### Getting a weather forecast for a location

The `/whisk.system/weather/forecast` action returns a 10-day weather forecast for a location by calling an API from The Weather Company. The parameters are as follows:

- `apiKey`: An API key for The Weather Company that is entitled to invoke the 10-day forecast API.
- `latitude`: The latitude coordinate of the location.
- `longitude`: The longitude coordinate of the location.

Here is an example of creating a package binding and then getting a 10-day forecast.

1. Create a package binding with your API key.

  ```
  wsk package bind /whisk.system/weather myWeather --param apiKey 'MY_WEATHER_API'
  ```
  {: pre}

2. Invoke the `forecast` action in your package binding to get the weather forecast.

  ```
  wsk action invoke myWeather/forecast --blocking --result --param latitude '43.7' --param longitude '-79.4'
  ```
  {: pre}

  ```
  {
      "forecasts": [
          {
              "dow": "Wednesday",
              "max_temp": -1,
              "min_temp": -16,
              "narrative": "Chance of a few snow showers. Highs -2 to 0C and lows -17 to -15C.",
              ...
          },
          {
              "class": "fod_long_range_daily",
              "dow": "Thursday",
              "max_temp": -4,
              "min_temp": -8,
              "narrative": "Mostly sunny. Highs -5 to -3C and lows -9 to -7C.",
              ...
          },
          ...
      ],
  }
  ```
  {: screen}


## Using the Watson package
{: #openwhisk_catalog_watson}

The `/whisk.system/watson` package offers a convenient way to call various Watson APIs.

The package includes the following actions.

| Entity | Type | Parameters | Description |
| --- | --- | --- | --- |
| `/whisk.system/watson` | package | username, password | Actions for the Watson analytics APIs |
| `/whisk.system/watson/translate` | action | translateFrom, translateTo, translateParam, username, password | Translate text |
| `/whisk.system/watson/languageId` | action | payload, username, password | Identify language |

While not required, it's suggested that you create a package binding with the `username` and `password` values. This way you don't need to specify these credentials every time you invoke the actions in the package.

### Translating text

The `/whisk.system/watson/translate` action translate text from one language to another. The parameters are as follows:

- `username`: The Watson API username.
- `password`: The Watson API password.
- `translateParam`: The input parameter to translate. For example, if `translateParam=payload`, then the value of the `payload` parameter passed to the action is translated.
- `translateFrom`: A two digit code of the source language.
- `translateTo`: A two digit code of the target language.

The following is an example of creating a package binding and translating some text.

1. Create a package binding with your Watson credentials.

  ```
  wsk package bind /whisk.system/watson myWatson --param username 'MY_WATSON_USERNAME' --param password 'MY_WATSON_PASSWORD'
  ```
  {: pre}

2. Invoke the `translate` action in your package binding to translate some text from English to French.

  ```
  wsk action invoke myWatson/translate --blocking --result --param payload 'Blue skies ahead' --param translateParam 'payload' --param translateFrom 'en' --param translateTo 'fr'
  ```
  {: pre}

  ```
  {
      "payload": "Ciel bleu a venir"
  }
  ```
  {: screen}


### Identifying the language of some text

The `/whisk.system/watson/languageId` action identifies the language of some text. The parameters are as follows:

- `username`: The Watson API username.
- `password`: The Watson API password.
- `payload`: The text to identify.

Here is an example of creating a package binding and identifying the language of some text.

1. Create a package binding with your Watson credentials.

  ```
  wsk package bind /whisk.system/watson myWatson -p username 'MY_WATSON_USERNAME' -p password 'MY_WATSON_PASSWORD'
  ```
  {: pre}

2. Invoke the `languageId` action in your package binding to identify the language.

  ```
  wsk action invoke myWatson/languageId --blocking --result --param payload 'Ciel bleu a venir'
  ```
  {: pre}
  ```
  {
    "payload": "Ciel bleu a venir",
    "language": "fr",
    "confidence": 0.710906
  }
  ```
  {: screen}


## Using the Slack package
{: #openwhisk_catalog_slack}

The `/whisk.system/slack` package offers a convenient way to use the [Slack APIs](https://api.slack.com/).

The package includes the following actions:

| Entity | Type | Parameters | Description |
| --- | --- | --- | --- |
| `/whisk.system/slack` | package | url, channel, username | Interact with the Slack API |
| `/whisk.system/slack/post` | action | text, url, channel, username | Posts a message to a Slack channel |

While not required, it's suggested that you create a package binding with the `username`, `url`, and 'channel' values. With binding, you don't need to specify the values each time that you invoke the action in the package.

### Posting a message to a Slack channel

The `/whisk.system/slack/post` action posts a message to a specified Slack channel. The parameters are as follows:

- `url`: The Slack webhook URL.
- `channel`: The Slack channel to post the message to.
- `username`: The name to post the message as.
- `text`: A message to post.

The following is an example of configuring Slack, creating a package binding, and posting a message to a channel.

1. Configure a Slack [incoming webhook](https://api.slack.com/incoming-webhooks) for your team.

  After Slack is configured, you should get a Webhook URL that looks like `https://hooks.slack.com/services/aaaaaaaaa/bbbbbbbbb/cccccccccccccccccccccccc`. You'll need this in the next step.

2. Create a package binding with your Slack credentials, the channel that you want to post to, and the user name to post as.

  ```
  wsk package bind /whisk.system/slack mySlack --param url 'https://hooks.slack.com/services/...' --param username 'Bob' --param channel '#MySlackChannel'
  ```
  {: pre}

3. Invoke the `post` action in your package binding to post a message to your Slack channel.

  ```
  wsk action invoke mySlack/post --blocking --result --param text 'Hello from OpenWhisk!'
  ```
  {: pre}


## Using the GitHub package
{: #openwhisk_catalog_github}

The `/whisk.system/github` package offers a convenient way to use the [GitHub APIs](https://developer.github.com/).

The package includes the following feed:

| Entity | Type | Parameters | Description |
| --- | --- | --- | --- |
| `/whisk.system/github` | package | username, repository, accessToken | Interact with the GitHub API |
| `/whisk.system/github/webhook` | feed | events, username, repository, accessToken | Fire trigger events on GitHub activity |

While not required, it's suggested that you create a package binding with the `username`, `repository`, and `accessToken` values.  With binding, you don't need to specify the values each time that you use the feed in the package.

### Firing a trigger event with GitHub activity

The `/whisk.system/github/webhook` feed configures a service to fire a trigger when there is activity in a specified GitHub repository. The parameters are as follows:

- `username`: The username of the GitHub repository.
- `repository`: The GitHub repository.
- `accessToken`: Your GitHub personal access token. When you [create your token](https://github.com/settings/tokens), be sure to select the repo:status and public_repo scopes. Also, make sure you don't have any Webhooks already defined for your repository.
- `events`: The [GitHub activity type](https://developer.github.com/v3/activity/events/types/) of interest.

The following is an example of creating a trigger that will be fired each time that there is a new commit to a GitHub repository.

1. Generate a GitHub [personal access token](https://github.com/settings/tokens).

  The access token will be used in the next step.


2. Create a package binding configured for your GitHub respository and with your accesss token.

  ```
  wsk package bind /whisk.system/github myGit --param username myGitUser --param repository myGitRepo --param accessToken aaaaa1111a1a1a1a1a111111aaaaaa1111aa1a1a
  ```
  {: pre}

3. Create a trigger for the GitHub `push` event type using your `myGit/webhook` feed.

  ```
  wsk trigger create myGitTrigger --feed myGit/webhook --param events push
  ```
  {: pre}

