# **Intents, Activities, and SharedPreferences**

## **Tasks and Back Stack**

* A task: is a collection of activities that users interact with when performing a certain job.
* The activities are arranged in a stack (the back stack).
* when we open specific app, the current activity has been pushed to back stack ,then if we want to open another activity in the same app the new activity will push to the back stack ,If the user presses the Back button, that new activity is finished and popped off the stack.
* the system manages tasks, or groups of tasks, on a per-window basis.
* When all activities are removed from the stack, the task no longer exists.
* A task is a cohesive unit that can move to the "background" when users begin a new task or go to the Home screen, via the Home button.
* While in the background, all the activities in the task are stopped.
* When the user leaves a task by pressing the Home button, the current activity is stopped and its task goes into the background.
* The system retains the state of every activity in the task.
* If the user later resumes the task by selecting the launcher icon that began the task, the task comes to the foreground and resumes the activity at the top of the stack.

### **Managing Tasks**

* ```<activity>``` manifest element in the intent that you pass to startActivity() has a principal attributes:
  * taskAffinity.
  * launchMode.
  * allowTaskReparenting.
  * clearTaskOnLaunch.
  * alwaysRetainTaskState.
  * finishOnTaskLaunch.

* And it hase principal intent flags:
  * FLAG_ACTIVITY_NEW_TASK
  * FLAG_ACTIVITY_CLEAR_TOP
  * FLAG_ACTIVITY_SINGLE_TOP

* We use these manifest attributes and intent flags to define how activities are associated with tasks and how they behave in the back stack.

### **Defining launch modes**

* Launch modes allow you to define how a new instance of an activity is associated with the current task.
* We can define different launch modes in two ways:
    1. Using the manifest file
    2. Using Intent flags

### **Using the manifest file**

* We can specify how the activity should associate with a task using the ```<activity>``` element's launchMode attribute in manifest file.
* Launch modes have four different mode can assign to the launchMode attribute:
    1. standard.
    2. singleTop.
    3. singleTask.
    4. singleInstance.

### **Using Intent flags**

* When starting an activity, you can modify the default association of an activity to its task by including flags in the intent that you deliver to startActivity().
* The flags we can use to modify the default behavior are:
    1. FLAG_ACTIVITY_NEW_TASK.
    2. FLAG_ACTIVITY_SINGLE_TOP.
    3. FLAG_ACTIVITY_CLEAR_TOP.

### **Handling affinities**

* The affinity indicates which task an activity prefers to belong to.
* By default, all activities in the same app prefer to be in the same task.

### **Clearing the back stack**

* If the user leaves a task for a long time, the system clears the task of all activities except the root activity.
* There are some activity attributes that we can use to modify this behavior:
    1. alwaysRetainTaskState.
    2. clearTaskOnLaunch.
    3. finishOnTaskLaunch.

## **Save key-value data** 

* SharedPreferences APIs: is a object points to a file containing key-value pairs and provides simple methods to read and write them.
* SharedPreferences APIs managed by the framework and can be private or shared.
* we can create a new shared preference file or access an existing one by calling one of these methods:
    1. getSharedPreferences().
    2. getPreferences().

### **How to Write to shared preferences**

1. create a SharedPreferences.Editor by calling edit() on your SharedPreferences.
2. Pass the keys and values you want to write with methods such as putInt() and putString().
3. call apply() or commit() to save the changes.

### **How to Read from shared preferences**

1. Call methods such as getInt() and getString().
2. Providing the key for the value you want.
3. Optionally a default value to return if the key isn't present.



[HOME](https://malkhaleel88.github.io/reading-notes)