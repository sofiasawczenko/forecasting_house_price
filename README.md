# Predicting Boston House Prices with Machine Learning

This project aims to develop a Machine Learning algorithm to predict the average price of houses in Boston.

## Dataset

The data for this project was extracted from the Kaggle dataset. It contains pertinent information about various features of houses in Boston, such as the number of rooms, neighborhood crime rate, proximity to urban centers, and more.

## Project Overview

Real estate prices in Boston can be influenced by a multitude of factors, from location and size to local market trends. In this project, I utilized supervised regression learning, a technique where a model learns from labeled data and analyzes the relationship between variables for accurate predictions. The goal is to model this relationship and make precise estimations based on the data.

## Exploratory Data Analysis (EDA)

### Dataset Overview

The dataset contains the following columns:
- **RM**: Average number of rooms per house in the neighborhood.
- **LSTAT**: Percentage of homeowners in the neighborhood considered of "lower class."
- **PTRATIO**: Ratio of students to teachers in schools in the neighborhood.
- **MEDV**: Median value of owner-occupied homes (target variable).

### Dataset Properties
```python
df.shape
# Output: (489, 4)

df.dtypes
# Output:
# RM         float64
# LSTAT      float64
# PTRATIO    float64
# MEDV       float64
```
