# **Class 10 Reading Notes**

## *JavaScript & jQuery*

### Chapter 10 Overview: ERROR HANDLING & DEBUGGING
- Order of Execution
  * To find the source of an error, it helps to know how scripts are processed
  * The order in which statements are executed can be complex; some tasks cannot complete until another statement or function has been run
- Execution Contexts
  * The JavaScript interpreter uses the concept of **execution contexts**
  * There is one global execution context; plus, each function creates a new new execution context - they correspond to variable scope
- The Stack
  * The JavaScript interpreter processes one line of code at a time
  * When a statement needs data from another function, it **stacks**, *or piles* the new function on top of the current task
- SUMMARY: ERROR HANDLING & DEBUGGING
  * Debugging is the process of finding errors, it involves a process of deduction
  * The console helps narrow down the area in which the error is located, so you can try to find the exact error
  * JavaScript has 7 different types of errors, each created its own error object which can tell you its line number and gives a description error
  * If you know that you may get an error, you can handle it gracefully using *try, catch, finally* statements; use them to give your users helpful feedback