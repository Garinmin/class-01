# Chart.js, Canvas

## Chart.js

_Chart.js_ is a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page, that makes using all kinds of bar charts, line charts, pie charts and more, incredibly easy.

### Setting up Chart.js

The first thing we need to do is download Chart.js to folder.
Next, import the script in HTML page:
```
   <head>
      <script src='Chart.min.js'></script>
   </head>
```
### Drawing a line chart

```
   <canvas id="buyers" width="600" height="400"></canvas>                  // create the canvas element
```

```
   <script>
    var buyers = document.getElementById('buyers').getContext('2d');        // retrieve the context of the canvas
    new Chart(buyers).Line(buyerData);
    
    var buyerData = {
	  labels : ["January","February","March","April","May","June"],
	  datasets : [
		{
			fillColor : "rgba(172,194,132,0.4)",                // create our data 
			strokeColor : "#ACC26D",
			pointColor : "#fff",                          
			pointStrokeColor : "#9DB86D",
			data : [203,156,99,251,305,247]
		}
	  ]
    }   
   </script>
```

### Drawing a pie chart

```
   <canvas id="countries" width="600" height="400"></canvas>.                // create the canvas element
   
   var countries= document.getElementById("countries").getContext("2d");     // instantiate the chart
   new Chart(countries).Pie(pieData, pieOptions);
   
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
		color : "#FF8153"              // create the data
	},
	{
		value : 30,
		color : "#FFEA88"
	}
  ];
  
  var pieOptions = {
	segmentShowStroke : false,     // remove the stroke from the segments
	animateScale : true            // animate the scale of the pie so that it zooms out from nothing
  }
```

### 

```
   <canvas id="income" width="600" height="400"></canvas>            // create the canvas element
   
   var income = document.getElementById("income").getContext("2d");  // retrieve the element and create the graph
   new Chart(income).Bar(barData);   
   
   var barData = {
	labels : ["January","February","March","April","May","June"],
	datasets : [
		{
			fillColor : "#48A497",
			strokeColor : "#48A4D1",
			data : [456,479,324,569,702,600]
		},
		{                                                    // add in the bar chart’s data 
			fillColor : "rgba(73,188,170,0.4)",
			strokeColor : "rgba(72,174,209,0.4)",
			data : [364,504,605,400,345,320]
		}
	 ]
   }
```
   
## The _canvas_ element

The **canvas** element has only two attributes: ```width``` and ```height```
(When no ```width``` and ```height``` attributes are specified, the canvas will initially be 300 pixels wide and 150 pixels high).
Unlike the ```<img>``` element, the ```<canvas>``` element requires the closing tag ```</canvas>```
The canvas is initially blank. To display something, a script first needs to access the rendering context and draw on it
```
   var canvas = document.getElementById('tutorial');     // retrieves the node in the DOM by calling the document.getElementById() method
   var ctx = canvas.getContext('2d');                    // call getContext() method ("2d" to get a CanvasRenderingContext2D)
```

### Drawing rectangles

```<canvas>``` only supports two primitive shapes: rectangles and paths
There are three functions that draw rectangles on the canvas:
```fillRect(x, y, width, height)``` Draws a filled rectangle.
```strokeRect(x, y, width, height)``` Draws a rectangular outline.
```clearRect(x, y, width, height)``` Clears the specified rectangular area, making it fully transparent.
Each of these three functions takes the same parameters. ```x``` and ```y``` specify the position on the canvas (relative to the origin) of the top-left corner of the rectangle. ```width``` and ```height``` provide the rectangle's size.
Example:
```function draw() {
  var canvas = document.getElementById('canvas');
  if (canvas.getContext) {
    var ctx = canvas.getContext('2d');

    ctx.fillRect(25, 25, 100, 100);
    ctx.clearRect(45, 45, 60, 60);
    ctx.strokeRect(50, 50, 50, 50);
  }
  }
```
### Drawing paths

1. Create the path.
2. Use drawing commands to draw into the path.
3. You can stroke or fill the path to render it.

Here are the functions used to perform these steps:
```beginPath()``` Creates a new path.
``Path methods`` Methods to set different paths for objects.
```closePath()``` Adds a straight line to the path, going to the start of the current sub-path.
```stroke()``` Draws the shape by stroking its outline.
```fill()``` Draws a solid shape by filling the path's content area.

```moveTo(x, y)``` Moves the pen to the coordinates specified by x and y
```arc(x, y, radius, startAngle, endAngle, anticlockwise)``` Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending 
                                                             at endAngle going in the given direction indicated by anticlockwise (defaulting to clockwise)
```arcTo(x1, y1, x2, y2, radius)``` Draws an arc with the given control points and radius, connected to the previous point by a straight line.
