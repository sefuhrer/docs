---

Copyright :
  Années : 2015, 2016

---

# Enregistrement de périphériques Android
{: #android_register}

Utilisez l'API **IMFPush.register()** pour enregistrer le périphérique auprès d'un service Notification push. 

Copiez et collez les fragments de code suivants dans votre application mobile Android :

```
	//Enregistrez des périphériques Android
	push.register(new MFPPushResponseListener<String>() {
	    @Override
	    public void onSuccess(String deviceId) {
	           //Traitement de la réussite
	    }
	    @Override
	    public void onFailure(MFPPushException ex) {
	    //Traitement de l'échec
	    }
	});
```

```
	//Traitement de la notification lorsqu'elle arrive
	MFPPushNotificationListener notificationListener = new MFPPushNotificationListener() {
	    @Override
	    public void onReceive (final MFPSimplePushNotification message){
	      // Traitement de la notification push
	    }
	};
```
