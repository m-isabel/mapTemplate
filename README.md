mapTemplate
===========

This is a generic GoogleMaps template for Android.

Keep in mind that you still need to install Google Play Services SDK + anything extra. You will also need to get your SHA1 key and the API Key.

Windows Command to get SHA1 key:

1. Go to the directory project.
2. Generate the key with keytool. I am using Cygwin, so the command will be similar with the exception of your directories.


$ "/cygdrive/c/Program Files/Java/jre7/bin/keytool" -genkey -v -keystore debug.keystore -storepass android -alias 
androiddebugkey -keypass android -dname "CN=Android Debug,O=Android,C=US"

3. Get your SHA1 key, type:

$ "/cygdrive/c/Program Files/Java/jre7/bin/keytool" -list -v -keystore debug.keystore -storepass android -alias 
androiddebugkey -keypass android -dname "CN=Android Debug,O=Android,C=US"

4. Go to console.developer.google.com, create a project.
5. Go to APIs and find Google Maps Android API v2. Turn it on.
6. Go to credentials. Create a new key with Android key. Put your SHA1 key and your project package name (com.user1.mymap)
7. It will now generate a new key, use it and replace the google_key string in the XML file.

Hope this helps! Enjoy!

