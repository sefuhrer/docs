---

copyright:
  years: 2015, 2016
  
---

# Comunicações de backend para backend
{: #backend-comm}

Em alguns cenários avançados, pode ser necessário enviar solicitações de seu aplicativo backend que está em execução no {{site.data.keyword.Bluemix}} para outro serviço de backend que está protegido pelo serviço {{site.data.keyword.amashort}}, por exemplo, o serviço {{site.data.keyword.cloudant}}. Nesses casos, deve-se incluir um token OAuth na solicitação.

Use o módulo npmjs `bms-mca-oauth-sdk` para obter e injetar tokens OAuth nas solicitações.

## Instalando o módulo bms-mca-oauth-sdk
{: #sdk}

Em uma linha de comandos, abra o diretório do aplicativo Node.js e execute o comando a seguir:

```Bash
npm install -save bms-mca-oauth-sdk
```

## Usando o módulo bms-mca-oauth-sdk
{: #using-sdk}

O código a seguir demonstra como usar o módulo `bms-mca-oauth-sdk`.


``` JavaScript
var oauthSDK = require('bms-mca-oauth-sdk');

var options = {

	// É possível armazenar tokens em cache para evitar roundtrips extras em cada solicitação
	// Essa propriedade define o número de tokens a serem armazenados em cache

	cacheSize: 100,

	// Todas as propriedades abaixo são recuperadas automaticamente quando o Node.js
 // é executado no {{site.data.keyword.Bluemix_notm}} e ligado a uma instância do serviço {{site.data.keyword.amashort}}.
	// Como alternativa, é possível obter esses valores de propriedades clicando em Mostrar credenciais
	// no quadro do serviço {{site.data.keyword.amashort}} no painel do aplicativo {{site.data.keyword.Bluemix_notm}}

	appId: "appId",				// applicationGUID do Bleumix, conhecido como tenantId
	clientId: "clientId",			
	secret: "secret",
	serverUrl: "serverUrl"
};

oauthSDK.getAuthorizationHeader(options).then(function(authHeader){

	// In the request that you want to send to the protected
resource, 	// add the authHeader value.

	request.headers.Authorization = authHeader;

	// Enviar solicitação

});

```
