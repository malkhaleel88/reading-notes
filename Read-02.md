# **Arrays, Loops, Imports**


## **Java Packages and Import**

* **Package = directory.** Java classes can be grouped together in packages. A package name is the same as the directory (folder) name which contains the .java files. You declare packages when you define your Java program, and you name the packages you want to use from other libraries in an import statement.*

### **Package declaration syntax**

*The statement order is as follows. Comments can go anywhere.*

* Package statment (optional).
* Imports (optional).
* Class or interface definitions.

### **Common imports**

* **import java.awt.*; Common GUI elements.**
* **import java.awt.event.*; The most common GUI event listeners.**
* **import javax.swing.*; More common GUI elements. Note "javax".**
* **import java.util.*; Data structures (Collections), time, Scanner, etc classes.**
* **import java.io.*; Input-output classes.**
* **import java.text.*; Some formatting classes.**
* **import java.util.regex.*; Regular expression classes.**



## **Different types of loops in Java**

### **Types of loops that we can find in Java:**

* **Simple for loop**
```
for (int i = 0; i <= 10; i = i + 2) {
  System.out.println(i);
}
```
* **Enhanced for-each loop**
```
for (type variableName : arrayName) {
  // code block to be executed
}
```
* **While loop**
```
while (condition) {
  // code block to be executed
}
```
* **Do-While loop**
```
do {
  // code block to be executed
}
while (condition);
```


[HOME](https://malkhaleel88.github.io/reading-notes)