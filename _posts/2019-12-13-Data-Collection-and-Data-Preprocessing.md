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
  hv-chart-1: "charts/Tractmedianprice.html"
altair-loader:
  altair-chart-1: "charts/MedianPricebyyear1.json"
toc: true
toc_sticky: true
---

## Data Collection

We collect:
- Philadelphia house sales data from [OpenDataPhilly](https://cityofphiladelphia.carto.com/u/phl/me), we use the data from 2013 to 2018.
- Collecting The Census Data by URL.
- Collecting The Neighborhoof data by URL.

## Data Preprocessing

- We clean the data by selecting the range of the sale price. Outlier will influnence our data analysis.
```python
valid =  (test_sales_tract18['sale_price_K'] < 1000)
```
- First, we do the geospatial join to join the sales point data with census tract polygons data.
- We make a brief bar chart to check the median sales price in Philadelphia by years.
<div id="altair-chart-1"></div> 
It can be seen that overall house prices showed an upward trend, which was standing with our expectations. It can be inferred from the general trend that the housing market in Philadelphia is constantly developing. Using the tooltips, we can identify the median sales price of specific year. However, we want to the see the distribution of the price in spatial.
- We use the hvplot to plot a map show the median sale price by census tract with widget from 2013 to 2015.


<div id="hv-chart-1"></div>


From this time change to the map, it can be seen that there is a distribution of higher house prices in northeast Philadelphia. The city center and the south of the city center also have a high price. This trend has not changed significantly in the past five years. In general, the overall trend in prices varies geographically, but this differentiation has not changed significantly in census tracts.







