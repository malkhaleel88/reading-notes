# **In memory storage**

## **Understanding the JavaScript Call Stack**


 ### **What is a ‘call’?**

 *Predefined JavaScript method, It can be used to invoke (call) a method with an owner object as an argument (parameter).*

 ### **How many ‘calls’ can happen at once?**

 *one at a time, from top to bottom. It means the call stack is synchronous.*

 ### **What does LIFO mean?**

 *Last In, First Out.*

 ### **Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.** 

 ```
 function firstFunction(){
   throw new Error('Stack Trace Error');
 }

 function secondFunction(){
   firstFunction();
 }

 function thirdFunction(){
   secondFunction();
 }

 thirdFunction();
```

 ### **What causes a Stack Overflow?**

 *A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.*


## **JavaScript error messages**


 ### **What is a ‘refrence error’?**

 *This is as simple as when you try to use a variable that is not yet declared you get this type os errors.*

 ### **What is a ‘syntax error’?**

 *This occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.*

 ### **What is a ‘range error’?**

 *Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.*

 ### **What is a ‘type error’?**

 *This types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.*

 ### **What is a breakpoint?**

 *A way which will make your program stop at that point only if a condition is met, this is awesome for when you want to debug huge cycles for specific values*

 ### **What does the word ‘debugger’ do in your code?**

 *Putting a debugger statement in your code in the line you want to break.*



 ## **Things I want to know more about**



[HOME](https://malkhaleel88.github.io/reading-notes)
