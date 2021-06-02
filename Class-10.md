# **JS Debugging**

*Programming code might contain syntax errors, or logical errors.*
*Many of these errors are difficult to diagnose.*
*Often, when programming code contains errors, nothing will happen.*
*There are no error messages, and you will get no indications where to search for errors.*
*Searching for (and fixing) errors in programming code is called code debugging.*

![Debugger](https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/08/JavaScript-Debugging-and-Testing-1200x720.png)

## **JavaScript Debuggers**

*Debugging is not easy. But fortunately, all modern browsers have a built-in JavaScript debugger.*
*Built-in debuggers can be turned on and off, forcing errors to be reported to the user.*
*With a debugger, you can also set breakpoints (places where code execution can be stopped),
and examine variables while the code is executing.*

## **The `Console.log()` Method**

*If your browser supports debugging, you can use `console.log()` to display JavaScript values in the debugger window.*

*Example :*
```
<script>
a = 5;
b = 6;
c = a + b;
console.log(c);
</script>
```

## **Setting Breakpoints**

*In the debugger window, you can set breakpoints in the JavaScript code.*
*At each breakpoint, JavaScript will stop executing, and let you examine JavaScript values.*
*After examining values, you can resume the
execution of code (typically with a play button).*

## **The debugger Keyword**

*The debugger keyword stops the execution of JavaScript, and calls (if available) the debugging function.*
*This has the same function as setting a breakpoint in the debugger.*
*If no debugging is available, the debugger statement has no effect.*

*Example :*
```
var x = 15 * 5;
debugger;
document.getElementById("demo").innerHTML = x;
```

## **Types Of Errors In JavaScript**

![Errors](https://www.tutsmake.com/wp-content/uploads/2020/05/Types-of-Errors-In-JavaScript.jpeg)


[HOME](https://malkhaleel88.github.io/reading-notes)