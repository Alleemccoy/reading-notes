# Reading: Class 10

### [The JavaScript Call Stack](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)
The JavaScript engine (which is found in a hosting environment like the browser), is a single-threaded interpreter comprising of a heap and a single call stack
The browser provides web APIs like the DOM, AJAX, and Timers

*This article is aimed at explaining what the call stack is and why it is needed*
- The call stack is primarily used for function invocation - *call*
- Since the call stack is single, functions execution, is done, one at a time, from top to bottom - it means the call stack is synchronous
- The understanding of the call stack is vital to Asynchronous programming
- In Asynchronous JavaScript, we have a callback function, an event loop, and a task queue
- The callback function is acted upon by the call stack during execution after the call back function has been pushed to the stack by the event loop

**What is the call stack?**
- At the most basic level, a call stack is a data structure that uses the *Last In, First Out* principle to temporarily store and manage function invocation - *call*
- **LIFO:** When we say that the call stack, operates by the data structure principle of *Last In, First Out*, it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns
- **Temporarily store:** When a function is invoked or *called*, the function, its parameters, and variables are pushed into the call stack to form a stack frame
- This stack frame is a memory location in the stack, the memory is cleared when the function returns as it is pop out of the stack
- **Manage function invocation - *call*:** The call stack maintains a record of the position of each stack frame, it knows the next function to be executed and will remove it after execution - this is what makes code execution in JavaScript synchronous
  * Think of yourself standing on a queue, in a grocery store cash point, you can only be attended to after the person in front of you have been attended to - that’s synchronous
  * This is what we mean by “manage function invocation”
- How does the call stack handle function calls?
  * *example code - click link to review example*
- What causes a stack overflow?
  * A stack overflow occurs when there is a recursive function - *a function that calls itself*, without an exit point
  * The browser oe *hosting environment*, has a maximum stack call that it can accomodate before throwing a stack error
    * *example code - click link to review example*
- In summary
  * The key takeaways from the call stack are:
    1. It is single-threaded. Meaning it can only do one thing at a time
    2. Code execution is synchronous
    3. A function invocation creates a stack frame that occupies a temporary memory
    4. It works as a LIFO — Last In, First Out data structure

### [JavaScript Error Messages && Debugging](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)
- Types of error messages
The first thing that indicates you that something is wrong with your code is the infamous error message that the one we saw just moments ago, it usually appears on your console - being developer tools of the browser, terminal or whatever else you are using
  * Reference errors
    * This is as simple as when you try to use a variable that is not yet declared you get this type os errors
    `console.log(foo) // Uncaught ReferenceError: foo is not defined`
    * This is also a common thing when using const and let, they are hoisted like var and function but there is a time between the hoisting and being declared so when you try to access them a reference error occurs, the fact that this happens to let and const is called Temporal Dead Zone
    `foo = 'Hello' // Uncaught ReferenceError: foo is not defined let foo`
    * Whatever you are using *var, let or const* the fix is as simple has declaring the variable before any declaration is made
    `let = foo;`
    `foo = 'Hello'`
  * Syntax errors
    * I know it’s in the name of the errors, but like it says itself, this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse
    `JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1`
    * This can be solved by just fixing the syntax, in this case the object should be a JSON
    `JSON.parse('{"foo":"bar"}')`
    * Some syntax errors like sending a trailing comma when calling a function are handled without error by most recent browsers, but older ones you have to be careful
  * Range errors
    * Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up
    `var foo= []`
    `foo.length = foo.length -1 // Uncaught RangeError: Invalid array length`
    * An array for instance cannot have a negative length, why would you mess with the array length? Some people use it to set an array to empty, something of the likes of:
    `var foo = [0, 0]`
    `foo.length = foo.length - 2 // (or foo.length - foo.length)`
    `foo // would log [] instead of [0, 0]`
  * Type errors
    * Like the name indicates, this types of errors show up when the types *number, string and so on* you are trying to use or access are incompatible, like accessing a property in an undefined type of variable
    `var foo = {}`
    `foo.bar // undefined`
    `foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined`
    * This is probably the most frequent error in JS, trying to access a property/method thinking that bar is of the type *object* when in reality, since it hasn’t been declared yet, it’s undefined which doesn’t have any baz available
    * The fix is simple, just make sure that bar exists before trying to access it, either by creating bar or by checking for *undefined*
- Debugging
  * To debug your JS code, the easiest and maybe the most common way its to simply `console.log()` the variables you want to check or, by using chrome developer tools, open your page with your JS code `press cmd+o in macOS or Ctrl+o in Windows` and choose your file to debug, click the line you wanna debug and refresh your page again - F5
  * If the line you selected was run you will be able to see what has happened before that point and you can try and evaluate the next lines to check if everything is outputting what you are expecting
  * The breakpoint can also be achieved by putting a debugger statement in your code in the line you want to break
  * You can also add conditional breakpoints by right-clicking a previous set breakpoint, which will make your program stop at that point only if a condition is met, this is awesome for when you want to debug huge cycles for specific values, in this example the breakpoint will point stop when the index reaches 40
- Call stack
  * The red part of our first example represents the call stack, which is the path that your program has taken to reach the point were you set a breaking point or were you have an error
- Handling errors
  * About the light blue part of our earliest example of an error message, that shows up like that when we do not handle errors properly, meaning that anything after that error will not be executed
  * To avoid this we usually try to **catch** the errors so we can gracefully fallback to a default state of our application in case of an error *this fallback can be a 404 page which is normally not that graceful but is better than a page to just stop working*
- Tools to avoid runtime errors
  * JS is not a compiled language like Java so your errors will happen at runtime, that means that you can only see whatever is wrong with your code after your run it

  ### [Additional Resources](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)
