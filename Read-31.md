# **Espresso**

## **Espresso Testing**

* We can Use Espresso to write concise, beautiful, and reliable Android UI tests.
* Espresso tests state expectations, interactions, and assertions clearly without the distraction of boilerplate content, custom infrastructure, or messy implementation details getting in the way.

### **Target audience**

* Espresso is targeted at developers, who believe that automated testing is an integral part of the development lifecycle.
* it can be used for black-box testing,
* Espresso’s full power is unlocked by those who are familiar with the codebase under test.

### **Synchronization capabilities**

* the following synchronization conditions are met:

1. The message queue is empty.
2. There are no instances of AsyncTask currently executing a task.
3. All developer-defined idling resources are idle.

### **Packages**

* espresso-core
* espresso-web
* espresso-idling-resource
* espresso-contrib
* espresso-intents
* espresso-remote

## **Create UI tests with Espresso Test Recorder**

* The Espresso Test Recorder tool lets you create UI tests for your app without writing any test code.
* By recording a test scenario, you can record your interactions with a device and add assertions to verify UI elements in particular snapshots of your app.
* Espresso Test Recorder then takes the saved recording and automatically generates a corresponding UI test that you can run to test your app.
* Espresso Test Recorder writes tests based on the Espresso Testing framework.
* Espresso API encourages you to create concise and reliable UI tests based on user actions.
* Before using Espresso Test Recorder, make sure you turn off animations on your test device to prevent unexpected results.
* Espresso tests consist of two primary components
  * UI interactions and assertions on View elements
  * UI interactions include tap and type actions that a person may use to interact with your app

### **Record UI interactions**

* To start recording a test with Espresso Test Recorder, proceed as follows:

1. Click Run > Record Espresso Test.
2. In the Select Deployment Target window, choose the device on which you want to record the test.
3. Espresso Test Recorder triggers a build of your project, and the app must install and launch before Espresso Test Recorder allows you to interact with it.