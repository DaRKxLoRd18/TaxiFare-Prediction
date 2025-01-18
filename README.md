
# Taxi Fare Prediction Project

## Overview
This project predicts taxi fares in urban areas to improve fairness, transparency, and customer satisfaction. Using the **2015 Green Taxi Trip Data** of New York City, we developed machine learning models to estimate taxi fares based on dynamic variables like trip distance, time of day, and traffic conditions. The best-performing model, **XGBoost**, achieved a high accuracy with an **R² score of 0.956** after optimization and feature engineering.

## Authors
- Harsh Rawat (20222202)
- Manveet Singh (2022280)
- Harshit Gautam (2022208)
- Karan Yadav (2022234)

## Problem Statement
Accurate prediction of taxi fares is essential to:
- Ensure consistent pricing across varying conditions.
- Incorporate multiple factors influencing ride costs.
- Build transparent pricing systems.
- Address nonlinear relationships between variables like distance and time.

## Methodology
### Dataset
The dataset used is the **2015 Green Taxi Trip Data**, which includes:
- Pickup/drop-off locations.
- Passenger count.
- Trip distance.
- Fare amount.

### Data Preprocessing
Key preprocessing steps:
- **Feature Removal**: Excluded irrelevant features such as `vendorid`, `payment type`, and others to avoid data leakage and reduce complexity.
- **Date & Time Engineering**: Extracted temporal features like year, month, day, hour, etc.
- **Feature Scaling**: Applied standardization using `StandardScaler` from scikit-learn.
- **Outlier Removal**: Identified and removed spatial outliers in pickup/drop-off coordinates.

### Feature Engineering
Analyzed correlations and removed temporal features like day of the week and day of the month, as they showed minimal influence on fares.

### Models Evaluated
1. Linear Regression
2. Polynomial Regression
3. Decision Tree
4. Random Forest
5. XGBoost
6. Multi-Layer Perceptron (MLP)
7. Ridge Regression (L2 Regularization)

**XGBoost** emerged as the best model, and hyperparameters were optimized using grid search.

## Results
### XGBoost Performance (Post Optimization)
| Metric   | Test Set | Train Set |
|----------|----------|-----------|
| MAE      | 0.49     | 0.137     |
| MSE      | 4.320    | 0.035     |
| R² Score | 0.942    | -         |

### XGBoost Performance (Pre Optimization)
| Metric   | Test Set | Train Set |
|----------|----------|-----------|
| MAE      | 0.933    | 0.224     |
| MSE      | 0.933    | 0.118     |
| R² Score | 0.682    | -         |

### Comparison with MLP
| Metric   | Test Set | Train Set |
|----------|----------|-----------|
| MAE      | 1.13     | 1.1158    |
| MSE      | 1.129    | 87.598    |
| R² Score | 0.642    | -         |

## Conclusion
- **XGBoost** demonstrated superior performance due to its ability to handle complex, nonlinear relationships.
- Feature engineering and outlier removal significantly enhanced model reliability.
- The study highlights the importance of data preprocessing and hyperparameter tuning in improving model accuracy.

## References
1. NYC Taxi Fare Prediction Using Machine Learning (2023): [Link](https://github.com/harshrawat22202/ML-Project_final)
2. 2015 Green Taxi Trip Data: [Link](https://data.cityofnewyork.us/Transportation/2015-Green-Taxi-Trip-Data/gi8d-wdg5/about_data)
3. Fare and Duration Prediction: A Study of New York City Taxi Rides: [Link](https://cs229.stanford.edu/proj2016/report/AntoniadesFadaviFobaAmonJuniorNewYorkCityCabPricing-report.pdf)

## Repository
For the complete project details, visit the [GitHub repository](https://github.com/DaRKxLoRd18/TaxiFare-Prediction.git).
