# Android Fundamentals

Android apps can be written using Kotlin, Java, and C++ languages. The Android SDK tools compile your code along with any data and resource files into an APK or an Android App Bundle.


*_There are four different types of app components:_*

    1- *Activities* :It represents a single screen with a user interface , You implement an activity as a subclass of the Activity class.

    2- *Services* : It is a component that runs in the background to perform long-running operations or to perform work for remote processes , is implemented as a subclass of Service .

    3- *Broadcast receivers* : allowing the app to respond to system-wide broadcast announcements , is implemented as a subclass of BroadcastReceiver and each broadcast is delivered as an Intent object . 

    4- *Content providers* : manages a shared set of app data that you can store in the file system, in a SQLite database, on the web, or on any other persistent storage location that your app can access , is implemented as a subclass of ContentProvider and must implement a standard set of APIs that enable other apps to perform transactions.


_You must declare all app components using the following elements:_

   _ <activity> elements for activities.
   _ <service> elements for services.
   _ <receiver> elements for broadcast receivers.
   _ <provider> elements for content providers.

Activities, services, and content providers that you include in your source but do not declare in the manifest are not visible to the system and, consequently, can never run. However, broadcast receivers can be either declared in the manifest or created dynamically in code as BroadcastReceiver objects and registered with the system by calling registerReceiver().

_ You can declare an intent filter for your component by adding an <intent-filter> element as a child of the component's declaration element._

_The values for minSdkVersion and targetSdkVersion are set in your app module's build.gradle file: _



_ Declare the camera feature directly in your app's manifest file:_

<manifest ... >
    <uses-feature android:name="android.hardware.camera.any"
                  android:required="true" />
    ...
</manifest>

_App resources_
An Android app is composed of more than just code—it requires resources that are separate from the source code, such as images, audio files, and anything relating to the visual presentation of the app

