# **Class 7 Reading Notes**

## *Domain Modeling*
[Article](https://github.com/codefellows/domain_modeling#domain-modeling)
- Domain modeling is the process of creating a conceptual model in code for a specific problem
- A model describes the various entities, their attributes and behaviors as well as the constraints that govern the problem domain
- An entity that stores data in properties and encapsulates behaviors in methods in commonly referred to as an **object-oriented** model


## *HTML & CSS*

### Chapter 6 Overview: TABLES
- Whats a Table?
  * A table represents information in a grid format
- Basic Table Structure
  * `<table>`
  * `<tr>`
  * `<td>`
- Table Headings
  * `<th>`
- Spanning Columns
- Spanning Rows
- Long Tables
  * `<thead>`
  * `<tbody>`
  * `<tfoot>`


  ## *JavaScript & jQuery*
  
  ### Chapter 3 Overview: FUNCTIONS, METHODS & OBJECTS *pages 106 to 144*
  - Creating an Object: Constructor Notation
    * The **new** keyword and the object constructor create a blank object
    * You can add properties and methods to the object
    * First, you create a new object using a combo of the **new** keyword and the Object`()` constructor function
    * Next, having created the blank object, you can add properties and methods to it using dot notation
    * Each statement that adds a property or method should end with a semicolon
    * To create an empty object using literal notation use example: var hotel = `{}`
  - Updating an Object
    * To update the value of properties, use dot notation or square brackets
    * They work on objects created using literal or constructor notation
    * *To delete a property, use the **delete** keyword*
  - Creating Many Objects: Constructor Notation
    * Sometimes you will want several objects to represent similar things
    * Object constructors can use a function as a **template** for creating objects
    * First, create the template with the objects properties and methods
  - Properties vs. Methods
  - Key vs. Value
  - You create **instances** of the object using the constructor function
  - The **new** keyword followed by a call to the function creates a new object
  - The properties of each object are given as arguments to the function
  - THIS `(It is a Keyword)`
    * The keyword **t-h-i-s** is commonly used inside functions and objects
    * Where the function is declared alters what **t-h-i-s**  means
    * It always refers to one object, usually the object in which the function operates
  - Arrays are Objects
    * Arrays are actually a special type of object, they hold a related set of key/value pairs `(like all objects)` but the key for each value is its index number
  - Arrays of Objects & Objects in Arrays
    * You can combine arrays and objects to create complex data structures:
      1. Arrays can store a series of objects
      2. Objects can also hold arrays
  - Three Groups of Built-in Objects
  - Creating an Instance of the Date Object
    * In order to work with dates, you create an instance of th **Date** object
    * You can specify the time and date the you want it to represent