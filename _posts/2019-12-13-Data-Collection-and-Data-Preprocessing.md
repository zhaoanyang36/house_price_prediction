---
title: "Data Collection and Data Preprocessing"
date: 2019-12-13
published: true
tags: 
- Data Collection
- Altair
- hvplot
- Spatial Join
excerpt: "Collecting the Data by API and have a breif look at the median hosue price in Philadelphia from 2013 to 2015z"
hv-loader:
  hv-chart-1: "charts/hvplot_host_year.html"
toc: true
toc_sticky: true
---

## Data Collection

We collect 3 kind of data from url
- Philadelphia house sales data from [OpenDataPhilly](https://cityofphiladelphia.carto.com/u/phl/me), we use the data from 2013 to 2018.
- Collecting The Census Data by URL.
- Collecting The Neighborhoof data by URL.

## Data Preprocessing

- First, we do the geospatial join to join the sales data in point with census tract polygons.
- We make a brief bar chart to check the median sales price in Philadelphia by years.
![MediansalesPrice](https://raw.githubusercontent.com/zhaoanyang36/final/assets/images/MediansalesPrice.png)
- We use the hvplot to plot a map show the median sale price by census teact with widget.
<div id="hv-chart-2"></div> 






