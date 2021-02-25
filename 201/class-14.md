# **Class 14 Reading Notes**

#### What Google Learned From Its Quest to Build the Perfect Team [The New York Times Magazine Article](https://www.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.html?auth=link-dismiss-google1tap)
*In summary, this article was in large about how to successfully work in teams*

#### CSS Transforms [Article](https://learn.shayhowe.com/advanced-html-css/css-transforms/)
- Transform Syntax
  * The actual syntax for the transform property is quite simple, including the transform property followed by the value
  * The value specifies the transform type followed by a specific amount inside parentheses
- 2D Transforms
  * Two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes
  * Three-dimensional transforms work on both the x and y axes, as well as the z axis
- 2D Rotate
  * The rotate value provides the ability to rotate an element from 0 to 360 degrees
- 2D Scale
  * Using the scale value within the transform property allows you to change the appeared size of an element
- 2D Translate
  * Using the translateX value will change the position of an element on the horizontal axis while using the translateY value will change the position of an element on the vertical axis
- 2D Skew
  * Skew is used to distort elements on the horizontal axis, vertical axis, or both
- Combining Transforms
  * It is common for multiple transforms to be used at once, rotating and scaling the size of an element at the same time for example
  * In this event multiple transforms can be combined together
- Transform Origin
  * The default transform origin is the dead center of an element, both 50% horizontally and 50% vertically
- Perspective
  * In order for three-dimensional transforms to work the elements need a perspective from which to transform
  * The perspective of an element can be set in two different ways, one way includes using the perspective value within the transform property on individual elements, while the other includes using the perspective property on the parent element residing over child elements being transformed
- Perspective Depth Value
- Perspective Origin
- 3D Transforms
  * Using three-dimensional transforms we can change elements on the z axis, giving us control of depth as well as length and width
- 3D Rotate
  * With three-dimensional transforms we can rotate an element around any axes; to do so, we use three new transform values, including rotateX, rotateY, and rotateZ
- 3D Scale
  * By using the scaleZ three-dimensional transform elements may be scaled on the z axis
- 3D Translate
- 3D Skew
  * Skew is the one two-dimensional transform that **cannot** be transformed on a three-dimensional scale
  * Elements may be skewed on the x and y axis, then transformed three-dimensionally as wished, but they cannot be skewed on the z axis
 Transform Style
- Backface Visibility

#### Transitions & Animations [Article](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)
- Transitions
  * For a transition to take place, an element must have a change in state, and different styles must be identified for each state
- Transitional Property
  * The transition-property property determines exactly what properties will be altered in conjunction with the other transitional properties
- Shorthand Transitions
  * Using the transition value alone, you can set every transition value in the order of transition-property, transition-duration, transition-timing-function, and lastly transition-delay
  * **Do not use commas with these values** *unless* you are identifying numerous transitions
- Animations
- Customizing Animations
  * Animations provide the ability to further customize an element’s behavior, including the ability to declare the number of times an animation runs, as well as the direction in which an animation completes

#### 8 Simple CSS3 Transitions That Will WOW Your Users [Article](https://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)
*All of these effects - bar one - are controlled with the transition property so we can see these effects working, we’ll set up a div in an HTML page*
1. Fade In
`.fade`
`{`
`        opacity:0.5;`
`}`
`.fade:hover`
`{`
`        opacity:1;`
`}`
2. Change Color
`.color:hover`
`{`
`        background:#53a7ea;`
`}`
3. Grow & Shrink
`.grow:hover
`{`
`        -webkit-transform: scale(1.3);`
`        -ms-transform: scale(1.3);`
`        transform: scale(1.3);`
`}`
4. Rotate elements
`.rotate:hover
`{`
`        -webkit-transform: rotateZ(-30deg);`
`        -ms-transform: rotateZ(-30deg);`
`        transform: rotateZ(-30deg);`
`}`
5. Square to circle
`.circle:hover`
`{`
`        border-radius:50%;`
`}`
6. 3D shadow
`.threed:hover
`{`
`        box-shadow:`
`                1px 1px #53a7ea,`
`                2px 2px #53a7ea,`
`                3px 3px #53a7ea;`
`        -webkit-transform: translateX(-3px);`
`        transform: translateX(-3px);`
`}`
7. Swing *Reference article for code, too long to write in here*
8. Inset border
`.border:hover`
`{`
`        box-shadow: inset 0 0 0 25px #53a7ea;`
`}`

#### 6 Buttons Animated [CodePen](https://codepen.io/retyui/pen/ByoaXV)

#### CSS3 KeyFrames Animation [CodePen](https://codepen.io/akshaychauhan/pen/oAfae)

#### 404 [CodePen](https://codepen.io/kieranfivestars/pen/MYdQxX)

#### Pure CSS Bounce Animation [CodePen](https://codepen.io/dp_lewis/pen/gCfBv)