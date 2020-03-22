---
title: COVID-19 Maps
---
# Mapping Coronavirus
This is a testing site for visualizing Coronavirus data. Three plots (for now) are below, and at the end I describe the workflow for developers who want to work with this dataset but are not sure where to start.

The Johns Hopkins University Center for Systems Science and Engineering  generously make their data available, and they have great visualization  tool at their web site:
[https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6](https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6)

### Cases in the US versus Date
The dropdown menu in the graph lets you switch between logarithmic and linear scale for the y-axis.

<iframe src="cases_v_time.html"  width="900" height="500" frameborder="0" scrolling="no"></iframe>


### Heat-map

<iframe src="choropleth.html"  width="900" height="550" frameborder="0" scrolling="no"></iframe>

The colors are drawn after a logarithmic transform.

### Bubble map

<iframe src="bubble.html"  width="900" height="550"  frameborder="0" scrolling="no"></iframe>

This one is pretty hard to scale correctly: it might be good to switch to a logarithmic scale so that New York isn't so huge compared to the others. Let's put that on the to-do list.

## Analysis workflow
For those interested in working with this data, you can find the Jupyter notebook I used to generate the above plots here:
[https://github.com/EricThomson/covid-mapping/blob/master/covid_map.ipynb](https://github.com/EricThomson/covid-mapping/blob/master/covid_map.ipynb)

 The notebook includes how to download the data, which is conveniently available online as csv files and updated nightly. Within the notebook, we render the interactive graphs using plotly ([https://plot.ly/](https://plot.ly/)), save them as html files, and then embed them in this web page using frames.

 This web site is hosted by GitHub. Basically, make a `docs` folder in your repo, throw your html files and `index.md` in there (and pick this option in settings, as well as a theme), and github will tell you were to point people. Most of this work was done by repo contributor Julia [https://github.com/juliakm](https://github.com/juliakm).

One wrinkle: the Jupyter notebook needs to be run each night to pull the fresh data and update the plots. Currently I am doing it by hand, but with more time this could be ported to a server using papermill (which lets you run Jupyter notebooks from the command line) and a scheduler (e.g., cron). Ultimately this stuff could all be done in `py` files rather than Jupyter notebooks.
