# BoomBikes Linear Regression Analysis

This project analyzes bike sharing data to predict daily bike demand using linear regression.

## Problem Statement

BoomBikes is a bike-sharing company that has faced revenue challenges due to COVID-19. They want to understand what factors affect bike demand so they can plan better for when things get back to normal.

The company wants to know:
- Which factors are most important for predicting bike demand?
- How can they use this information to make business decisions?

## Dataset

The dataset contains daily bike sharing data with information about:
- Weather conditions (temperature, humidity, wind speed)
- Time factors (season, month, year, working day)
- Bike rental counts (casual users, registered users, total)

## My Approach

I followed these steps to solve the problem:

1. **Data Loading**: Imported the day.csv file and checked for any data quality issues
2. **Data Understanding**: Explored the data to understand patterns and relationships
3. **Data Preparation**: Converted categorical variables and created dummy variables
4. **Train-Test Split**: Split data into 70% training and 30% testing
5. **Feature Scaling**: Used StandardScaler to normalize the features
6. **Feature Selection**: Used RFE (Recursive Feature Elimination) to find the best features
7. **Model Building**: Built linear regression model using scikit-learn
8. **Model Validation**: Checked assumptions and evaluated performance
9. **Business Insights**: Interpreted results for practical business use

## Key Findings

### Model Performance
- **R² Score: 0.836** - The model explains 83.6% of variation in bike demand
- **RMSE: ±804 bikes** - Average prediction error
- The model performs well and is reliable for forecasting

### Important Factors (Top 3)
1. **Year (2019 vs 2018)**: Being in 2019 increases demand by ~1974 bikes/day
2. **Temperature**: Higher temperatures increase bike demand significantly  
3. **Weather Conditions**: Light rain/snow decreases demand by ~1901 bikes/day

### Business Insights
- **Seasonal Patterns**: Fall is the best season (5,644 bikes/day), Spring is lowest (2,604 bikes/day)
- **Weather Impact**: Clear weather drives highest demand (4,876 bikes/day)
- **Growth Trend**: 47% growth from 2018 to 2019 shows strong business recovery
- **Temperature Effect**: Temperature has 0.627 correlation with demand - strongest numerical predictor

## Technical Details

### Libraries Used
- pandas, numpy: Data manipulation
- matplotlib, seaborn: Data visualization
- scikit-learn: Machine learning (LinearRegression, RFE, StandardScaler)
- statsmodels: Statistical analysis and detailed model summary

### Model Specifications
- **Algorithm**: Multiple Linear Regression
- **Feature Selection**: RFE with 15 optimal features
- **Preprocessing**: StandardScaler for feature normalization
- **Validation**: Train-test split with basic assumption checking

## Files in This Project

- `BikeSharing_LinearRegression.ipynb`: Main analysis notebook with all code and results
- `day.csv`: Original dataset with daily bike sharing data
- `Linear_Regression_Subjective_Answers.pdf`: Answers to assignment questions
- `README.md`: This overview file

## How to Run

1. Make sure you have Python with pandas, numpy, matplotlib, seaborn, and scikit-learn installed
2. Place the `day.csv` file in the same directory as the notebook
3. Run all cells in the Jupyter notebook from top to bottom
4. The analysis will generate visualizations and model results

## Results Summary

The linear regression model successfully identifies the key drivers of bike sharing demand and provides BoomBikes with actionable insights for their business recovery strategy. The model shows that weather conditions, seasonal patterns, and the overall growth trend are the most important factors to consider when planning operations and fleet management.

The analysis demonstrates that bike sharing demand is highly predictable using basic weather and temporal factors, giving BoomBikes a solid foundation for data-driven decision making.
