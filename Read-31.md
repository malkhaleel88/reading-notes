# **Espresso**

![Espresso](https://developer.android.com/images/training/testing/espresso.png)

## **Espresso Testing**

* We can Use Espresso to write concise, beautiful, and reliable Android UI tests.

```
@Test
public void greeterSaysHello() {
    onView(withId(R.id.name_field)).perform(typeText("Steve"));
    onView(withId(R.id.greet_button)).perform(click());
    onView(withText("Hello Steve!")).check(matches(isDisplayed()));
}
```

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

1. espresso-core - Contains core and basic View matchers, actions, and assertions. See Basics and Recipes.
2. espresso-web - Contains resources for WebView support.
3. espresso-idling-resource - Espresso's mechanism for synchronization with background jobs.
4. espresso-contrib - External contributions that contain DatePicker, RecyclerView and Drawer actions, accessibility checks, and CountingIdlingResource.
5. espresso-intents - Extension to validate and stub intents for hermetic testing.
6. espresso-remote - Location of Espresso's multi-process functionality.


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

### **Add assertions to verify UI elements**

* Assertions verify the existence or contents of a View element through three main types:

1. text is: Checks the text content of the selected View element
2. exists: Checks that the View element is present in the current View hierarchy visible on the screen
3. does not exist: Checks that the View element is not present in the current View hierarchy


[HOME](https://malkhaleel88.github.io/reading-notes)