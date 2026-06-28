# Model Equations

## Introduction

Regression analysis was used to identify the business factors most strongly associated with monthly sales across retail stores. Both simple linear regression and multiple linear regression models were developed. The simple regression models evaluated the effect of one variable at a time, while the multiple regression model assessed the combined impact of several operational and store-related factors.

---

# Simple Regression Equations

## Model 1: Marketing Spend

**Equation**

**Monthly Sales = Intercept(560777.345449437) + (Marketing Spend Coefficient(2.12957532758983) × Marketing Spend)**

### Business Interpretation

This model estimates monthly sales using only marketing spend. The positive relationship indicates that increasing marketing investment is associated with higher monthly sales. However, since this model considers only one factor, it does not capture the influence of customer traffic, staffing, pricing strategy, or store type.

---

## Model 2: Footfall

**Equation**

**Monthly Sales = Intercept(446410.582933953) + (Footfall Coefficient(35.6780310726405) × Footfall)**

### Business Interpretation

This model predicts monthly sales based only on customer footfall. The positive coefficient indicates that stores attracting more customers generally generate higher sales. While useful for understanding customer traffic, this model ignores several other business factors that also affect sales performance.

---

# Multiple Regression Equation

The final multiple regression model is:

**Monthly Sales = 380,861.98**

**+ (1.115 × Marketing Spend)**

**+ (29.111 × Footfall)**

**− (82,179.33 × Average Discount %)**

**+ (2,460.17 × Staff Count)**

**+ (17,099.18 × Store_High_Street)**

**+ (35,613.77 × Store_Airport)**

**+ (26,173.48 × Store_Mall)**

---

# Explanation of Each Coefficient

### Intercept (380,861.98)

The intercept represents the estimated monthly sales for a store in the reference store type (Residential) when all numerical variables are zero. Although this situation is unlikely in practice, the intercept provides the baseline from which the effects of the other variables are measured.

### Marketing Spend (1.115)

Holding all other variables constant, every one-unit increase in marketing spend is associated with an average increase of approximately **1.12 units** in monthly sales. This suggests that marketing investment contributes positively to revenue growth.

### Footfall (29.111)

Each additional customer visiting the store is associated with an average increase of approximately **29.11 units** in monthly sales. This indicates that increasing customer traffic is one of the most effective ways to improve sales.

### Average Discount Percentage (-82,179.33)

The negative coefficient indicates that higher average discount percentages are associated with lower monthly sales after considering the other variables. This suggests that excessive discounting may reduce revenue or may be more common during lower-performing sales periods.

### Staff Count (2,460.17)

The positive coefficient suggests that stores with more employees tend to have higher sales. However, because this variable was not statistically significant in the final model (p = 0.069), its effect should be interpreted with caution.

### Store_High_Street (17,099.18)

High Street stores are expected to generate approximately **17,099** more units of monthly sales than the reference store type, assuming all other variables remain constant.

### Store_Airport (35,613.77)

Airport stores are expected to generate approximately **35,614** more units of monthly sales than the reference store type, making them the strongest-performing store format in the model.

### Store_Mall (26,173.48)

Mall stores are expected to generate approximately **26,173** more units of monthly sales than the reference store type.

---

# Explanation of Dummy Variables

Store type is a categorical variable and cannot be included directly in a regression model. Therefore, dummy variables were created to represent each store type numerically.

The following dummy variables were included:

* **Store_High_Street**
* **Store_Airport**
* **Store_Mall**

Each dummy variable is assigned:

* **1** if the store belongs to that category.
* **0** if the store does not belong to that category.

This allows the model to estimate how each store type differs from the reference store type while keeping all other variables constant.

---

# Reference Category

The omitted store type was used as the **reference category** during dummy variable creation.

All store type coefficients are interpreted relative to this reference category.

**Reference Store Type:** - Residential

---

# Final Model Selected

The **Multiple Linear Regression Model** was selected as the final model for analysis.

---

# Reason for Selecting the Final Model

The multiple regression model was selected because it provides a more complete understanding of the factors associated with monthly sales than the simple regression models.

The model explains approximately **79.98% of the variation in monthly sales (R² = 0.7998)**, indicating strong explanatory power. It simultaneously evaluates the effects of marketing spend, customer footfall, average discount percentage, staff count, and store type, allowing leadership to understand how these factors work together rather than in isolation.

The model also identified several statistically significant business drivers, including marketing spend, footfall, average discount percentage, and store type. These insights make the model more useful for business planning, resource allocation, and strategic decision-making than the simple regression models, which examine only one variable at a time.

Overall, the multiple regression model provides stronger evidence for identifying the key operational factors associated with monthly sales and is therefore the preferred model for supporting management decisions.
