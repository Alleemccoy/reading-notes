# ES6 Classes - Prep Work

### [Shred Talk](https://www.youtube.com/watch?v=9Yc5J3Ap9-4)
- Data Modeling
- Constructor Function and Prototypes
- ES6 Classes

* Person
  * Attributes: hair color, height, weight, location
  * Behaviors: (verbs) walk(), speak(), drive()

*Here is SOME example code*
*The full demo code can be found[here](https://codefellows.github.io/code-301-guide-react/curriculum/prework/classes/DEMO.html)

`const Animal = function(name, legs) {`
  `this.name = name;`
  `this.legs = legs;`
  `this.eat = function() {`
    `this.isEating = true;`
  `}`
`}`
`Animal.prototype.walk = function() {`
  `this.isWalking = true;`
`}`

`let puppy = new Animal('blake', 4);`
`puppy.walk();`
`puppy.eat();`
`console.log(puppy);`

### The [Assignment](https://codefellows.github.io/code-301-guide-react/curriculum/prework/classes/LAB.html) was completed in Repl