# **Maps, primitives, File I/O**


## **Primitives vs. Objects**

### **Java Type System**

*Java has a two-fold type system consisting of primitives such as int, boolean and reference types such as Integer, Boolean. Every primitive type corresponds to a reference type.*
*Every object contains a single value of the corresponding primitive type. The wrapper classes are immutable (so that their state can't change once the object is constructed) and are final (so that we can't inherit from them).*
*Under the hood, Java performs a conversion between the primitive and reference types if an actual type is different from the declared one:*
```
Integer j = 1;          // autoboxing
int i = new Integer(1); // unboxing
```
*The process of converting a primitive type to a reference one is called autoboxing, the opposite process is called unboxing.*

## **Exceptions in Java**

*The Java programming language uses exceptions to handle errors and other exceptional events. This lesson describes when and how to use exceptions.*

### **Kinds of Exceptions**

* Checked Exception.
* Error.
* Runtime Exception.


## **Scanning**

*Objects of type Scanner are useful for breaking down formatted input into tokens and translating individual tokens according to their data type.*

```
import java.io.*;
import java.util.Scanner;

public class ScanXan {
    public static void main(String[] args) throws IOException {

        Scanner s = null;

        try {
            s = new Scanner(new BufferedReader(new FileReader("xanadu.txt")));

            while (s.hasNext()) {
                System.out.println(s.next());
            }
        } finally {
            if (s != null) {
                s.close();
            }
        }
    }
}
```

[HOME](https://malkhaleel88.github.io/reading-notes)