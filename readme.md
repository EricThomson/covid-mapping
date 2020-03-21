# Covid mapping
A jupyter notebook used for mapping the coronavirus outbreak using pandas and plotly.

![bubble map](images/bubble_map.png)

There are already great visualization tools online: this is mainly to hook into the raw online data in case anyone is curious about how to work the knobs, and maybe  do some modeling.

The Johns Hopkins University Center for Systems Science and Engineering  generously makes their data available, and they have made the best visualization tool out there, at:
https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6

## To do
- Convert scatter plots to plotly.
- Add dropdown so user can shift b/w linear/semilog plot:
https://stackoverflow.com/questions/54872300/how-to-enable-and-disable-the-logarithmic-scale-as-a-viewer-in-plotly
- Get simple example working of creating html/embed file created and shown on a minimal web site.
- Get ability host/show somewhere.
- Use papermill to update.
- Write good documentation on Jupyter (with suggestions for tacks to take) so developers can go to town.

## On plotly
Plotly is great, but front end web stuff is traumatic.  Some resources I found helpful for getting this served:
- https://stackoverflow.com/questions/47529290/python-plotly-offline-chart-embed-into-html-not-working/47593250
- https://towardsdatascience.com/how-to-create-a-plotly-visualization-and-embed-it-on-websites-517c1a78568b
- https://plot.ly/chart-studio-help/embed-graphs-in-websites/

Basically, create a plotly html file for a single plot, or an embed file and then use an `iframe` to embed it into a web site.

## On papermill
Eventually I want this to automatically update, and can use papermill:
https://towardsdatascience.com/introduction-to-papermill-2c61f66bea30

## Acknowledgments
Thanks to Julia (https://github.com/juliakm) for lots of suggestions, like for using iframes and papermill.
