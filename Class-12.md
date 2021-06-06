# **Docs for the HTML `<canvas>` Element & Chart.js**

## **HTML `<canvas>` Element**

*The HTML `<canvas>` element is used to draw graphics, on the fly, via JavaScript.*
*The `<canvas>` element is only a container for graphics. You must use JavaScript to actually draw the graphics.*
*Canvas has several methods for drawing paths, boxes, circles, text, and adding images.*

**Example**

*HTML*

```
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #d3d3d3;">
Your browser does not support the HTML canvas tag.
</canvas>
```

*JavaScript*

```
<script>
var c = document.getElementById("myCanvas");
var ctx = c.getContext("2d");
ctx.moveTo(0,0);
ctx.lineTo(200,100);
ctx.stroke();
</script>
```

## **Chart.js**

![Chart.js](https://www.bypeople.com/wp-content/uploads/2020/02/javascript-chart-js.png)

*JavaScript library using for both Artificial Intelligence graphs and other charts.*

**Chart.js** *comes with the following built-in chart types:*

* Scatter
* Line
* Bar
* Radar
* Pie and Doughnut
* Polar Area
* Bubble



[HOME](https://malkhaleel88.github.io/reading-notes)
