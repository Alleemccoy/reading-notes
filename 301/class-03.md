# Reading: Class 03

### [Lifting State Up](https://reactjs.org/docs/lifting-state-up.html)
- Often, several components need to reflect the same changing data
- Adding a Second Input
- Writing Conversion Functions
- Lifting State Up
- Lessons Learned

### [Lists and Keys](https://reactjs.org/docs/lists-and-keys.html)
- Rendering Multiple Components
- Basic List Component
- Keys
- Extracting Components with Keys
- Keys Must Only Be Unique Among Siblings
- Embedding map() in JSX

### [Tutorial: Declaring a Winner](https://reactjs.org/tutorial/tutorial.html)
- We are building a Tick-Tac-Toe game
  * You can follow along in **Starter Code** or in a *Local Development Environment*
- Declaring a Winner
  * Now that we show which player’s turn is next, we should also show when the game is won and there are no more turns to make
  * Given an array of 9 squares, this function will check for a winner and return 'X', 'O', or null as appropriate
  * We will call calculateWinner(squares) in the Board’s render function to check if a player has won
  * If a player has won, we can display text such as “Winner: X” or “Winner: O”

### [The Spread Operator](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)
- How to use the Spread Operator (...) in JavaScript
  * The spread operator is a useful and quick syntax for adding items to arrays, combining arrays or objects and spreading an array into a function's arguments
- What is the spread operator?
  * In JavaScript, spread syntax refers to the use of an ellipsis of three dots (...) to expand an iterable object into tje list of arguments
  * "What **...arr** is used in the function call, it *expands* an iterable object **arr** into the list of arguments" - JavaScript.info
  - What is ... used for?
    * "It looks similar to the rest parameters, also using **...**, but does quite the opposite" - JavaScript.info
  - What else can ... do?
    * The **...** spread operator is useful for many different routine tasks in JavaScript, including the following:
      * Copying an array
      * Concatenating or combining arrays
      * Using Math functions
      * Using an array as arguments
      * Adding an item to a list
      * Adding to state in React
      * Combining objects
      * Converting NodeList to an array
    * In each case, the spread syntax expands an iterable object, usually an array, though it can be used on any interable, including a string
- Examples of using ...
- Copying an array
  * Using the **...** spread operator is a convenient way to copy an array or combine arrays, and it can even add new items
- Concatenating arrays
  * The spread operator can quickly combine two arrays, an operation known as **array concatenation**
- Using Math functions
  * "The Math object's set of functions are a perfect example of the spread operator as the only argument to a function" - David Walsh
  * One of the best ways to understand the use of spread operator in JavaScript is to look at the the built-in functions Math.min() and Math.max(), which both expect a list of arguments, not an array
- Using an array as arguments
  * Since the spread operator “spreads” an array into different arguments, any functions that accepts multiple any number of arguments can benefit from use of the spread operator
- Adding an item to a list
  * The spread operator can add an item to an another array with a natural, easy-to-understand syntax
- Adding to state in React
  * Adding an item to an array in React state is easily accomplished using the spread operator
- Combining objects
  * The spread syntax is useful for combining the properties and methods on objects into a new object
- Converting NodeList to Array
  * The spread operator can convert *NodeList* and *arguments* objects to arrays, such as when selecting HTML elements on the page
- The spread operator and older browsers
  * When programming to support Internet Explorer and browsers on older mobile devices, the spread operator is not going to work
- A note about copying by reference
  * One of the benefits of using the spread operator is that it will create a new reference to its primitive values, copying them
  * That means that changes to the original array will not affect the copied array, which is what would happen if the array had been linked to the original with the assignment operator **=**
- Watch out for the deeply-nested Gotcha!
  * On the other hand, when JavaScript objects including arrays are deeply nested, the spread operator only copies the first level with a new reference, but the deeper values are still linked together
  * This type of problem is called creating a deep copy, as opposed to a shallow copy
  * Deep copies can be made using lodash or the R.clone() method from the Ramda functional programming library
- Conclusion
  * "The spread operator can expand another item by split an iterable element like a string or an array into individual elements:" - CodinGame.com
  * The spread operator … is useful for working with arrays and objects in JavaScript. It is a convenient feature added in ES6 (ES2015)