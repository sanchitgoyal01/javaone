Tutorial Resources
=======

## Cordova

http://cordova.apache.org/

## Eclipse Thym 

https://www.eclipse.org/thym/

## JBoss Tools

http://tools.jboss.org/

## Using Native Features 

### Camera demo 

Be sure to have the camera plugin installed

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

## ionic

http://ionicframework.com/

http://codepen.io/ionic/public-list/

http://ngcordova.com/

https://github.com/sebastienblanc/javaonesearch


## UnifiedPush Server

http://aerogear.org/push/

https://github.com/aerogear/aerogear-push-helloworld

https://github.com/aerogear/aerogear-push-quickstarts

## Keycloak

http://keycloak.jboss.org/

https://github.com/lfryc/keycloak/tree/ionic-styling/

## Demo Apps

Client : https://github.com/sebastienblanc/ionic-keycloak-client
Backend : 

## Other Resource 

AeroGear IRC : #aerogear

AeroGear ML : aerogear-dev@lists.jboss.org aerogear-user@lists.jboss.org

My Twitter handle : @sebi2706





