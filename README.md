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

### Dataset
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
### Statistical Summary
```python
df.describe()
```
![image](https://github.com/user-attachments/assets/5c720765-eba2-4af3-975f-bafe4236a58c)

### Data Exploration and Preprocessing
**1. Statistical Analysis:**
- Summary statistics for all features were analyzed.
- Relationships between features were visualized using scatter plots and heatmaps.

**2. Outlier Analysis:**
- Boxplots were created for each feature to detect outliers.

**3. Normality Tests:**
- Conducted Shapiro-Wilk and Lilliefors tests for normality.
- QQ plots and histograms were generated for visual analysis.

**4. Correlation:**
- Pearson, Spearman, and Kendall correlation methods were applied to study feature relationships.

### Models Developed
**1. Simple Linear Regression**
- Example: Predicting house price (MEDV) using the average number of rooms (RM).
- Performance:
R²: Train = 0.57, Test = 0.60
RMSE: ~99,315

**2. Multiple Linear Regression**
- Features: RM, LSTAT, PTRATIO
- Equation:
MEDV = Intercept + (Coefficient_RM × RM) + (Coefficient_LSTAT × LSTAT) + (Coefficient_PTRATIO × PTRATIO)
Performance:
R²: Train = 0.73, Test = 0.68
RMSE: ~96,087

**3. Polynomial Regression**
- Applied a polynomial transformation to model non-linear relationships.
- Example: Quadratic regression on RM.

**4. Cross-Validation**
- Used 15-fold cross-validation to assess model generalization.
- Best R²: ~69.25% (Multiple Linear Regression).

## Key Results
**1. Simple Linear Regression:**
- Moderate fit; suitable for understanding single variable impacts.

**2. Multiple Linear Regression:**
- Improved accuracy by incorporating multiple features.
  
**3. Polynomial Regression:**
- Captured non-linear trends but increased computational complexity.

## Tools and Libraries
- Python: Core programming language.
- Libraries:
   **NumPy, Pandas** for data handling.
   **Matplotlib, Seaborn, Plotly** for visualization.
   **Scikit-learn** for machine learning algorithms.
   **SciPy, Statsmodels** for statistical analysis.

## Conclusion
The models demonstrate that house prices in Boston are influenced by various factors, with multiple regression providing the most accurate predictions. Further refinements can include feature engineering, hyperparameter tuning, and exploring advanced models like Random Forest or Gradient Boosting.
