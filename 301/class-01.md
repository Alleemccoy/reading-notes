# Reading Notes: 1

### [Tutorial: Intro to React](https://reactjs.org/tutorial/tutorial.html)
- We are building a Tick-Tac-Toe game
  * You can follow along in **Starter Code** or in a *Local Development Environment*
- What is React?
  * React is a declarative, efficient, and flexible JavaScript library for building user interfaces
  * It lets you compose complex UIs from small and isolated pieces of code called “components”

### [Hello World](https://reactjs.org/docs/hello-world.html)
- The smallest React example looks like this - *which displays a heading saying "Hello World!"*:
`ReactDOM.render(`
  `<h1>Hello World!</h1>,`
  `document.getElementById('root')`
`);`

### [Introducing JSX](https://reactjs.org/docs/introducing-jsx.html)
- This tag syntax is neither a string or HTML, it is called JSX and it is a syntax extension to JavaScript:
  `const element = <h1>Hello World!</h1>;`
- Why JSX?
  * React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display
  * React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code
- Embedding Expressions in JSX
- JSX is an Expression Too
- Specifying Attributes with JSX
- Specifying Children with JSX
- JSX Prevents Injection Attacks
- JSX Represents Objects

### [Rendering Elements](https://reactjs.org/docs/rendering-elements.html)
- An element describes what you want to ee on the screen:
  `const element - <h1>Hello World!</h1>;`
  * Unlike browser DOM elements, React elements are plain objects, and are cheap to create
  * React DOM takes care of updating the DOM to match the React elements
- Rendering an Element into the DOM
- Updating rhe Rendered Element
- React Only Updates What's Necessary

### [Components and Props](https://reactjs.org/docs/components-and-props.html)
- Components let you split the UI into independent, reusable pieces, and think about each piece in isolation
- Conceptually, components are like JavaScript functions, they accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen
- Function and Class Components
- Rendering a Component
- Composing Components
- Extracting Components
- Props are Read-Only