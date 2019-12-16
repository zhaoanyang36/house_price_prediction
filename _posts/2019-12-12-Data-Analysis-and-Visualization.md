---
title: "Data Analysis and Visualization"
date: 2019-12-12
published: true
tags: 
- Data Collection
- Altair
- hvplot
excerpt: "The sales data was combined with the neighborhoods tracts and it calculate the price increase Rate."
altair-loader:
  altair-chart-1: "charts/top20.json"
  altair-chart-2: "charts/scatterplot.json"
hv-loader:
  hv-chart-1: "charts/2018increaserate1.html"
toc: true
toc_sticky: true
---

## Data Analysis
- We use the sales data spatial join with the neighborhood tract.
- We calculate the price increase and the price increase rate from 2013 to 2018 for each census tract.


## Data Visualization

**First**, We select the top 20 highest median house price neighborhood.

<div id="altair-chart-1"></div> 

We can use the widget to find which the neighborhood and the value of the median house price. The top 3 of the highest price area is The Filter Square, The Woodland Terrace and Rittenhouse. From the location study, we can know that these three areas are characterized by beautiful surroundings or environments and luxury apartments or villas.

**Second**, We visualize a interactive chart for median sale price and price increase groupby year and show the information of neighborhood.

<div id="altair-chart-2"></div> 

We use the median sales price and increase price as the x and y for coordinate systems. Using the widget can show the average value of median sales price of selected point grouped by years. We also can use the tooltips to look for the detail information of the data point.

**Third**, We visualize the median house price increase rate from 2013 to 2018 here. This interactive map shows where housing prices are growing signifcant. We also desire to use this map as a comparable with the predicted house price increase map in the following part.

<div id="hv-chart-1"></div> 

It can be seen that house prices in the city center and the southeast have grown very rapidly in the past five years. This indicates that the market here may have more potential。

