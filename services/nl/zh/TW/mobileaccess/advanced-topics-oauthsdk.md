---

copyright:
  years: 2015, 2016
  
---

# 後端對後端通訊
{: #backend-comm}

在部分進階情境中，您可能需要將來自 {{site.data.keyword.Bluemix}} 上執行之後端應用程式的要求，傳送至 {{site.data.keyword.amashort}} 服務所保護的另一個後端服務（例如 {{site.data.keyword.cloudant}} 服務）。在這些情況下，您必須將 OAuth 記號新增至要求。

使用 `bms-mca-oauth-sdk` npmjs 模組，以取得 OAuth 記號並將其注入要求中。

## 安裝 bms-mca-oauth-sdk 模組
{: #sdk}

在指令行上，開啟 Node.js 應用程式目錄，然後執行下列指令：

```Bash
npm install -save bms-mca-oauth-sdk
```

## 使用 bms-mca-oauth-sdk 模組
{: #using-sdk}

下列程式碼示範如何使用 `bms-mca-oauth-sdk` 模組。


``` JavaScript
var oauthSDK = require('bms-mca-oauth-sdk');

var options = {

	// You can cache tokens to avoid extra roundtrips on every request
	// This property defines the number of tokens to be cached

	cacheSize: 100,

	// All of the below properties are retrieved automatically when your Node.js
	// runs on {{site.data.keyword.Bluemix_notm}} and bound to an instance of {{site.data.keyword.amashort}} Service.
	// Alternatively you can get these properties values by clicking Show Credentials
	// on the {{site.data.keyword.amashort}} Service tile in your {{site.data.keyword.Bluemix_notm}} application dashboard

	appId: "appId",				// Bleumix applicationGUID, a.k.a tenantId
	clientId: "clientId",			
	secret: "secret",
	serverUrl: "serverUrl"
};

oauthSDK.getAuthorizationHeader(options).then(function(authHeader){

	// In the request that you want to send to the protected resource, 
	// add the authHeader value.

	request.headers.Authorization = authHeader;

	// Send request

});

```
