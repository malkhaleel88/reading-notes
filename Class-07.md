# **HTML Tables; JS Constructor Functions**

## **HTML Tables**

*HTML tables allow web developers to arrange data into rows and columns.*

*The `<table>` tag defines an HTML table.*

*Each table row is defined with a `<tr>` tag. Each table header is defined with a `<th>` tag. Each table data/cell is defined with a `<td>` tag.*

*By default, the text in `<th>` elements are bold and centered.*

*By default, the text in `<td>` elements are regular and left-aligned.*

*For long tables you can split the table into a `<thead>`,
`<tbody>`, and `<tfoot>`.*

## **JS Constructor Functions**

*Sometimes we need a "blueprint" for creating many objects of the same "type".*

*The way to create an "object type", is to use an object constructor function.*

*The value of this, when used in an object, is the object itself.*

*In a constructor function this does not have a value. It is a substitute for the new object. The value of this will become the new object when a new object is created.*

Example :
```
function Person(first, last, age, eye) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eye;
}
```

### **Built-In Objects**

*Built-in objects are not related to any Window or DOM object model.*
*These objects are used for simple data processing in the JavaScript.*

![Built-In](https://i.imgur.com/J3ETg5D.png)


[HOME](https://malkhaleel88.github.io/reading-notes)