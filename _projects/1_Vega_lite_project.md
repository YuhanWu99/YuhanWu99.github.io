---
name: HW_8
tools: [Python, HTML, vega-lite]
image: assets/pngs/humidity.png
description: This is my homework 8 for IS 445!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Interactive Dashboard

Yoho! You can use the "brush" to select certain area in the right plot and see how the left histgram change with your choice :)

<vegachart schema-url="{{ site.baseurl }}/assets/json/dashboard.json" style="width: 100%"></vegachart>


## Write Up (first plot):
The first plot is about the count of different humidity level per state. 
For choice of encoding types used: On the x-axis, binned humidity level is showing for each state. For example, in Washington, the count of humidity level between 0.70 to 0.80 is about 100 (really dark blue), and its count of humidity level between 0.20 to 0.30 is about 10 or 5 (really light green). On the y-axis is all the states listed.
For color, I use the aggregate data of count of humidity to show different level of count, darker means more count. 
For transformations done, I use binned data of humidity to plot so that we can select different rectangular and make them interactive with second plot.
This plot is pretty much the same as in HW 7 but I also add a brush to select encodings 'x' and 'y'.

## Write Up (second plot):
The second plot is a histogram with humidity score on the x-axis and count of records on the y-axis.
For choice of encoding types used: On the x-axis, humidity score is showing for each state when selected. On y-axis, count of records is shown.
For color, I chose dark blue to be corresponding with the style in first plot.
For transformations done, I also bin the data to make a plot of histgram.
This plot is pretty much the same as in HW 7 except now it's interactive and changes with your selection.

## Write Up (interactivity):
Before interaction, the histgram is only showing the count of records of different humidity level for the entire dataset, and we are unable to see what's happening for each state. Now, by choosing any retangular in the first plot, we can see the histgram for each state individually. This allow the visualization to demonstrate the humidity level in more detail.


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/YuhanWu99/YuhanWu99.github.io/tree/main/_data/bfro_reports_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/YuhanWu99/YuhanWu99.github.io/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>

