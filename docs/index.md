---
title: COVID-19 Maps
---
# Mapping Coronavirus
The three interactive plots shown below were all generated using the associated github repo [https://github.com/EricThomson/covid-mapping](https://github.com/EricThomson/covid-mapping). At the end I describe the workflow for developers who want to work with this dataset but are not sure where to start.

The data, updated nightly, are from the generous folks at [https://covidtracking.com/]( https://covidtracking.com/).

### Cases in the US versus Date
The dropdown menu in the graph lets you switch between logarithmic and linear scale for the y-axis.

<iframe src="cases_v_time.html"  width="900" height="500" frameborder="0" scrolling="no"></iframe>


### Heat-map

<iframe src="choropleth.html"  width="900" height="550" frameborder="0" scrolling="no"></iframe>

The colors are drawn after a logarithmic transform.

### Bubble map

<iframe src="bubble.html"  width="900" height="550"  frameborder="0" scrolling="no"></iframe>

This one is pretty hard to scale correctly: it might be good to switch to a logarithmic scale so that New York isn't so huge compared to the others. Let's put that on the to-do list.

## Workflow
For Python peeps, you can find the Jupyter notebook I used to generate the above plots here:    

[https://github.com/EricThomson/covid-mapping/blob/master/covid_map.ipynb](https://github.com/EricThomson/covid-mapping/blob/master/covid_map.ipynb)

 The notebook includes how to download the data, which is conveniently available online as csv files and updated nightly. Within the notebook, we render the interactive graphs using plotly ([https://plot.ly/](https://plot.ly/)), save them as html files, and then embed them in this web page using frames.

 This web site is hosted by GitHub. Basically, make a `docs` folder in your repo, throw your html files and `index.md` in there (and pick this option in settings, as well as a theme), and github will tell you the url to point people. Styles changes by adding stuff you will find in the `assets` folder. The web site was set up by repo contributor Julia [https://github.com/juliakm](https://github.com/juliakm). Thanks Julia!

One slightly annoying wrinkle: the Jupyter notebook needs to be run each night to pull the fresh data and update the plots. Currently I am doing it by hand: this could all be ported to a server using papermill and a scheduler (e.g., cron). For production-ready code we likely would just use a `py` file not a notebook.
