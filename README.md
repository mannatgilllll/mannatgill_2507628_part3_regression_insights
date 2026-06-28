# mannatgill_2507628_part3_regression_insights # Part 3: Regression-Based Business Insights & Model Interpretation

## Student Information

**Name:** Mannat Gill
**Student ID:** 2507628

---

# Business Problem Summary

A retail chain wants to understand which business factors are most strongly associated with monthly sales performance across its stores. Leadership is considering decisions such as increasing marketing spend, improving inventory availability, changing discount strategies, reallocating staff, and prioritizing investments across different store types and regions.

The objective of this project is to use regression analysis to identify the variables that are most strongly associated with monthly sales and provide data-driven business recommendations.

---

# Dataset Description

The dataset contains store-level monthly business information used to model sales performance.

Typical variables in the dataset include:

* Monthly Sales (Dependent Variable)
* Marketing Spend
* Footfall
* Average Discount Percentage
* Inventory Availability Percentage
* Customer Rating
* Region
* Store Type

Each row represents one store's monthly performance.

---

# Dependent Variable

**Monthly Sales**

Monthly Sales is the response (dependent) variable because it represents the business outcome the company wants to explain and improve.

---

# Independent Variables

Potential independent variables include:

* Marketing Spend
* Footfall
* Average Discount Percentage
* Inventory Availability Percentage
* Customer Rating
* Region (Dummy Variables)
* Store Type (Dummy Variables)

These variables are expected to influence monthly sales and are evaluated using regression analysis.

---

# Data Preparation

Before building regression models, the following preparation steps were completed:

* Reviewed the dataset for missing values.
* Checked for duplicate records.
* Validated numerical variables.
* Identified categorical variables requiring dummy encoding.
* Preserved the original dataset in a separate worksheet.
* Created cleaned and prepared data for modelling.

The original dataset was not modified.

---

# Regression Approach

Two types of regression models were developed.

## 1. Simple Linear Regression

Separate models were created using Monthly Sales as the dependent variable and one predictor at a time, for example:

* Marketing Spend
* Footfall
* Average Discount Percentage

Each model was evaluated using:

* Regression Equation
* Coefficient
* R-squared
* P-value
* Business Interpretation

---

## 2. Multiple Linear Regression

A multiple regression model was developed using:

* At least three numerical predictors
* At least one dummy variable created from a categorical variable

The model was evaluated using:

* Regression Coefficients
* R-squared
* Adjusted R-squared
* P-values
* Residual Analysis
* Business Interpretation

---

# Dummy Variable Approach

Categorical variables cannot be directly included in regression models.

Dummy variables were created for at least one categorical variable, such as:

* Region
* Store Type

One category was excluded and treated as the reference category to avoid the Dummy Variable Trap (perfect multicollinearity).

The dummy variable creation process is explained in:

```
outputs/model_equations.md
```

---

# Model Comparison Summary

Multiple regression models were compared based on:

* Variables Included
* R-squared
* Significant Predictors
* Business Usefulness
* Model Limitations

The comparison is documented in:

```
analysis/model_comparison.md
```

A summary table is also available in:

```
outputs/regression_summary.xlsx
```

---

# Residual Analysis

Residuals were calculated as:

Residual = Actual Sales − Predicted Sales

The analysis includes:

* Predicted Monthly Sales
* Residual Values
* Largest Positive Residuals
* Largest Negative Residuals
* Business Interpretation

Residual analysis helps identify stores where the model under-predicts or over-predicts sales and highlights unusual business behaviour.

Details are available in:

```
analysis/residual_analysis.md
```

---

# Final Model Selected

The final regression model was selected based on:

* Higher explanatory power (R-squared)
* Statistically significant variables
* Business interpretability
* Stable coefficients
* Practical usefulness for decision-making

The complete regression equations are documented in:

```
outputs/model_equations.md
```

---

# Business Recommendation

Based on the regression analysis, leadership should focus on the variables that demonstrate the strongest positive association with Monthly Sales while considering both statistical significance and business practicality.

Regression identifies relationships between variables but does not prove causation. Therefore, business decisions should combine regression findings with operational knowledge and additional testing where appropriate.

The complete recommendation is available in:

```
outputs/final_recommendation.md
```

---

# Assumptions and Limitations

The regression analysis is based on the following assumptions:

* Linear relationship between predictors and Monthly Sales.
* Independent observations.
* Normally distributed residuals.
* Constant variance of residuals (Homoscedasticity).
* Limited multicollinearity among predictors.

Limitations include:

* Regression measures association, not causation.
* External factors not included in the dataset may affect sales.
* Model performance depends on data quality and representativeness.
* Predictions are reliable only within the observed data range.

---

# Repository Structure

```
part3_regression_insights/

├── data/
│   └── business_regression_data.xlsx
│
├── analysis/
│   ├── regression_workbook.xlsx
│   ├── model_comparison.md
│   └── residual_analysis.md
│
├── outputs/
│   ├── regression_summary.xlsx
│   ├── final_recommendation.md
│   └── model_equations.md
│
├── screenshots/
│   ├── simple_regression_output.png
│   ├── multiple_regression_output.png
│   ├── residuals_preview.png
│   └── model_comparison_preview.png
│
└── README.md
```

---

# Screenshots Included

The repository contains the following screenshots:

* **simple_regression_output.png** – Output from a simple linear regression model.
* **multiple_regression_output.png** – Output from the multiple regression model.
* **residuals_preview.png** – Predicted values and residual calculations.
* **model_comparison_preview.png** – Comparison table summarizing regression models.

---

# Conclusion

This project applies regression analysis to identify factors associated with monthly sales performance. By combining simple and multiple regression models, dummy variable encoding, model comparison, and residual analysis, the project provides evidence-based insights to support retail decision-making while acknowledging the limitations of regression and the distinction between association and causation.
