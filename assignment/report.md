# Smart Factory Energy Consumption Prediction Report

## Overview
This project aims to predict the energy consumption of equipment in a smart factory using historical sensor data. The dataset includes various environmental and operational parameters, such as temperature, pressure, and humidity, recorded at specific timestamps. We have employed several machine learning models to predict the target variable, `equipment_energy_consumption`. The models were evaluated based on their performance on a test set, and feature importance analysis was conducted to identify the key factors influencing energy consumption.

## Model Performance

### Performance Table

The following table presents the evaluation metrics for the models trained on the data:

| Model             | RMSE   | MAE    | R²    |
|-------------------|--------|--------|-------|
| Linear Regression | 162.07 | 71.84  | 0.02  |
| Ridge             | 162.07 | 71.84  | 0.02  |
| Random Forest     | 159.12 | 68.62  | 0.06  |

- **RMSE (Root Mean Squared Error)**: Indicates the model's average prediction error.
- **MAE (Mean Absolute Error)**: Measures the average absolute difference between predicted and actual values.
- **R²**: Shows the proportion of variance in the target variable explained by the model.

### Insights

- The **Random Forest** model performed the best in terms of RMSE and R², although the performance is still not very high. This suggests that there are other factors or improvements (like feature engineering or hyperparameter tuning) that could boost accuracy.
- Both **Linear Regression** and **Ridge** models show nearly identical performance, with slightly worse metrics than the Random Forest model.

## Feature Importance

The feature importance analysis for the **Random Forest** model reveals that the most impactful features influencing energy consumption are:

- **Zone Temperatures (Zones 1-4)**
- **Outdoor Temperature**
- **Lighting Energy Consumption**
- **Machine Load**
- **Humidity Levels**

These insights can guide energy optimization efforts in specific zones and processes.


## Recommendations

Based on the analysis and model results, the following recommendations are made:

1. **Optimize HVAC in High-Impact Zones**: Zone temperatures (Zones 1–4) are key predictors of energy consumption. Focus on improving HVAC systems in these areas to reduce energy usage.
2. **Upgrade Lighting Systems**: The moderate impact of lighting energy consumption suggests that upgrading to energy-efficient LEDs or implementing smart lighting systems can yield significant savings.
3. **Monitor Real-Time Data for High-Impact Zones**: Zones with high energy consumption, such as those with high temperatures or machine loads, should be continuously monitored to adjust equipment usage dynamically.
4. **Shift Non-Critical Loads to Off-Peak Hours**: Energy peaks in certain hours suggest that non-essential processes should be shifted to off-peak times to optimize overall energy usage.
5. **Investigate Unexplained Variability**: Features like humidity and machine load had varying degrees of importance. Further investigation into their correlation with energy usage may uncover additional optimization opportunities.

## Conclusion

The model analysis and feature importance provide valuable insights into optimizing energy consumption in the smart factory. By focusing on the most influential factors, such as temperature, lighting, and machine load, significant improvements in energy efficiency can be achieved.
