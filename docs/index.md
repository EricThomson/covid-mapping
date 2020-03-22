---
title: COVID-19 Maps
---
# Mapping Coronavirus
This is a testing site for visualizing Coronavirus data. Three plots (for now) are below, and at the end I describe the workflow for developers who want to work with this dataset but are not sure where to start.

The Johns Hopkins University Center for Systems Science and Engineering  generously make their data available, and they have great visualization  tool at: https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6

## Cases in the US versus Date
Note there is a dropdown menu in the graph lets you switch beteween logarithmic and linear scale for the y-axis.

<iframe src="cases_v_time.html"  width="900" height="500" frameborder="0" scrolling="no"></iframe>


## Heat-map

<iframe src="choropleth.html"  width="900" height="550" frameborder="0" scrolling="no"></iframe>

The colors are drawn after a logarithmic transform.

## Bubble map

<iframe src="bubble.html"  width="900" height="550"  frameborder="0" scrolling="no"></iframe>

## Workflow for developers
For those interested in working with this data, you can find the Jupyter notebook I used to generate the above plots here:
https://github.com/EricThomson/covid-mapping/blob/master/covid_map.ipynb

 The notebook includes how to download the data, which is conveniently available online as csv files, and updated nightly. Within the notebook, we render the interactive graphs using plotly (https://plot.ly/), save them as html files, and then embed them in this web page using frames.

One wrinkle: the Jupyter notebook needs to be run each night to refresh the plots: to do this we are using papermill. Basically, first make sure your jupyter notebook runs from end-to-end (Run all cells). 
