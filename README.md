# Diamond Price Prediction

Welcome to the Diamond Price Prediction project! This repository contains code and insights for predicting the prices of diamonds based on various features such as carat, cut, color, clarity, and dimensions. The project uses multiple regression models, with a focus on a stacking regressor for improved accuracy.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Feature Engineering](#feature-engineering)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Final Model and Predictions](#final-model-and-predictions)
- [Conclusion](#conclusion)

## Introduction

This project aims to predict the prices of diamonds using various machine learning models. We employ techniques like one-hot encoding, feature engineering, and advanced ensemble methods to achieve high prediction accuracy.

## Dataset

The dataset used in this project contains the following features:
- `carat`: The weight of the diamond.
- `cut`: The quality of the cut (Fair, Good, Very Good, Premium, Ideal).
- `color`: The color grade of the diamond (D to J, with D being the best).
- `clarity`: The clarity of the diamond (IF, VVS1, VVS2, VS1, VS2, SI1, SI2, I1).
- `depth`: Total depth percentage.
- `table`: The width of the top of the diamond relative to the widest point.
- `x`, `y`, `z`: Dimensions of the diamond in mm.
- `price`: The price of the diamond (target variable).

## Exploratory Data Analysis

We performed extensive exploratory data analysis (EDA) to understand the distribution and relationships between the features and the target variable, `price`. Key visualizations include:
- **Price vs. Carat**
- **Price vs. Cut**
- **Price vs. Color**
- **Price vs. Clarity**

## Feature Engineering

Feature engineering steps included:
- Creating a `volume` feature by multiplying `x`, `y`, and `z`.
- Encoding categorical features (`cut`, `color`, `clarity`) using one-hot encoding.

## Modeling

We experimented with various models, including:
- Linear Regression
- Ridge Regression
- Lasso Regression
- Decision Tree Regression
- Random Forest Regression
- Gradient Boosting Regression
- XGBoost Regression

The final model is a **Stacking Regressor** that combines the strengths of multiple models:
- **Base Models**: Random Forest, Gradient Boosting, XGBoost
- **Final Estimator**: Ridge Regression

## Evaluation

The models were evaluated using Root Mean Squared Error (RMSE) and R-squared (R²) metrics. The final stacking model achieved:
- **RMSE**: 516.48
- **R²**: 0.983

These metrics indicate a high level of accuracy in predicting diamond prices.

## Final Model and Predictions

The final model was used to make predictions on a test set. The predictions were saved to a CSV file for submission.

## Conclusion

The project demonstrates the effectiveness of ensemble methods, particularly stacking, in predicting diamond prices. The feature engineering and model tuning steps were crucial in achieving high accuracy.
