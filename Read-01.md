# **Java Basics**


## **Variables**

*The Java programming language defines the following kinds of variables:*

* **Instance Variables (Non-Static Fields)** Technically speaking, objects store their individual states in "non-static fields", that is, fields declared without the static keyword.

* **Class Variables (Static Fields)** A class variable is any field declared with the static modifier; this tells the compiler that there is exactly one copy of this variable in existence, regardless of how many times the class has been instantiated.

* **Local Variables** Similar to how an object stores its state in fields, a method will often store its temporary state in local variables. The syntax for declaring a local variable is similar to declaring a field (for example, int count = 0;). There is no special keyword designating a variable as local; that determination comes entirely from the location in which the variable is declared — which is between the opening and closing braces of a method. As such, local variables are only visible to the methods in which they are declared; they are not accessible from the rest of the class.

* **Parameters** Recall that the signature for the main method is public static void main(String[] args). Here, the args variable is the parameter to this method. The important thing to remember is that parameters are always classified as "variables" not "fields". This applies to other parameter-accepting constructs as well (such as constructors and exception handlers) that you'll learn about later in the tutorial.

### **Primitive Data Types**

![Primitive Data Types](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20191105122725/Primitive-Data-Types-in-Java-4.jpg)

**Examples:**
```
boolean result = true;
byte b = 100;
char capitalC = 'C';
short s = 10000;
int i = 100000;
long cardNumber = 1234_5678_9012_3456L;
float f1  = 123.4f;
double d1 = 123.4d;
```

### **Arrays**
*An array is a container object that holds a fixed number of values of a single type. The length of an array is established when the array is created. After creation, its length is fixed.*

![Arrays](https://docs.oracle.com/javase/tutorial/figures/java/objects-tenElementArray.gif)

**declaring arrays**
```
int[] anArray;
String[] anArrayOfStrings;
```

## **Operators**

![Operators](https://www.softwaretestingmaterial.com/wp-content/uploads/2018/03/Operators-Table.png)

## **Expressions, Statements, and Blocks**

### **Expressions**
*An expression is a construct made up of variables, operators, and method invocations, which are constructed according to the syntax of the language, that evaluates to a single value.*

**Examples:**
```
int cadence = 0;
anArray[0] = 100;
System.out.println("Element 1 at index 0: " + anArray[0]);

int result = 1 + 2; // result is now 3
if (value1 == value2) 
    System.out.println("value1 == value2");
```

### **Statements**
*Statements are roughly equivalent to sentences in natural languages. A statement forms a complete unit of execution.*

**Examples:**
```
// assignment statement
aValue = 8933.234;
// increment statement
aValue++;
// method invocation statement
System.out.println("Hello World!");
// object creation statement
Bicycle myBike = new Bicycle();
// declaration statement
double aValue = 8933.234;
```

### **Blocks**
*A block is a group of zero or more statements between balanced braces and can be used anywhere a single statement is allowed.*

**Examples:**
```
class BlockDemo {
     public static void main(String[] args) {
          boolean condition = true;
          if (condition) { // begin block 1
               System.out.println("Condition is true.");
          } // end block one
          else { // begin block 2
               System.out.println("Condition is false.");
          } // end block 2
     }
}
```

## **Control Flow Statements**
![Control Flow Statements](https://1.bp.blogspot.com/-nh6ZkX6q_Dk/Xfc0S5zftiI/AAAAAAAAE24/y2brpWATADoxtCdeKt7Fv7nKaxx9dvTeQCLcBGAsYHQ/s1600/Screenshot%2B%2528463%2529.png)

*The statements inside your source files are generally executed from top to bottom, in the order that they appear. Control flow statements, however, break up the flow of execution by employing decision making, looping, and branching, enabling your program to conditionally execute particular blocks of code. This section describes the decision-making statements (if-then, if-then-else, switch), the looping statements (for, while, do-while), and the branching statements (break, continue, return) supported by the Java programming language.*

