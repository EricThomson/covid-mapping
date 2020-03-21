# Covid mapping
A jupyter notebook used for mapping the coronavirus outbreak using pandas and plotly.

![bubble map](images/bubble_map.png)

There are already great visualization tools online: this is mainly to hook into the raw online data in case anyone is curious about how to work the knobs, and maybe  do some modeling.

The Johns Hopkins University Center for Systems Science and Engineering  generously makes their data available, and they have made the best visualization tool out there, at:
https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6

## To do before serving
- Get all examples to web site
- Use papermill to update.
- Write good documentation on Jupyter (with suggestions for tacks to take) so developers can go to town.

# Suggestions for analysis
- Plot curves for all states instead of entire country.
- Normalize to population density instead of showing raw number (e.g., comparing california to rhode island is ridiculous).
- Fit exponential to data. Early part of curves see how much it depends on state's population density.
- Extract deaths/recovered data in addition.
- Come up with way to determine if a curve has hit the bend (i.e., has an exponential started to drop to linear yet).

## On plotly
Plotly is great, but front end web stuff is traumatic.  Some resources I found helpful for getting this served:
- https://stackoverflow.com/questions/47529290/python-plotly-offline-chart-embed-into-html-not-working/47593250
- https://towardsdatascience.com/how-to-create-a-plotly-visualization-and-embed-it-on-websites-517c1a78568b
- https://plot.ly/chart-studio-help/embed-graphs-in-websites/

Basically, create a plotly html file for a single plot, or an embed file and then use an `iframe` to embed it into a web site.

## On papermill
Eventually I want this to automatically update, and can use papermill:
https://towardsdatascience.com/introduction-to-papermill-2c61f66bea30

## Useful plotly docs
- https://plot.ly/python/time-series/#time-series-plot-with-datetime-objects

## Acknowledgments
Thanks to Julia (https://github.com/juliakm) for lots of suggestions, like for using iframes and papermill.
