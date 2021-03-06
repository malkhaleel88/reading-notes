# **Passing Functions as Props**

## **React Docs - lists and keys**

 ### **What does .map() return?**

 *Return a new array of the same length as the original array comprised of your return values.*

 ### **If I want to loop through an array and display each value in JSX, how do I do that in React?**

 *Using **.map()***.

 ### **Each list item needs a unique**"KEY"**.

 ### **What is the purpose of a key?**

 *Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity.*


## **The Spread Operator**

 ### **What is the spread operator?**

 *The spread operator is a useful and quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a functionβs arguments.*

 ### **List 4 things that the spread operator can do.**

 * Copying an array.

 * Concatenating or combining arrays.

 * Using Math functions.

 * Using an array as arguments.

 * Adding an item to a list.

 * Adding to state in React.

 * Combining objects.

 * Converting NodeList to an array.


 ### **Give an example of using the spread operator to combine two arrays.**
 
 ```
 const fruits = ['π','π','π','π','π']
 const moreFruits = [...fruits];
 console.log(moreFruits) // Array(5) [ "π", "π", "π", "π", "π" ]
 fruits[0] = 'π'
 console.log(...[...fruits,'...',...moreFruits]) //  π π π π π ... π π π π π
```

 ### **Give an example of using the spread operator to add a new item to an array.**

 ```
 const fewFruit = ['π','π','π']
 const fewMoreFruit = ['π', 'π', ...fewFruit]
 console.log(fewMoreFruit) //  Array(5) [ "π", "π", "π", "π", "π" ]
 ```
 
 ### **Give an example of using the spread operator to combine two objects into one.**

 ```
 const objectOne = {hello: "π€ͺ"}
 const objectTwo = {world: "π»"}
 const objectThree = {...objectOne, ...objectTwo, laugh: "π"}
 console.log(objectThree) // Object { hello: "π€ͺ", world: "π»", laugh: "π" }
 const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("π".repeat(5))}}
 objectFour.laugh() // πππππ
 ```


## **How to Pass Functions Between Components**

 ### **In the video, what is the first step that the developer does to pass functions between components?**

 *Create function Wherever the state is that we are going to change.* 

 ### **In your own words, what does the increment function do?**
 
 *Looping through people array and finding the matching object on it then increasing number of clicks.*


 ### **How can you pass a method from a parent component into a child component?**

 *We can pass method using "this.method" in child component inside render function in parent component.*

 ### **How does the child component invoke a method that was passed to it from a parent component?**
 
 *We can pass method using "this.props.method" wherever inside child component "calling function".*



## **Things I want to know more about**



[HOME](https://malkhaleel88.github.io/reading-notes)