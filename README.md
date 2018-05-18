This is a fork of the plugin under https://github.com/darryncampbell/darryncampbell-cordova-plugin-intent
Includes just a small change within plugin.xml to use the correct package path/namespace (the one used in the .java file)

<source-file src="src/android/IntentShim.java" target-dir="src/com/darryncampbell/cordova/plugin/intent" />

/cordova was missing...and the plugin class could not be instantiated by cordova, at least in my case...

