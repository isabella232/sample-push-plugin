- [Description](#description)
- [Requirements](#requirements)
- [Getting started](#getting-started)

# Description

This sample shows an integration between the [NativeScript Push Notifications plugin](https://github.com/NativeScript/push-plugin) with [Telerik Backend Services](http://www.telerik.com/backend-services). 

# Requirements

   * Registration in [Telerik Platform](https://platform.telerik.com)
   * A new or existing Backend Services project in your Platform account.
   * The project must be configured for push notifications as specified in the Backend Services [documentation](http://docs.telerik.com/platform/backend-services/features/push-notifications/setup).

> In order to send a notification to a subset of users you will need a Telerik Platform [subscription plan](http://www.telerik.com/purchase/platform) that supports "Push to Segment".

# Running the sample

- Add the NativeScript Push Plugin

		tns plugin add nativescript-push-notifications 	

- Go to main-view-model and set the correct settings:
	-	 Set your Everlive API Key at:

			self.everlive = new Everlive('<ENTER_YOUR_API_KEY_HERE>');
	-	 Android: Set your project number
 
			projectNumber: '<ENTER_YOUR_PROJECT_NUMBER>'
	
## Android

- Add the android platform to the sample

		tns platform add android 

- Add Google Play Services, as GCM is part of it. It's present in the android-sdk. Add it like this (NOTE: your path may be different, it depends on the installation path of the Android SDK): 

		tns library add android C:\Users\your_user_name\AppData\Local\Android\android-sdk\extras\google\google_play_services\libproject\google-play-services_lib\libs


- Run the application

		tns run android

- Click Register to register the device in Backend Services and you can start sending push notifications from your account.

## iOS

- Set the correct bundle ID in the package.json at the root level of the project. The ID should be the same as in your Certificate for Push Notifications.

```javascript
	"nativescript": {
		"id": "com.telerik.PushNotificationApp",
		...
	}
````

- Add the iOS platform to the sample

		tns platform add ios

- Run the applications

		tns run ios

	  