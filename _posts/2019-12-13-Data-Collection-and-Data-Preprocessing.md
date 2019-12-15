---
title: "Data Collection and Data Preprocessing"
date: 2019-12-13
published: true
tags: 
- Data Collection
- Altair
- hvplot
- Spatial Join
excerpt: "Collecting the Data by API and have a breif look at the median hosue price in Philadelphia from 2013 to 2015."
hv-loader:
  hv-chart-1: "Tractmedianprice.html"
toc: true
toc_sticky: true
---

## Data Collection

We collect:
- Philadelphia house sales data from [OpenDataPhilly](https://cityofphiladelphia.carto.com/u/phl/me), we use the data from 2013 to 2018.
- Collecting The Census Data by URL.
- Collecting The Neighborhoof data by URL.

## Data Preprocessing

- First, we do the geospatial join to join the sales point data with census tract polygons data.
- We make a brief bar chart to check the median sales price in Philadelphia by years.
![MediansalesPrice](https://github.com/zhaoanyang36/final/blob/master/assets/images/MediansalesPrice.png)
It is interesting that the 2013 have a higher median house price than 2018. We believe there are some error in it. For example, small samples and uneven distribution lead to this problem. From 2014 to 2018, overall house prices showed an upward trend, which was standing with our expectations.
- We use the hvplot to plot a map show the median sale price by census tract with widget.
<div id="hv-chart-1"></div>
From this time change to the map, it can be seen that there is a higher distribution of house prices in northwest and southeast Philadelphia.







