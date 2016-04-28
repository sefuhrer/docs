---

 

copyright:

  years: 2015，2016

 

---

{:shortdesc: .shortdesc} 
{:new_window: target="_blank"}

# Creating Cloud Foundry apps
*Last updated: 18 April 2016*

With {{site.data.keyword.Bluemix}}, you can create your app in the {{site.data.keyword.Bluemix_notm}} user interface. After it's created, you can decide to continue to use the UI, use the cf command line interface, or use {{site.data.keyword.jazzhub_title}} to develop, track, plan, and deploy your app.
{:shortdesc}

When you create an app in {{site.data.keyword.Bluemix_notm}}, you begin with a starter. A *starter* is a template that includes predefined services and application code that is configured with a particular buildpack. There are two types of starters: boilerplates and runtimes.

A *boilerplate* is a container for an application and its associated runtime environment and predefined services for a particular domain. For example, the Mobile Cloud boilerplate includes a Node.js runtime, as well as the Mobile Data, Mobile Application Security, and Push services. It also includes an SDK and sample applications to get started developing mobile apps that access these services.

A *runtime* is the set of resources that is used to run an application. {{site.data.keyword.Bluemix_notm}} provides runtime environments as containers for different types of applications. The runtime environments are integrated as buildpacks into {{site.data.keyword.Bluemix_notm}}, are automatically configured for use, and require little to no maintenance.

To get started creating your application, take the following steps:
  1. Go to the Dashboard in the {{site.data.keyword.Bluemix_notm}} user interface.
  2. Click **CREATE AN APP**.
  3. Click **WEB** and follow the guided experience to choose a starter, specify a name, and select how you want to code.
  4. When you are finished with the guided experience, click **VIEW APP OVERVIEW**. The Overview for your app is displayed on the Dashboard.
  5. You can add a service to your app by clicking **ADD A SERVICE OR API** on the app Overview in the Bluemix user interface. Browse and select services from the catalog, or, scroll to the end of the catalog and click **{{site.data.keyword.Bluemix_notm}} Experimental Services** to browse experimental services. Or, you can use the cf command line interface. See Options for working with apps.
  6. On the app Overview, click Add Git to save your application source in a Git repository and create a Git hosted project. You can also deploy the application from {{site.data.keyword.jazzhub_title}}.

**Note:** If a service that you bind to an app crashes, the app might stop running or have errors. {{site.data.keyword.Bluemix_notm}} does not automatically restart the app to recover from these problems. Consider coding your app to identify and recover from outages, exceptions, and connection failures. See the Apps are not automatically restarted troubleshooting topic for more information.

## Options for working with apps

After your app is created, you have a few options for continuing to add services to your app and to build and deploy your app:

<dl><dt>cf command line interface</dt>
<dd>Use the cf command line interface to update your application, create a service instance, or bind the service to your application. You can also use the cloud-cli command line interface to create, update, and delete service offerings.</dd>
<dt>{{site.data.keyword.Bluemix_notm}} user interface</dt>
<dd>Use the {{site.data.keyword.Bluemix_notm}} user interface to build your application, including picking which services and runtimes to combine to solve your business problem.</dd>
<dt>{{site.data.keyword.jazzhub_title}}</dt>
<dd>Use {{site.data.keyword.jazzhub_title}} to create an application in the cloud and deploy it to {{site.data.keyword.Bluemix_notm}}. The services that are provided by {{site.data.keyword.jazzhub_title}} include Track & Plan and Delivery Pipeline, listed in the {{site.data.keyword.Bluemix_notm}} Catalog under DevOps, as well as Web IDE and Git hosting.</dd>
</dl>

## Tips

Use the following tips while developing your web apps:

<dl><dt>Persistence</dt>
<dd>Do not specify any local storage for your applications. Each instance of your application, even if only one instance is running, can be restarted or moved to a different virtual machine at any time, typically for load balancing. Anything stored in local storage is erased when the application is moved or deleted. Use one of the Bluemix data store services for persistence.</dd>
<dt>Resource limits</dt>
<dd>Be aware of limits on the quantities of resources that a trial account can use. The limits are as follows:
<table style="width:100%">
  <th>Resource type</th>	<th>Quantity limit</th>
<tr><td>Number of services that are used across all apps</td> <td>10</td>
<tr><td>Memory used across all apps</td> <td>	2 G</td>
<tr><td>Number of routes</td> <td>500</td>
</table>
</dd></dl>

*Table 1. {{site.data.keyword.Bluemix_notm}} resource limits for a trial account*
