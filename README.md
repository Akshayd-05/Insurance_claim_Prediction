# Health Insurance Claim Prediction

This repository contains a project focused on predicting health insurance claims based on various demographic, lifestyle, and health factors. The dataset includes variables like age, weight, BMI, exercise habits, smoking status, and medical conditions. The goal of the project is to explore and analyze the data, apply machine learning models, and make predictions regarding health insurance claims.

## Dataset Overview

The **Health Insurance Dataset** consists of the following key variables:

- **Age**: Individual's age, crucial for assessing health risk and insurance cost.
- **Sex**: Gender of individuals, affecting risk assessment and health needs.
- **Weight**: Individual's weight, indicative of overall health status.
- **BMI**: Body Mass Index, measuring obesity levels, which impacts health risk and insurance premiums.
- **Hereditary Diseases**: Presence of inherited diseases, affecting insurance risk assessments.
- **No. of Dependents**: Influences insurance coverage needs and potential claims.
- **Smoker**: Smoking status, which significantly impacts health risks and insurance rates.
- **City**: Residence city, affecting healthcare access and cost variations.
- **Blood Pressure**: Indicator of cardiovascular health, influencing risk and premiums.
- **Diabetes**: Presence of diabetes, crucial for assessing health and coverage.
- **Regular Exercise**: Exercise habits, impacting health status and insurance costs.
- **Job Title**: Provides insight into occupational risks and lifestyle.
- **Claim**: The insurance claim amount, reflecting financial implications of health risks.

## Project Analysis

### Summary
- The dataset provides insights into the relationships between various factors and health insurance claim amounts.
- Missing values in 'age' and 'bmi' were imputed with their respective mean values.
- The **correlation matrix** showed:
  - A positive correlation between age, weight, and BMI.
  - A notable correlation between smoking and high claim amounts (0.77).
- Outliers were removed using the **Interquartile Range (IQR)** method for a cleaner dataset.

### Visualizations
1. **Histogram of Claim Amounts**: Shows the distribution of insurance claims, with the highest frequency between 0 and 20,000 dollars.
2. **Bar Plot of Claims by Smoking Status**: Non-smokers have higher claim amounts, while smokers' claims are lower.
3. **Impact of Regular Exercise on Claims**: Those who engage in regular exercise tend to have lower insurance claims.
4. **Boxplot of BMI by Diabetes Status**: Highlights BMI distribution across diabetes status, showing a higher BMI for individuals with diabetes.

## Machine Learning Models

### 1. **Linear Regression**: 
   - **Age, Weight, and Exercise** were used to predict the health insurance claim amount.
   - The model showed that age has a positive impact on the claim amount, while regular exercise significantly reduces the claim amount.

### 2. **Logistic Regression**: 
   - Used to predict the likelihood of having diabetes based on **Age** and **BMI**.
   - The model showed that both age and BMI positively influence the likelihood of having diabetes, with a modest AUC of 0.5659.

### 3. **Lasso Regression**: 
   - Employed to analyze the relationship between predictors, including **Smoking**, and insurance claims.
   - Lasso regularization helped identify the most influential variables while penalizing less important predictors.

### 4. **Ridge Regression**: 
   - Analyzed the impact of **Regular Exercise** and **Blood Pressure** on insurance claims.
   - The Ridge regression model showed reasonable predictive capabilities, with an RMSE of 11989.526.

## Project Conclusion

This project provides a comprehensive analysis of the factors influencing health insurance claims. The predictive models developed can help in better risk assessment and decision-making in insurance.

## Files in the Repository

- `insurance_claim_prediction.ipynb`: Jupyter notebook containing data analysis, visualizations, and model implementation.
- `insurance_claim_data.csv`: Raw dataset used for analysis and prediction.
