
# Model Comparison

## Overview

Three regression models were developed to identify factors influencing monthly sales in the retail chain.

### Model 1: Simple Linear Regression – Marketing Spend

* **Dependent Variable:** Monthly Sales
* **Independent Variable:** Marketing Spend

**R-squared:** *(Insert your R² value)*

Marketing spend was found to have a positive and statistically significant relationship with monthly sales (p < 0.05). The model indicates that higher marketing investment is associated with increased sales. However, because only one predictor is included, the model does not account for other operational factors that may influence sales.

---

### Model 2: Simple Linear Regression – Footfall

* **Dependent Variable:** Monthly Sales
* **Independent Variable:** Footfall

**R-squared:** *(Insert your R² value)*

Footfall showed a positive and statistically significant relationship with monthly sales (p < 0.05). The model suggests that stores with more customer visits generally achieve higher sales. Like the previous model, it considers only one predictor and therefore has limited explanatory power.

---

### Model 3: Multiple Linear Regression

* **Dependent Variable:** Monthly Sales

**Independent Variables:**

* Marketing Spend
* Footfall
* Average Discount Percentage
* Staff Count
* Store Type (Dummy Variables)

**R-squared:** 0.7998

The multiple regression model explains approximately **80% of the variation in monthly sales**, making it substantially more informative than the individual simple regression models.

Statistically significant variables include:

* Marketing Spend
* Footfall
* Average Discount Percentage
* Store_High_Street
* Store_Airport
* Store_Mall

Staff Count was not statistically significant (p > 0.05).

---

## Model Comparison

| Criteria              | Simple Regression    | Multiple Regression                     |
| --------------------- | -------------------- | --------------------------------------- |
| Variables Included    | One predictor        | Multiple predictors                     |
| R-squared             | Lower                | Higher (0.7998)                         |
| Business Insight      | Limited              | Comprehensive                           |
| Significant Variables | Single variable only | Multiple significant drivers identified |
| Decision Support      | Limited              | Strong                                  |

---

## Business Usefulness

The multiple regression model provides better support for business decision-making because it evaluates the combined impact of marketing activities, customer traffic, staffing, pricing strategy, and store type. It enables management to identify the most influential factors affecting monthly sales while controlling for the effects of other variables.

---

## Limitations

* The model assumes linear relationships between predictors and monthly sales.
* Other factors such as local economic conditions, competitor promotions, and seasonal trends are not included.
* The analysis is based on historical data and may not fully capture future market changes.
* Some variables, such as staff count, were not statistically significant and may require further investigation.
