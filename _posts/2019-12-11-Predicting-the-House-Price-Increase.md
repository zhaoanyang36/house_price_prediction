---
title: "Predicting the House Price Increase"
date: 2019-12-11
published: true
tags: [hvplot]
excerpt: "The random forest was used in this part to make the prediction."
hv-loader:
  hv-chart-1: "charts/d.html"
altair-loader:
  altair-chart-1: "charts/top20.json"
  altair-chart-2: "charts/scatterplot.json"
toc: true
toc_sticky: true
---
In this part, we desire to predict the increase rate by census tract in philadelphia. We hope the prediction can help the different groups of people understanding the trend of the house price in specific area and help them making decision

## Data preprocessing
- First, we calculate the **Price Increase percentage** and **Price percentage** for every census tract.
```python
test_sales_tract18['Price Increase percentage'] = test_sales_tract18['sale_price_K']/test_sales_tract13['sale_price_K']
test_sales_tract18['Price Increase'] = test_sales_tract18['sale_price_K']-test_sales_tract13['sale_price_K']
```
- We collect the sales data of 2018 and select the feature columns we want to use.
```python
# The feature columns we want to use
cols = [
    "sale_price",
    "total_livable_area",
    "total_area",
    "garage_spaces",
    "fireplaces",
    "number_of_bathrooms",
    "number_of_bedrooms",
    "number_stories",
    "exterior_condition",
    "zip_code",
    "geometry"
]
```
- Use the spatial join to combine the sales data with tract data and add the columns **Price Increase percentage** and **Price percentage** for the sales data.
- Do the data cleaning，such as trim thr columns and remove NaNs, trim zip code to only the first five digits.
```python
sales = salesRaw[cols].dropna()
sales['zip_code'] = sales['zip_code'].astype(str).str.slice(0, 5)
```

## Feature Eng
We create some feature for our sales data. For example:

- Distance to the *nearest* university/college
- Distance to the nearest park centroid
- Distance to City Hall
- Distance to the 5 nearest new construction permits from 2018.

Then we make a regression by random forest to predict the Price Change Percentage.
<div id="hv-chart-1"></div>
