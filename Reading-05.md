# **Putting it all together**

## **React Docs - thinking in React**

 ### **How would you break a mock into a component heirarchy?**
 
 *The first thing you’ll want to do is to draw boxes around every component (and subcomponent) in the mock and give them all names.*
  
 ### **What is the single responsibility principle and how does it apply to components?**
 
 *The Single Responsibility Principle (SRP) means that code with the same functionality should not exist in multiple places. Component Composition makes SRP easier to maintain so that there can be a single source of truth.*

 ### **What does it mean to build a ‘static’ version of your application?**
 
 * Building components that reuse other components and pass data using props.*

 ### **Once you have a static application, what do you need to add?**
 
 *Data.*

 ### **What are the three questions you can ask to  determine if something is state?**

 * *Is it passed in from a parent via props? If so, it probably isn’t state.*

 * *Does it remain unchanged over time? If so, it probably isn’t state.*

 * *Can you compute it based on any other state or props in your component? If so, it isn’t state.*

 ### **How can you identify where state needs to live?**
 
 * *Identify every component that renders something based on that state.*

 * *Find a common owner component (a single component above all the components that need the state in the hierarchy).*

 * *Either the common owner or another component higher up in the hierarchy should own the state.*

 * *If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.*



 ## **Things I want to know more about**



[HOME](https://malkhaleel88.github.io/reading-notes)