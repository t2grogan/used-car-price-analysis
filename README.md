# Used Car Price Analysis

## Summary

This project analyzes 368,000 used car listings to identify the key drivers of used car prices, 
providing actionable inventory and pricing recommendations for a used car dealership client. 
The analysis follows the CRISP-DM framework across business understanding, data understanding, 
data preparation, modeling, evaluation, and deployment phases.

## Key Findings

- **Vehicle age** is the strongest predictor of price -- newer vehicles command significantly higher resale values
- **Odometer reading** independently depresses price regardless of vehicle age
- **Manufacturer tier** matters -- luxury brands command a consistent premium over mass-market and budget brands even after controlling for age and mileage
- **Title status** is critical -- clean titles are strongly associated with higher prices while salvage and rebuilt titles carry discounts that are difficult to overcome
- **Drive type and fuel type** contribute secondary signal, with 4WD/AWD and diesel vehicles showing pricing premiums in relevant segments

## Methods

- Data cleaning and outlier filtering on 426,000 raw records yielding 368,000 usable observations
- Feature engineering including manufacturer tier grouping and year x odometer interaction term
- Log transformation of target variable to address price skew
- Linear Regression, Ridge, and Lasso models evaluated on RMSE and R²
- Final model R² of ~0.65 with a prediction error factor of ~1.68x

## Notebook

[used_car_price_analysis.ipynb](used_car_price_analysis.ipynb)
