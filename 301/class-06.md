# Reading: Class 06
#### NODE.JS

### [NODE.JS Intro on sitepoint.com](https://www.sitepoint.com/an-introduction-to-node-js/)
- What is Node.js?
  * Node.js is a JavaScript runtime built on Chrome’s V8 JavaScript engine
  * Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library
  * Node Is Built on Google Chrome’s V8 JavaScript Engine
  * The V8 engine is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers, including Brave, Opera, and Vivaldi
  * It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute
- How do I install Node.js?
  * Many websites will recommend that you head to the official Node download page and grab the Node binaries for your system
- "Hello, World" the Node.js way...
  * You can check that Node is installed on your system by opening a terminal and typing **node -v**
  * If all has gone well, you should see something like *v12.14.1* displayed, this is the current LTS version at the time of writing
  * Next, create a new file **hello.js** and copy of in the following code:
    * `console.log("Hello, World!");`
    * This uses Node’s *built-in console module* to display a message in a terminal window. To run the example, enter the following command: **node hello.js**
    * If Node.js is configured properly, “Hello, World!” will be displayed
- Node.js Has Excellent Support for Modern JavaScript
  * Node has excellent support for ECMAScript 2015 (ES6) and beyond
  * As you’re only targeting one runtime *a specific version of the V8 engine*, this means that you can write your JavaScript using the latest and most modern syntax, it also means that you don’t generally have to worry about compatibility issues — as you would if you were writing JavaScript that would run in different browsers
- Introducing npm, the JavaScript Package Manager
  * Node comes bundled with a package manager called npm, to check which version you have installed on your system, type **npm -v**
  * In addition to being the package manager for JavaScript, npm is also the world’s largest software registry
  * There are over 1,000,000 packages of JavaScript code available to download, with billions of downloads per week
- Installing a Package Globally
  1. **npm install -g jshint**
    * This will install the jshint package globally on your system, we can use it to lint the *index.js* file from the previous example: **jshint index.js**
    * You should now see a number of ES6-related errors
    * If you want to fix them up, add /* jshint esversion: 6 */ to the top of the index.js file, re-run the command and linting should pass
- Installing a Package Locally
  * Create a *test* folder and open a terminal in that directory, next type this: **npm init -y**
  * This will create and auto-populate a *package.json* file in the same folder
  * Next, use npm to install the lodash package and save it as a project dependency: **npm install lodash --save**
  * Create a file named test.js - *visit link for code to type in*
  * Finally, run the script using node test.js, you should see **[ 1, 2, 3 ]** output to the terminal
- Working with the package.json file
  * If you look at the contents of the test directory, you’ll notice a folder entitled *node_modules*
  * This is where npm has saved lodash and any libraries that lodash depends on
  * The *node_modules* folder shouldn’t be checked in to version control, and can, in fact, be re-created at any time by running *npm install* from within the project’s root
  * If you open the *package.json* file, you’ll see lodash listed under the *dependencies* field
  * By specifying your project’s dependencies in this way, you allow any developer anywhere to clone your project and use npm to install whatever packages it needs to run
- What is Node.js used for?
  * Common uses: installing (via npm) and running (via Node) various build tools — designed to automate the process of developing a modern JavaScript application
  * These build tools come in all shapes and sizes, and you won’t get far in a modern JavaScript landscape without bumping into them
  * They can be used for anything from bundling your JavaScript files and dependencies into static assets, to running tests, or automatic code linting and style checking
- Node.js lets us run JavaScript on the server
- What kind of apps is Node.js suited to?
  * Node is particularly suited to building applications that require some form of real-time interaction or collaboration — for example, chat sites, or apps such as CodeShare, where you can watch a document being edited live by someone else
  * It’s also a good fit for building APIs where you’re handling lots of requests that are I/O driven (such as those needing to perform operations on a database), or for sites involving data streaming, as Node makes it possible to process files while they’re still being uploaded
- What are the advantages of Node.js?
  * Aside from speed and scalability, an often-touted advantage of using JavaScript on a web server — as well as in the browser — is that your brain no longer needs to switch modes
  * You can do everything in the same language, which, as a developer, makes you more productive (and hopefully, happier), for example, you can easily share code between the server and the client
  * Another of Node’s big pluses is that it speaks JSON
  * Finally, JavaScript is ubiquitous: most of us are familiar with JavaScript, or have used it at some point, this means that transitioning to Node development is potentially easier than to other server-side languages
- Other Uses of Node
- Conclusion
  * JavaScript is everywhere, and Node is a vast and expansive subject
  * Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library

### [6 Reasons for Pair Programming](https://canvas.instructure.com/courses/2608709/discussion_topics/10837440)
- How does pair programming work?
  * Greater efficiency
  * Engaged collaboration
  * Learning from fellow students
  * Social skills
  * Job interview readiness
  * Work environment readiness

[Geocoding API Docs](https://locationiq.com/) - *Bookmarked*
[Axios docs](https://www.npmjs.com/package/axios) - *Bookmarked*
[MDN async and await](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Async_await) - *Bookmarked*