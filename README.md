# Readme.md

# Airbnb Price Prediciton Project

This project's aim is to build a price prediction model based on Chicago Airbnb Listings dataset available from [InsideAirbnb](http://insideairbnb.com/get-the-data.html). The dataset is further extended by creating new variables based on geospatial analysis.

### Table of Contents

1. [Foreword](https://www.notion.so/gevosa/Readme-md-a7e27559376e49f48128f050731dc100#394dfb01b7e54d658836381ca150332a)
2. [Installation](https://www.notion.so/gevosa/Readme-md-a7e27559376e49f48128f050731dc100#ca49a53cb21f41c3aaa389c3c058da87)
3. [File Descriptions](https://www.notion.so/gevosa/Readme-md-a7e27559376e49f48128f050731dc100#443c6cd5dd334106976b853ab93e8e7f)
4. [Results](https://www.notion.so/gevosa/Readme-md-a7e27559376e49f48128f050731dc100#bb14749690ea461ab8573723830adb26)
5. [Resources](https://www.notion.so/gevosa/Readme-md-a7e27559376e49f48128f050731dc100#7b8596825ed04a4e868d484b49c6650b)

## Foreword

This project is a part of James Rocco Research Scholarship provided by Lake Forest College and was carried out under the supervision and with great help of Prof. Arthur Bousquet. The main idea is based on an article by Graciela Carrillo posted on [Towards Data Science](https://towardsdatascience.com/predicting-airbnb-prices-with-machine-learning-and-location-data-5c1e033d0a5a). 

## Installation

Using Anaconda create a new environment from environment.yml. 

```python
conda env create --file environment.yml
```

## File Descriptions (Follow in order)

To conveniently read all the notebooks follow this [link](https://nbviewer.jupyter.org/). 

1. [EDA.ipynb (Exploratory Data Analysis)](https://github.com/amac-lfc/airbnb/blob/master/EDA.ipynb) - A brief overview and analysis of raw data
2. kepler_map.ipynb - Visualization of the whole dataset using [Kepler.gl](http://kepler.gl) 
3. [data_preprocessing.ipynb](https://github.com/amac-lfc/airbnb/blob/master/data_preprocessing.ipynb) - Preprocessing the data for future uses (outlier detection, feature selection, handling missing data, etc.) 
4. regressions.ipynb - Development of initial price prediction models
5. geo_loc.py - A python script for geospatial analysis: creates 5 new variables using such libraries as [OSMnx](https://github.com/gboeing/osmnx) and [OpenRouteSerivce](https://github.com/GIScience/openrouteservice-py):
    - Restaurants - Number of restaurants in a 1000 meters radius
    - Cafes - Number of cafes in the radius
    - Bars - Number of bard in the radius
    - CTA - Number of CTA (Chicago Subway) stations in the radius
    - time_to_cta_minutes - Time in minutes to the nearest CTA station (can be out of the radius)
6. cta_mapping.ipynb - Visualization of geo_loc.py using [Folium](https://python-visualization.github.io/folium/index.html) maps (Map of routes to CTAs in the radius and shortest path detection)

## Results

Coming Soon 

## **Resources**

1. [https://www.youtube.com/playlist?list=PLLssT5z_DsK-h9vYZkQkYNWcItqhlRJLN](https://www.youtube.com/playlist?list=PLLssT5z_DsK-h9vYZkQkYNWcItqhlRJLN) - Complete Machine Learning Course by Andrew NG
2. [https://campus.datacamp.com/courses/pandas-foundations/](https://campus.datacamp.com/courses/pandas-foundations/) - Pandas Foundations Course on DataCamp
3. [https://learn.datacamp.com/courses/unsupervised-learning-in-python](https://learn.datacamp.com/courses/unsupervised-learning-in-python) - Unsupervised Learning Course on DataCamp
4. [https://learn.datacamp.com/courses/supervised-learning-with-scikit-learn](https://learn.datacamp.com/courses/supervised-learning-with-scikit-learn) - Supervised Learning Cousr on DataCamp
5. [https://www.textbook.ds100.org/intro.htmlPrinciples](https://www.textbook.ds100.org/intro.htmlPrinciples) and Techniques of Data Science By Sam Lau, Joey Gonzalez, and Deb Nolan
6. [https://github.com/Jie-Yuan/FeatureSelector/blob/master/Feature%20Selector%20Usage.ipynb](https://github.com/Jie-Yuan/FeatureSelector/blob/master/Feature%20Selector%20Usage.ipynb) - Feature_Selector package
7. [https://towardsdatascience.com/airbnb-price-prediction-using-linear-regression-scikit-learn-and-statsmodels-6e1fc2bd51a6](https://towardsdatascience.com/airbnb-price-prediction-using-linear-regression-scikit-learn-and-statsmodels-6e1fc2bd51a6) - Simmilar Price Prediciton model for Airbnb data
8. [https://towardsdatascience.com/ridge-and-lasso-regression-a-complete-guide-with-python-scikit-learn-e20e34bcbf0b](https://towardsdatascience.com/ridge-and-lasso-regression-a-complete-guide-with-python-scikit-learn-e20e34bcbf0b) - Explanation of the theory behind Lasso and Ridge Regressions
9. [https://www.youtube.com/watch?v=Q81RR3yKn30](https://www.youtube.com/watch?v=Q81RR3yKn30) - Ridge Regression
10. [https://www.youtube.com/watch?v=NGf0voTMlcs](https://www.youtube.com/watch?v=NGf0voTMlcs) - Lasso Regression
11. [https://www.youtube.com/watch?v=1dKRdX9bfIo&t=219s](https://www.youtube.com/watch?v=1dKRdX9bfIo&t=219s) - Elastic Net Regression
12. [https://www.youtube.com/watch?v=0GzMcUy7ZI0](https://www.youtube.com/watch?v=0GzMcUy7ZI0) - Theory behind PCA