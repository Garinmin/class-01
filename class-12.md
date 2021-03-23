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
