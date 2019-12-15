---
title: "Data Analysis and Visualization"
date: 2019-12-12
published: true
tags: 
- Data Collection
- Altair
- hvplot
excerpt: "The sales data was combined with the neighborhoods tracts and it calculate the price increase percentage."
altair-loader:
  altair-chart-1: "charts/top20.json"
  altair-chart-2: "charts/scatterplot.json"
hv-loader:
  hv-chart-1: "2018increaserate.html"
toc: true
toc_sticky: true
---

## Data Analysis
- We use the sales data spatial join with the neighborhood tract.
- We calculate the price increase and the price increase rate from 2013 to 2018 for each census tract.


## Data Visualization

### 1. There is the top 20 highest median house price neighborhood.

<div id="altair-chart-1"></div> 

### 2. We visualize a interactive chart for median sale price and price increase groupby year and show the information of neighborhood.

<div id="altair-chart-2"></div> 

### 3. There is the median house price increase from 2013 to 2018.

<div id="hv-chart-1"></div> 

