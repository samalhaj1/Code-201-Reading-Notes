# EASILY CREATE STUNNING ANIMATED CHARTS WITH CHART.JS
![img](http://codinghelptech.com/blog_post/Easily-create-stunning-animated-charts-with-Chart-js.jpg)

Charts.js is a library for JavaScript which uses HTML5â€™s canvas to render various different beautiful charts for the web. You can download it from:http://www.chartjs.org and start using it immediately. All you have to do is add the Chart.js script to your document and you can take advantage of its functionality, documented at http://www.chartjs.org/docs/.

In our case, we would not be downloading Chart.js as we will use a CDN. We load it by adding a script tag to our DOM:

Thereafter, we create a helper function which we will use to create charts faster and not repeat ourselves.

The function takes as arguments the id of the canvas where our chart will appear, the chart type (Charts.js supports many chart types such as bars, pies, and line charts) and the data and options objects for the particular chart. We use the chartType argument to call the appropriate method given to us by instantiating a new chart and pass it the data and the options. For example, if we want a pie the **chart type** has to be Pie because we create a new pie by calling the **Pie** function on the return value from new **Chart(ctx)**.

Then, in our **chartHelper** object we define another helper method called **addCommas**. This method will be used to prettify the numbers in the labels of one of the charts as those numbers will have a lot of digits in them.

## Creating a custom Bar chart
We define our options object which will prettify any big numbers and instruct Chart.js to display the labels of the Bar chart in the tooltip along with the numeric value of the field.

**Afterwards**, we create the data for the first Bar chart. We add two labels for the data and create two datasets. In the first dataset, we create a label property which will be displayed in the tooltip in response to the code in our options object.Â  We proceed to define the fillColor property which defines the color inside the chartâ€™s fields, the stroke color which would be the corners of the chartâ€™s fields, the **highlight color** which would be the color of the inside of the chartâ€™s fields when a user hovers over the field and the highlight stroke which would represent the corners of the chartâ€™s fields. The values of these properties that relate to colors can take a **hexadecimal color** value, an rgb or **rgba** value or a color string.

**Finally**, we define the data for the two labels, the first representing the Retirement Age and the second the Average Life Expectancy. Then, we create another object within the datasets array which will have the same properties but will possess a label of Women and different data numbers.

<img class="aligncenter size-full wp-image-3039" src="http://i2.wp.com/images.phpgang.com/2016/01/bar.png?resize=362%2C419" alt="bar" srcset="http://i2.wp.com/images.phpgang.com/2016/01/bar.png?w=362 362w, http://i2.wp.com/images viagra naturel pas cher.phpgang.com/2016/01/bar.png?resize=130%2C150 130w, http://i2.wp.com/images.phpgang.com/2016/01/bar.png?resize=259%2C300 259w” sizes=”(max-width: 362px) 100vw, 362px” data-recalc-dims=”1″ />

Now, all we have to do is call our helper and the Bar will appear:

When done, the Bar chart would look something like the above picture. When you hover upon a set of Bar fields such as Average Life Expectancy or Retirement Age you would see the nice labels.

## Drawing a pie chart
                                                                                                                                              
 First, we need the canvas element:
                                                                                                                                              
 < canvas id="countries" width="600" height="400"></canvas >
                                                 
Next, we need to get the context and to instantiate the chart:

var countries= document.getElementById("countries").getContext("2d");
new Chart(countries).Pie(pieData, pieOptions);
                                                                   
Next we need to create the data. This data is a little different to the line chart because the pie chart is simpler, we just need to supply a value and a color for each section:

var pieData = [
                                                                   
	{
                                                                   
		value: 20,
                                                                   
		color:"#878BB6"
                   
	},
                   
	{
		value : 40,
                   
		color : "#4ACAB4"
	},
                     
	{
                     
		value : 10,
                     
		color : "#FF8153"
                     
	},
                     
	{
                     
		value : 30,
                     
		color : "#FFEA88"
                     
	}];
                     

Now, immediately after the pieData we’ll add our options:

var pieOptions = {
                     
	segmentShowStroke : false,
                     
	animateScale : true
} 
                     
## Basic usage of canvas 
                     
#### Fallback content
                     
The <canvas> element differs from an <img> tag in that, like for <video>, <audio>, or <picture> elements, it is easy to define some fallback content, to be displayed in older browsers not supporting it, like versions of Internet Explorer earlier than version 9 or textual browsers. You should always provide fallback content to be displayed by those browsers.

Providing fallback content is very straightforward: just insert the alternate content inside the <canvas> element. Browsers that don't support <canvas> will ignore the container and render the fallback content inside it. Browsers that do support <canvas> will ignore the content inside the container, and just render the canvas normally                    

#### Required </canvas> tag
As a consequence of the way fallback is provided, unlike the <img> element, the <canvas> element requires the closing tag (</canvas>). If this tag is not present, the rest of the document would be considered the fallback content and wouldn't be displayed.

If fallback content is not needed, a simple <canvas id="foo" ...></canvas> is fully compatible with all browsers that support canvas at all.

#### The rendering context
The <canvas> element creates a fixed-size drawing surface that exposes one or more rendering contexts, which are used to create and manipulate the content shown. In this tutorial, we focus on the 2D rendering context. Other contexts may provide different types of rendering; for example, WebGL uses a 3D context based on OpenGL ES.

The canvas is initially blank. To display something, a script first needs to access the rendering context and draw on it. The <canvas> element has a method called getContext(), used to obtain the rendering context and its drawing functions. getContext() takes one parameter, the type of context. For 2D graphics, such as those covered by this tutorial, you specify "2d" to get a CanvasRenderingContext2D.

var canvas = document.getElementById('tutorial');

var ctx = canvas.getContext('2d');

## Drawing shapes with canvas

**Rectangular shape example**

function draw() {

  var canvas = document.getElementById('canvas');
  
  if (canvas.getContext) {
  
    var ctx = canvas.getContext('2d');
    

    ctx.fillRect(25, 25, 100, 100);
    
    ctx.clearRect(45, 45, 60, 60);
    
    ctx.strokeRect(50, 50, 50, 50);
    
  }}
  
  **Drawing a triangle**
  
For example, the code for drawing a triangle would look something like this:

function draw() {

  var canvas = document.getElementById('canvas');
  
  if (canvas.getContext) {
  
    var ctx = canvas.getContext('2d');

    ctx.beginPath();
    
    ctx.moveTo(75, 50);
    
    ctx.lineTo(100, 75);
    
    ctx.lineTo(100, 25);
    
    ctx.fill();
  }}
  
  ### Applying styles and colors
  **Colors**
  
Up until now we have only seen methods of the drawing context. If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.

fillStyle = color

Sets the style used when filling shapes.

strokeStyle = color

Sets the style for shapes' outlines.

color is a string representing a CSS <color>, a gradient object, or a pattern object. We'll look at gradient and pattern objects later. By default, the stroke and fill color are set to black (CSS color value #000000)

### Drawing text
The canvas rendering context provides two methods to render text:

fillText(text, x, y [, maxWidth])

Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.

strokeText(text, x, y [, maxWidth])

Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

**A fillText example**

The text is filled using the current fillStyle.

function draw() {

  var ctx = document.getElementById('canvas').getContext('2d');
  
  ctx.font = '48px serif';
  
  ctx.fillText('Hello world', 10, 50);
  
}


















