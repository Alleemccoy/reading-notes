# Reading: Class 09

### [Concepts of Functional Programming in Javascript](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)
- What is Functional Programming?
  * Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data
- Pure Functions
  * The first fundamental concept we learn when we want to understand functional programming is **pure functions**
  * How do we know if a function is *pure* or not?
    * It returns the same result if given the same arguments - it is also referred as *deterministic*
    * It does not cause any observable side effects
  * It returns the same result if given the same arguments
  * Reading Files
  * Random number generation
  * It does not cause any observable side effects
  * Pure functions benefits
- Immutability
  *Unchanging over time or unable to be changed.*
  * When data is immutable, **its state cannot change after it’s created**
  * If you want to change an immutable object, you can’t - instead, **you create a new object with the new value**
  * In Javascript we commonly use the `for` loop
- Referential Transparency
- Functions as First-class Entities
  * The idea of functions as first-class entities is that functions are **also** treated as values **and** used as data
  * Functions as first-class entities can:
    * refer to it from constants and variables
    * pass it as a parameter to other functions
    * return it as result from other functions
  * The idea is to treat functions as values and pass functions like data, this way we can combine different functions to create new functions with new behavior
- Higher-order Functions
  * When we talk about higher-order functions, we mean a function that either:
    * takes one or more functions as arguments, or
    * returns a function as its result
  * The *doubleOperator* function we implemented above is a higher-order function because it takes an operator function as an argument and uses it
- Filter
  * Given a collection, we want to filter by an attribute
  * The filter function expects a *true or false* value to determine if the element **should or should not** be included in the result collection
  * Basically, if the callback expression is *true*, the filter function will include the element in the result collection - otherwise, it will not
  * A simple example is when we have a collection of integers and we want only the even numbers
  * Imperative approach
    * An imperative way to do it with Javascript is to:
      * create an empty array `evenNumbers`
      * iterate over the `numbers` array
      * push the even numbers to the `evenNumbers` array
  * Declarative approach
    * But we want a more declarative way to solve this problem, and using the `filter` higher order function as well
- Map
  * The `map` method transforms a collection by applying a function to all of its elements and building a new collection from the returned values
- Reduce
  * The idea of reduce is to receive a function and a collection, and return a value created by combining the items

### [Refactoring JavaScript for Performance and Readability](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec)
*It is best to click the link to read notes about this article as it shows many examples and different scenarios*