# **Inheritance and Interfaces**

## **Inheritance**

*Mechanism in which one object acquires all the properties and behaviors of a parent object. It is an important part of OOPs(Object Oriented programming system).*

*The idea behind inheritance in Java is that you can create new classes that are built upon existing classes. When you inherit from an existing class, you can reuse methods and fields of the parent class. Moreover, you can add new methods and fields in your current class also.*

**The syntax of Java Inheritance**
```
class Subclass-name extends Superclass-name  
{  
   //methods and fields  
}  
```
![Inheritance](https://www.scientecheasy.com/wp-content/uploads/2020/07/java-is-a-relationship.png)


## **Interfaces**

*Blueprint of a class. It has static constants and abstract methods.*

*The interface in Java is a mechanism to achieve abstraction. There can be only abstract methods in the Java interface, not method body. It is used to achieve abstraction and multiple inheritance in Java.*

*In other words, you can say that interfaces can have abstract methods and variables. It cannot have a method body.*

**Example**
```
interface printable{  
void print();  
}  
class A6 implements printable{  
public void print(){System.out.println("Hello");}  
  
public static void main(String args[]){  
A6 obj = new A6();  
obj.print();  
 }  
}  
```
![Interfaces](https://static.javatpoint.com/images/core/interfacerelation.jpg)



[HOME](https://malkhaleel88.github.io/reading-notes)
