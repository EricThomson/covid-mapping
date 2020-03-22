# Covid mapping
A jupyter notebook used for mapping the coronavirus outbreak using pandas and plotly.

![bubble map](images/bubble_map.png)

There are already great visualization tools online: this is meant to be a kind of starters kit for anyone that wants to do the same, or do some modelling. If you want to explore the interactive maps and don't care about how they are made, you can find them at the associated site:
https://ericthomson.github.io/covid-mapping/

The Johns Hopkins University Center for Systems Science and Engineering  generously makes their data available, and they have made the best visualization tool out there, at:
https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6

# Future possibilities
- Plot curves for all states instead of aggregate over entire country.
- Normalize to population density instead of showing raw number (e.g., comparing california to rhode island is ridiculous).
- Fit exponential to data (and see how much it depends on state's population density).
- Extract deaths/recovered data in addition to number of diagnoses.
- Come up with way to determine if a curve has hit the bend (i.e., has an exponential started to drop to linear yet?).

## Acknowledgments
Thanks to repo contributer Julia (https://github.com/juliakm) for building the jekyll site and helping to troubleshoot everything.
