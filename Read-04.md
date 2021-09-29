# **Object-Oriented Programming "OOP"**


## **Object-Oriented Programming Concepts**

### **What Is an Object?**

*An object is a software bundle of related state and behavior. Software objects are often used to model the real-world objects that you find in everyday life. This lesson explains how state and behavior are represented within an object, introduces the concept of data encapsulation, and explains the benefits of designing your software in this manner.*

![Objects](https://docs.oracle.com/javase/tutorial/figures/java/concepts-object.gif)

**A software object**


### **What Is a Class?**

*A class is a blueprint or prototype from which objects are created. This section defines a class that models the state and behavior of a real-world object. It intentionally focuses on the basics, showing how even a simple class can cleanly model state and behavior.*

**Example :**
```

class Bicycle {

    int cadence = 0;
    int speed = 0;
    int gear = 1;

    void changeCadence(int newValue) {
         cadence = newValue;
    }

    void changeGear(int newValue) {
         gear = newValue;
    }

    void speedUp(int increment) {
         speed = speed + increment;   
    }

    void applyBrakes(int decrement) {
         speed = speed - decrement;
    }

    void printStates() {
         System.out.println("cadence:" +
             cadence + " speed:" + 
             speed + " gear:" + gear);
    }
}
```
### **Declaring Classes**

***Class declarations can include these components, in order:***

* Modifiers such as public, private, and a number of others that you will encounter later. (However, note that the private modifier can only be applied to Nested Classes.)
* The class name, with the initial letter capitalized by convention.
* The name of the class's parent (superclass), if any, preceded by the keyword extends. A class can only extend (subclass) one parent.
* A comma-separated list of interfaces implemented by the class, if any, preceded by the keyword implements. A class can implement more than one interface.
* The class body, surrounded by braces, {}.

**Defining Methods**

***Method declarations have six components, in order:***

* Modifiers—such as public, private, and others you will learn about later.
* The return type—the data type of the value returned by the method, or void if the method does not return a value.
* The method name—the rules for field names apply to method names as well, but the convention is a little different.
* The parameter list in parenthesis—a comma-delimited list of input parameters, preceded by their data types, enclosed by parentheses, (). If there are no parameters, you must use empty parentheses.
* An exception list—to be discussed later.
* The method body, enclosed between braces—the method's code, including the declaration of local variables, goes here.

**A method returns to the code that invoked it when it**

* Completes all the statements in the method.
* Reaches a return statement.
* Throws an exception (covered later).

***Within an instance method or a constructor, this is a reference to the current object — the object whose method or constructor is being called. You can refer to any member of the current object from within an instance method or a constructor by using this.***

## **Binary, Decimal and Hexadecimal Numbers**

### **Binary Numbers**

*Binary Numbers are just "Base 2" instead of "Base 10". So you start counting at 0, then 1, then you run out of digits ... so you start back at 0 again, but increase the number on the left by 1.*

![Binary](https://assets.sutori.com/user-uploads/image/5af5782f-c329-42b3-b03b-86b21ffd1d44/3d3926d9b1f70c0d7d4987356989d80b.gif)

### **Decimal Numbers**

*Every digit in a decimal number has a "position", and the decimal point helps us to know which position is.*
*The Decimal Number System is also called "Base 10", because it is based on the number 10.*

![Decimal](https://www.assignmentpoint.com/wp-content/uploads/2017/10/Rounding-Decimals.jpg)


### **Hexadecimal Numbers**

*They look the same as the decimal numbers up to 9, but then there are the letters ("A',"B","C","D","E","F") in place of the decimal numbers 10 to 15.*



[HOME](https://malkhaleel88.github.io/reading-notes)