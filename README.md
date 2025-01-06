# Boston House Price Prediction

This repository contains a comprehensive analysis and predictive modeling project based on the Boston House Price dataset. The primary objective is to develop regression models to estimate the median value of owner-occupied homes in Boston (MEDV) using neighborhood statistics.

---

## Project Overview

This project explores linear regression and its advanced regularization techniques: Ridge, Lasso, and Elastic Net regression. Key steps include:

1. **Data Preprocessing**: Handling outliers, skewness, and multicollinearity.
2. **Feature Selection and Engineering**: Selecting and engineering predictors for optimal performance.
3. **Model Implementation**: Building and tuning regression models.
4. **Evaluation**: Comparing models using performance metrics such as R-squared, MSE, and MAPE.

The final model employs Elastic Net regression, achieving the best balance between predictive accuracy and robustness.

---

## Dataset

The dataset originates from the U.S. Census Service and is a part of the sklearn library. It includes 13 features:

- **CRIM**: Per capita crime rate by town.
- **ZN**: Proportion of residential land zoned for lots over 25,000 sq. ft.
- **INDUS**: Proportion of non-retail business acres per town.
- **CHAS**: Charles River dummy variable (1 if tract bounds river; 0 otherwise).
- **NOX**: Nitric oxides concentration (parts per 10 million).
- **RM**: Average number of rooms per dwelling.
- **AGE**: Proportion of owner-occupied units built prior to 1940.
- **DIS**: Weighted distances to five Boston employment centers.
- **RAD**: Index of accessibility to radial highways.
- **TAX**: Full-value property tax rate per $10,000.
- **PTRATIO**: Pupil-teacher ratio by town.
- **B**: 1000(Bk - 0.63)^2 where Bk is the proportion of Black residents by town.
- **LSTAT**: Percentage of lower-status population.

**Target Variable**:
- **MEDV**: Median value of owner-occupied homes (in $1,000).

---

## Key Findings

1. **Exploratory Data Analysis**:
   - Identified potential predictors: RM, LSTAT, and PTRATIO.
   - Discovered multicollinearity among features such as TAX and RAD.

2. **Data Preprocessing**:
   - Treated outliers and skewness for improved model robustness.
   - Used log transformations and standard scaling.
   - Selected features with high correlation to MEDV while addressing multicollinearity using Variance Inflation Factor (VIF).

3. **Model Performance**:
   - **Baseline Model**: Linear regression with all features achieved an R² of 0.6688.
   - **Advanced Models**: Elastic Net regression performed best with:
     - R²: 0.7177
     - MSE: 20.8063
     - MAPE: 15.18%

4. **Regularization**:
   - Ridge and Lasso addressed overfitting but required careful tuning.
   - Elastic Net balanced L1 (Lasso) and L2 (Ridge) penalties for optimal feature selection and prediction.

---

## Repository Structure

- **Boston_House_Price_Report.pdf**: Comprehensive report detailing the methodology, results, and analysis.
- **Notebook**: Python Jupyter Notebook implementing the entire analysis and modeling pipeline.
- **README.md**: This file.

---

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/boston-house-price-prediction.git
   ```
2. Open the Jupyter Notebook to explore the analysis:
   ```bash
   jupyter notebook Boston_House_Price_Analysis.ipynb
   ```
3. Review the report for detailed explanations.

---

## Results and Insights

- Regularization improves model performance by addressing overfitting and multicollinearity.
- Elastic Net regression is particularly effective when predictors exhibit multicollinearity and require feature selection.
- Preprocessing steps, such as outlier removal and feature scaling, significantly impact model accuracy.

---

## Recommendations

1. Enhance preprocessing by exploring advanced imputation methods or robust regression techniques.
2. Experiment with polynomial features or dimensionality reduction to capture non-linear relationships.
3. Incorporate additional datasets to improve model generalizability.

---

## References

- [Statistics By Jim: Multicollinearity in Regression Analysis](https://statisticsbyjim.com/regression/multicollinearity-in-regression-analysis/)
- [Sklearn Documentation: Ridge, Lasso, and Elastic Net](https://scikit-learn.org/)
- [Kumar, A. "Boston Housing Dataset Linear Regression"](https://vitalflux.com/)

---

## Author

Aaron Jetro C. Alvarez
