---
name: Illinois Building Visualizations
tools: [Python, Altair, Vega-lite]
description: Exploring building counts and construction years across Illinois agencies.
permalink: /projects/building-visualizations/
---
# Illinois  Building Visualizations
## Buildings by Agency
<div id="chart1"></div>

The first chart depicts the building count for each Illinois agency. Nominal agency names are on the y-axis while quantitative building counts are on the x-axis. Horizontal bars have been used to enhance readability, and agencies are ordered from highest to lowest count to make comparisons easier. The default blue is used for the bars because color does not denote any other variable; thus, a separate color palette is not needed. Altair groups records by agency and then counts the records per group through the count() function. No other data transformations have been done for this chart.
## Construction Years by Agency
<div id="chart2"></div>

The next plot illustrates the construction years of buildings for a selected agency. Quantitative construction years are located on the x-axis and grouped into bins with maxbins = 30. Quantitative building counts for each year bin are located on the y-axis. I have chosen a histogram since it helps identify periods with more building construction. I left the default blue color to focus on the distribution rather than color categories. The chart filters out observations with construction years equal to or less than zero, filters observations by the selected agency, and counts records for each year bin.

The agency dropdown box enables viewing one agency at a time. The University of Illinois is chosen by default. Upon selecting an agency in the dropdown menu, its histogram of construction years will be displayed. This interaction makes the visualization easier to explore since it allows viewers to examine each agency’s construction patterns separately. Axes might be rescaled upon changing selections.
## Data and Anaylsis
[The Data](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv)

[The Analysis](https://github.com/parkshinhyeong-crypto/parkshinhyeong-crypto.github.io/blob/main/python_notebooks/building_visualizations.ipynb)

<script src="https://cdn.jsdelivr.net/npm/vega@6"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@6"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@7"></script>

<script>
vegaEmbed('#chart1', '{{ "/assets/chart1.json" | relative_url }}');
vegaEmbed('#chart2', '{{ "/assets/chart2.json" | relative_url }}');
</script>
