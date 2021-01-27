# **Class 6 Reading Notes**

## *JavaScript & jQuery*

### Chapter 3 Overview: FUNCTIONS, METHODS & OBJECTS *pages 100 to 105*
- What is an Object?
  * Objects group together a set of variables and functions to create a model of something you would recognize from the real world. In an object, variables and functions take on the new names.
  * IN AN OBJECT: Variables become known as properties
    * If a variable is part of an object, it is called a **property**; properties tell us about the object.
  * IN AN OBJECT: Functions become known as methods
    * If a function is part of an object, it is called a **method**. Methods represent tasks that are associated with the object.
  * Like variables and named functions, properties have a name and a value. In an object, that name is called a **key**.
  * Properties:

  | KEY       | VALUE     |
  |:--------: | :--------:|
  | name      | string    |
  | rooms     | number    |
  | booked    | number    |
  | gym       | Boolean   |
  | roomTypes | array     |

- Creating an Object: Literal Notation
  * Literal notation is the easiest and most popular way to create objects
- Accessing an Object and Dot Notation
  * You access the properties or methods od an object using dot notation
  * You can also access properties using `[]`
- Creating Objects Using Literal Notation
- Creating More Object Literals


### Chapter 5 Overview: DOCUMENT OBJECT MODEL
- The Dom Tree is a Model of a Web Page
  * As a browser loads a web page, or created a model of that page
  * The model is called a DOM tree, and it is stored in the browser memory
- Working with the DOM Tree
  1. Step One: Access the elements
  2. Step Two: Work with those elements
- Caching DOM Queries
- Accessing Elements
- Methods that Select Individual Elements
- Selecting an Element from a Nodelist
  * There are two ways to select an elements from a Nodelist
    1. The item `()` method
    2. Array syntax
- Repeating Actions for an Entire Nodelist
  * When you have a Nodelist, you can loop through each node in the collection and apply the same statements to each
- Adding or Removing HTML Content
  * There are two very different approaches to adding and removing content from a DOM tree: the innerHTML property and DOM manipulation
- Attribute Nodes