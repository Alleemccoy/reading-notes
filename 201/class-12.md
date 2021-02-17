# **Class 12 Reading Notes**

### Easily Create Stunning Animated Charts with [CHART.JS](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)
*A great way to get started with charts is with Chart.js, a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page*

- Setting Up
  1. The first thing we need to do is download Chart.js
  2. Copy the Chart.min.js out of the unzipped folder and into the directory you’ll be working in
  3. Then create a new html page and import the script

- Drawing a Line Chart
  1. To draw a line chart, the first thing we need to do is create a canvas element in our HTML in which Chart.js can draw our chart
  2. Next, we need to write a script that will retrieve the context of the canvas
  3. Inside the same script tags we need to create our data, in this instance it’s an object that contains labels for the base of our chart and datasets to describe the values on the chart

- Drawing a Pie Chart
  1. Our line chart is complete, so let’s move on to our pie chart. First, we need the canvas element
  2. Next, we need to get the context and to instantiate the chart
  3. Next we need to create the data. This data is a little different to the line chart because the pie chart is simpler, we just need to supply a value and a color for each section
  4. Now, immediately after the pieData we’ll add our options

- Drawing a Bar Chart
  1. Finally, let’s add  a bar chart to our page. Happily the syntax for the bar chart is very similar to the line chart we’ve already added. First, we add the canvas element
  2. Next, we retrieve the element and create the graph
  3. And finally, we add in the bar chart’s data

- **Conclusion** - *Here in the article you can find the full script coded out*

### [Chart.js docs](https://www.chartjs.org/docs/latest/)

### [Basic Usage](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage)

### [Drawing Shapes with Canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)

### [Applying Styles and Colors](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)

### [Drawing Text](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)