# **Class 8 Reading Notes**

## *HTML & CSS*

### Chapter 15 Overview: LAYOUT
- Key Concepts in Positioning Elements
  * Building Blocks
    * CSS treats each HTML element as if it is in its own box
    * This box will either be a **block-level** box or an **inline** box
  * Containing Element
    * If one block-level element sits inside another block-level element then the outer box is known as the containing pr **parent** element
- Controlling the Position of Elements
  * CSS has the following **positioning schemes** that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning
  * You specify the positioning scheme using the *position* property in CSS
  * You can also float elements using the *float* property
  To indicate where a box should be positioned, you may also need to use **box offset** properties to tell the browser how far from the top or bottom and left to right it should be placed
  * Normal Flow
  * Relative Positioning
  * Absolute Positioning
  * Fixed Positioning
  * Floating Elements
- When you move any element from normal flow, boxes can overlap, the **z-index** property allows you to control which box appears on top
- Screen Sizes
  * Different visitors to you site will have different sized screens that show different amounts of information, so your design needs to be able to work on a range of different sized screens
- Screen Resolution
  * Resolution refers to the number of dots a screen shows per inch
  * Some devices have a higher resolution than desktop computers and most operating systems allow users to adjust the resolution of their screens
- Page Sizes
  * Because screen sizes and display resolutions vary so much, web designers often try to create pages of around 960-1000 pixels wide
- Fixed Width Layouts
  * Fixed width layout designs do not change size as the user increases or decreases the size od their browser window
  * Measurements tend to be given in pixels
- Liquid Layouts
  * Liquid layouts designs stretch and contract as the user increases or decreases the size of their browser window
  * They tend to use percentages
  