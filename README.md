
This is a fork of the plugin under [https://github.com/darryncampbell/darryncampbell-cordova-plugin-intent](https://github.com/darryncampbell/darryncampbell-cordova-plugin-intent)

With the following:


* Within plugin.xml to use the correct package path/namespace (the one used in the .java file)

   ```<source-file src="src/android/IntentShim.java" target-dir="src/com/darryncampbell/cordova/plugin/intent" />```

  `/cordova` was missing...and the plugin class could not be instantiated...


* Updated the `getIntent` action, in order to add one extra to it, whenever the app was launched from recent apps (means it was resumed, and not really launched from icon on home screen/notification).
This way, the consuming application will be able to to determine the appropriate routing/state/screen, depending on whether the app was launched vs. resumed/recovered from recent apps...