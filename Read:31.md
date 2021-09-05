# Espresso

Use Espresso to write concise, beautiful, and reliable Android UI tests.

The Espresso Test Recorder tool lets you create UI tests for your app without writing any test code. By recording a test scenario, you can record your interactions with a device and add assertions to verify UI elements in particular snapshots of your app. Espresso Test Recorder then takes the saved recording and automatically generates a corresponding UI test that you can run to test your app.



_Synchronization capabilities_

Each time your test invokes onView(), Espresso waits to perform the corresponding UI action or assertion until the following synchronization conditions are met:

    The message queue is empty.
    There are no instances of AsyncTask currently executing a task.
    All developer-defined idling resources are idle.


_Record UI interactions_

To start recording a test with Espresso Test Recorder, proceed as follows:

    Click Run > Record Espresso Test.
    In the Select Deployment Target window, choose the device on which you want to record the test. If necessary, create a new Android Virtual Device. Click OK.
    Espresso Test Recorder triggers a build of your project, and the app must install and launch before Espresso Test Recorder allows you to interact with it. The Record Your Test window appears after the app launches, and since you have not interacted with the device yet, the main panel reads "No events recorded yet." Interact with your device to start logging events such as "tap" and "type" actions.


_Save a recording_

    Click Complete Recording.
    Use the Test class name text field if you want to change the suggested name. Click Save.
    Android Studio shows the test class as selected in the Project window of the IDE.
