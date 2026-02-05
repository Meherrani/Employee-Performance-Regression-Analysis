# Employee Performance Analysis & Regression Modeling

## Overview
This project performs an end-to-end HR analytics study using the R programming language to understand and predict employee performance using statistical analysis and regression modeling. The objective is to identify the most influential factors affecting employee performance and build a validated predictive model that can support data-driven HR decision-making.

The analysis follows a structured workflow including data cleaning, exploratory data analysis (EDA), feature engineering, regression modeling, model selection, and cross-validation.

---

## Problem Statement
Organizations often face challenges in objectively evaluating and predicting employee performance. Performance is influenced by multiple factors such as training, experience, KPIs, awards, education level, department, and recruitment channel.

The goal of this project is to:
- Identify key performance indicators (KPIs) that significantly impact employee performance
- Quantify the relationship between training and performance
- Build a statistically sound regression model with strong predictive power
- Validate the model to ensure generalizability to unseen data

---

## Dataset
- **Source:** Kaggle – Employee’s Performance for HR Analytics  
- **Link:** https://www.kaggle.com/datasets/sanjanchaudhari/employees-performance-for-hr-analytics  
- **Description:**  
  The dataset contains employee-level information including demographics, education, department, training history, KPIs, awards, recruitment channels, and performance-related metrics.

---

## Project Structure


---


---

## Data Cleaning & Preprocessing
The following preprocessing steps were applied:
- Identified missing and blank values across all variables
- Observed that employees with less than one year of experience had missing values for `previous_year_rating`
- Replaced missing values in `previous_year_rating` with 0
- Removed records with blank values in the `education` field
- Converted categorical variables into numerical dummy variables

### Baseline Categories
- Department: Analytics  
- Education: Bachelors  
- Gender: Female  
- Recruitment Channel: Other  

This ensured interpretability and consistency in regression modeling.

---

## Exploratory Data Analysis (EDA)
EDA was performed to understand data distributions and relationships:
- Distribution analysis for categorical variables
- Boxplots to analyze variability in employee performance
- Scatter plots to study relationships between numerical variables
- Correlation analysis for:
  - Numerical variables
  - Dummy variables

These analyses helped identify potential predictors and detect multicollinearity issues.

---

## Regression Modeling
### Model Type
- Multiple Linear Regression

### Model Selection Techniques
- Backward elimination
- Forward selection
- Cp and Adjusted R-squared comparison

Variables that were found to be statistically insignificant during selection included:
- Number of trainings
- Age
- Length of service
- Certain department and recruitment channel indicators

---

## Final Model
The final selected model was based on forward selection and achieved strong statistical performance.

**Adjusted R-squared:** 0.886  
**Interpretation:** The model explains approximately **88.6%** of the variability in employee performance.

All retained predictors were statistically significant with p-values < 0.05.

---

## Model Validation
### Train-Test Split
- Training set: 75%
- Test set: 25%

### Cross-Validation
- 5-fold cross-validation
- Evaluated using Root Mean Squared Error (RMSE)

**Cross-validated RMSE:** ~0.00298

The low RMSE indicates strong predictive accuracy and generalizability.

---

## Model Diagnostics
- Residual analysis confirmed no major violations of regression assumptions
- No significant multicollinearity detected
- Influential points and outliers were examined and addressed

---

## Key Insights
- Previous year performance ratings and KPI completion strongly influence employee performance
- Awards won have a measurable impact on training performance outcomes
- Education level and department play a significant role in performance variability
- Recruitment channels contribute differently to performance outcomes
- The regression model demonstrates high explanatory and predictive power

---

## Tools & Technologies
- R
- RMarkdown
- Statistical Modeling (lm)
- DAAG library for cross-validation
- GitHub for version control

---

## How to Reproduce the Analysis
1. Clone the repository
2. Download the dataset from Kaggle and place it in the `data/` folder
3. Open the RMarkdown file in RStudio
4. Ensure required R libraries are installed
5. Run the analysis sequentially
6. Knit the RMarkdown file to generate the final report

---

## Conclusion
This project demonstrates a robust and validated regression framework for employee performance prediction. With strong explanatory power and reliable validation results, the model provides actionable insights that can support HR strategy, performance evaluation, and workforce planning.

---

## Author
**Vamsi Routhu**

