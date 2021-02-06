# **Class 9 Reading Notes**

## *HTML & CSS*

### Chapter 15 Overview: FORMS
- Why Forms?
  * The best known form on the web is probably the box that sits right in the middle of Google's homepage
- Form Controls
  * There are several types of form controls that you can use to collect information from visitors to your site
    * Adding text
    * Making choices
    * Submitting forms
- How Forms Work
  * A user fills in a form and then presses a button to submit the information to the server
  * A form may have several form controls, each gathering different information
  * The server needs to know which piece of inputted data corresponds with which form element
- Form Structure
  * Action
  * Method
  * ID
- Text Input
  * type="text"
  * name
  * size
  * maxlength
- Password Input
  * type="password"
  * name
  * size, maxlength
- Text Area
  * `<textarea>`
- Radio Button
  * type="radio"
  * name
  * value
  * checked
- Checkbox
  * type="checkbox"
  * name
  * value
  * checked
- Drop Down List Box
  * `<select>`
  * name
  * `<option>`
  * value
  * Selected
- Multiple Select Box
  * `<select>`
  * size
  * multiple
- File Input Box
  * `<input>`
  * type="file"
- Submit Button
  * `<input>`
  * type="submit"
  * name
  * value
- Image Button
  * `<input>`
  * type="image"
- Button & Hidden Controls
  * `<button>`
  * `<input>`
  * type="hidden"
- Labelling Form Controls
  * `<label>`
  * for
- Grouping Form Elements
  * `<fieldset>`
  * `<legend>`
- HTML5 Sections
- SUMMARY: FORMS
  * Whenever you want to collect information from visitors you will need a form, which lives inside a `<form>` element
  * Information from a form is sent in name/value pairs
  * Each form control is given a name, and the text the user types in or the values of the options they select are sent to the server
  * HTML5 introduces new form elements which make it easier for visitors to fill in forms

### Chapter 14 Overview: LISTS, TABLES AND FORMS
- Bullet Point Styles
- Images for Bullets
- Positioning The Marker
- List Shorthand
- Table Properties
- Border On Empty Cells
- Gaps Between Cells
- Styling Forms
- Styling Text Inputs
- Styling Submit Buttons
- Styling Fieldsets & Legends
- Aligning Form Controls: Problem
- Aligning Form Controls: Solution
- Cursor Styles
- Web Developer Toolbar
- SUMMARY: LISTS, TABLES AND FORMS
  * In addition to the CSS properties covered in other chapters which work with the contents of all elements, there are several others that are specifically used to control the appearance of lists, tables and forms
  * List markers can be given different appearances using the *list-style-type* and *list-style* image properties
  * Table cells can have different borders and spacing in different browsers, but there are properties you can use to control them and make them more consistent
  * Forms are easier to use if the form controls are vertically aligned using CSS
  * Forms benefit from styles that make them feel more interactive

  ## *JavaScript & jQuery*

### Chapter 6 Overview: EVENTS
- Different Event Types
- How Events Trigger JavaScript Code
  * When the user interacts with the HTML on a web page, there are three steps involved in getting it to trigger some JavaScript code
  * Together these steps are known as **event handling**
    1. Select the **element** node or nodes you want the script to respond to
    2. Indicate which **event** on the selected node or nodes will trigger the response
    3. State the **code** you want to run when the event occurs
- Three Ways to Bind an Event to an Element
  * Event handlers let you indicate which event you are waiting for on any particular element
    1. HTML Event Handlers ! *this is bad practice, but you needs to be aware of it because you may see it in older code* !
    2. Traditional DOM Event Handlers
    3. DOM Level 2 Event Listeners
- Event Flow
  * HTML elements nest inside other elements
  * If you hover or click on a link, you will also ne hovering or clicking on its parent elements
- Why Flow Matters
  * The flow of events only really matters when your code has event handlers on an element and one its ancestors or descendant elements
- The Event Object
  * When an event occurs, the *event* object tells you information about the event and the element it happened upon
- The Event Object in IE5-8
- Using Event Listeners with the Event Object
- Event Delegation
  * Creating event listeners for a lot of elements can slow down a page, but event flow allows you to listen for an event on a parent element
- Changing Default Behavior
  * The **event** object has methods that change: the default behavior of an element and how the element's ancestors respond to the event
- Using Event Delegation
- Which Element Did an Event Occur on?
  * When calling a function, the *event* object's target property is the best way to determine which element the event occurred on
- Different Types of Events
  * User Interface Events
  * Load
  * Focus & Blur Events
  * Focus & Blur
  * Mouse Events
  * Click
- Where Events Occur
  * The **event** object can tell you where the cursor was positioned when an event was triggered
  * Determining Position
  * Keyboard Events
  * Which Key Was Pressed
  * Forms Events
  * Using Form Events
  * Mutation Events & Observers
  * Using Mutation EventsHTML5 Events
  * Using HTML5 Events
- SUMMARY: EVENTS
  * Events are the browsers way of indicating when something has happened
  * Binding is the process of stating which event you are waiting to happen, and which element you are waiting for that event to happen upon
  * When an event occurs on an element you trigger a JavaScript function, when this function then changes the web page in some way it feels interactive because is has responded to the user
  * You can use event delegation to monitor for events that happen on all of the children of an element