# Camera code

```
<!DOCTYPE html>
<html>
  <head>
    <title>Capture Photo</title>

    <script type="text/javascript" charset="utf-8" src="cordova.js"></script>
    <script type="text/javascript" charset="utf-8">

    var pictureSource;   // picture source
    var destinationType; // sets the format of returned value

    // Wait for device API libraries to load
    //
    document.addEventListener("deviceready",onDeviceReady,false);

    // device APIs are available
    //
    function onDeviceReady() {
        pictureSource=navigator.camera.PictureSourceType;
        destinationType=navigator.camera.DestinationType;
    }

    // Called when a photo is successfully retrieved
    //
    function onPhotoDataSuccess(imageData) {
      // Get image handle
      //
      var largeImage = document.getElementById('largeImage');

      // Unhide image elements
      //
      largeImage.style.display = 'block';

      // Show the captured photo
      // The inline CSS rules are used to resize the image
      //
      largeImage.src = "data:image/jpeg;base64," + imageData;
    }


    // A button will call this function
    //
    function capturePhoto() {
      // Take picture using device camera and retrieve image as base64-encoded string
      navigator.camera.getPicture(onPhotoDataSuccess, onFail, { quality: 50,
        destinationType: destinationType.DATA_URL });
    }

    // Called if something bad happens.
    //
    function onFail(message) {
      alert('Failed because: ' + message);
    }

    </script>
  </head>
  <body>
    <button onclick="capturePhoto();">Capture Photo</button> <br>
    <img style="display:none;" id="largeImage" src="" />
  </body>
</html>

```


## forge

```
project-new --named whatever
jpa-new-entity --named name
jpa-new-field --named fieldName
 
```


## UPS 

```
    <dependency>
         <groupId>org.jboss.aerogear</groupId>
         <artifactId>unifiedpush-java-client</artifactId>
         <version>1.0.0</version>
    </dependency>
``` 


## keycloak


```
 var keycloak = new Keycloak();  
    
    keycloak.init({ onLoad: 'login-required' }).success(function(){
    	$rootScope.token = keycloak.token;
    	
    	
    	pushConfig.alias = keycloak.idToken.preferred_username;
        push.register(onNotification, successHandler, errorHandler, pushConfig); 
    });

```

## jboss-web.xml 

```
<jboss-web>
    <valve>
        <class-name>org.keycloak.adapters.as7.KeycloakAuthenticatorValve</class-name>
    </valve>
</jboss-web>
```

## web.xml

```
<?xml version="1.0" encoding="UTF-8"?>
<web-app xmlns="http://java.sun.com/xml/ns/javaee"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://java.sun.com/xml/ns/javaee http://java.sun.com/xml/ns/javaee/web-app_3_0.xsd"
         version="3.0">

   

    <security-constraint>
        <web-resource-collection>
            <web-resource-name>example</web-resource-name>
            <url-pattern>/rest/*</url-pattern>
        </web-resource-collection>
        <auth-constraint>
            <role-name>user</role-name>
        </auth-constraint>
    </security-constraint>

   

    <login-config>
        <auth-method>KEYCLOAK</auth-method>
        <realm-name>example</realm-name>
    </login-config>

    <security-role>
        <role-name>user</role-name>
    </security-role>

</web-app>

```

# keycloak.json	

```
{
  "realm" : "example",
  "realm-public-key": "MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQCrVrCuTtArbgaZzL1hvh0xtL5mc7o0NqPVnYXkLvgcwiC3BjLGw1tGEGoJaXDuSaRllobm53JBhjx33UNv+5z/UMG4kytBWxheNVKnL6GgqlNabMaFfPLPCF8kAgKnsi79NMo+n6KnSY8YeUmec/p2vjO2NjsSAVcWEQMVhJ31LwIDAQAB",
  "auth-server-url" : "https://javaonekc-sblanc.rhcloud.com/auth/",
  "ssl-required" : "external",
  "resource" : "awesome",
  "bearer-only" : true,
  "disable-trust-manager" : true
}
```


