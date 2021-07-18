# **JS Object Literals; The DOM**

## **JS Objects Literals**

*A JavaScript object literal is a comma-separated list of name-value pairs wrapped in curly braces. Object literals encapsulate data, enclosing it in a tidy package. This minimizes the use of global variables which can cause problems when combining code.*

Example :
```
var myObject = {
  prop1: 'hello',
  prop2: 'world',
  output: function() {
    console.log(this.prop1 + ' ' + this.prop2);
  }
};

myObject.output(); // hello world
```

## **The DOM**

*The HTML DOM is a standard object model and programming interface for HTML. It defines:*

* The HTML elements as objects.
* The properties of all HTML elements.
* The methods to access all HTML elements.
* The events for all HTML elements.

*When a web page is loaded, the browser creates a Document Object Model of the page.*

*The HTML DOM model is constructed as a tree of Objects.*

![DOM](https://techinsight.com.vn/wp-content/uploads/2020/08/1-2.png)


[HOME](https://malkhaleel88.github.io/reading-notes)
