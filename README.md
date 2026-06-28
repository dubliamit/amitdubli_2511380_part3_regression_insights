# amitdubli_2511380_part3_regression_insights
Part 3: Regression-Based Business Insights &amp; Model Interpretation

# Task 1: Understanding the Dataset

## Business Problem

The objective of this project is to identify the factors that influence **monthly sales** across retail stores using multiple linear regression. The insights will help management make data-driven decisions regarding marketing, inventory management, staffing, discount strategies, and store operations.

## Dataset Description

The dataset contains monthly operational and sales information for multiple retail stores. Each record represents one store's performance for a specific month.

| Variable                   | Description                                           | Type                   |
| -------------------------- | ----------------------------------------------------- | ---------------------- |
| store_id                   | Unique identifier for each store                      | Identifier             |
| month                      | Month of observation                                  | Date/Time              |
| region                     | Geographic region of the store                        | Categorical            |
| store_type                 | Type of retail store                                  | Categorical            |
| marketing_spend            | Monthly marketing expenditure                         | Numerical              |
| footfall                   | Number of customers visiting the store                | Numerical              |
| avg_discount_pct           | Average discount offered (%)                          | Numerical              |
| staff_count                | Number of employees in the store                      | Numerical              |
| inventory_availability_pct | Percentage of inventory available                     | Numerical              |
| competitor_distance_km     | Distance to the nearest competitor (km)               | Numerical              |
| holiday_flag               | Indicates whether the month includes a holiday season | Categorical (Binary)   |
| customer_rating            | Average customer satisfaction rating                  | Numerical              |
| monthly_sales              | Total monthly sales revenue                           | **Dependent Variable** |
| monthly_profit             | Monthly profit generated                              | Numerical              |

---

## Dependent Variable (Target)

The regression model aims to predict:

* **monthly_sales**

This is the response variable that represents the monthly sales performance of each retail store.

---

## Potential Independent Variables

The following variables are considered potential predictors of monthly sales:

* marketing_spend
* footfall
* avg_discount_pct
* staff_count
* inventory_availability_pct
* competitor_distance_km
* customer_rating
* region
* store_type
* holiday_flag

These variables represent operational, customer, and environmental factors that may influence sales performance.

---

## Numerical Variables

The dataset contains the following numerical variables:

* marketing_spend
* footfall
* avg_discount_pct
* staff_count
* inventory_availability_pct
* competitor_distance_km
* customer_rating
* monthly_sales
* monthly_profit

---

## Categorical Variables

The categorical variables are:

* region
* store_type
* holiday_flag

These variables will require encoding before regression analysis.

---

## Variables Requiring Cleaning or Transformation

Several variables may require preprocessing before model building:

| Variable            | Required Transformation                                      |
| ------------------- | ------------------------------------------------------------ |
| month               | Convert to datetime format if needed for time-based analysis |
| region              | One-Hot Encoding                                             |
| store_type          | One-Hot Encoding                                             |
| holiday_flag        | Convert Yes/No to 1/0 or One-Hot Encode                      |
| Numerical variables | Check for missing values, outliers, and scaling if required  |

Additional preprocessing steps include:

* Handling missing values as in our case for competitor_distance_km and customer_rating
* Removing duplicate records but there are no duplicates in our case
* Verifying data types
* Detecting outliers

---

## Variables Not Useful for Regression

The following variables are not suitable as predictors:

| Variable           | Reason                                                                                                                   |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| store_id           | Unique identifier with no predictive value                                                                               |
| monthly_profit     | Excluded to avoid data leakage since profit is directly related to sales                                                 |

---

## Expected Relationship with Monthly Sales

The following hypotheses will be tested during regression analysis:

* Higher marketing spend is expected to increase sales.
* Greater customer footfall should positively influence sales.
* Higher inventory availability should improve sales performance.
* Customer ratings may positively impact repeat purchases and sales.
* Holiday periods are expected to generate higher sales.
* Appropriate discount strategies may increase sales volume.
* Store type and region may explain differences in store performance.
* Greater competitor distance may reduce competitive pressure and increase sales.

---

This understanding of the dataset provides the foundation for data cleaning, exploratory analysis, feature engineering, and multiple linear regression to identify the key drivers of monthly sales.

Below is a README section tailored to your project and consistent with the work you've completed.

---

# Regression Approach

Regression analysis was performed to identify the factors associated with monthly sales across retail stores. The analysis began with simple linear regression models to evaluate the relationship between monthly sales and individual variables such as marketing spend and footfall. A multiple linear regression model was then developed by combining several business variables, including marketing spend, footfall, average discount percentage, staff count, and store type dummy variables. The final model was evaluated using R-squared, adjusted R-squared, p-values, and coefficient interpretation to determine the most important drivers of sales.

---

# Dummy Variable Approach

The dataset contained categorical variables that required numerical encoding before they could be included in the regression model.

* **Store Type** was converted into dummy variables:

  * Store_High_Street
  * Store_Airport
  * Store_Mall

The omitted store type was used as the **reference category (Residential)**, and all dummy variable coefficients were interpreted relative to this category.

The **holiday_flag** variable was already coded as **0 (Non-Holiday)** and **1 (Holiday)**, so it was already in binary format and did not require additional dummy variable creation.

---

# Model Comparison Summary

Two simple regression models and one multiple regression model were developed and compared.

* The simple regression models showed the individual impact of marketing spend and footfall on monthly sales.
* The multiple regression model combined several predictors and provided a more comprehensive understanding of sales performance.
* The final multiple regression model achieved an **R-squared of 0.7998**, meaning it explained approximately **80% of the variation in monthly sales**, which was higher than the simple regression models.
* The multiple regression model also identified several statistically significant predictors, making it more useful for business decision-making.

---

# Final Model Selected

The **Multiple Linear Regression Model** was selected as the final model because it provided the strongest explanatory power and evaluated multiple business factors simultaneously.

The model included:

* Marketing Spend
* Footfall
* Average Discount Percentage
* Staff Count
* Store Type (Dummy Variables)

The model achieved:

* **R² = 0.7998**
* **Adjusted R² = 0.7953**

These results indicate that the model explains approximately **80% of the variation in monthly sales**, making it suitable for identifying key business drivers.

---

# Business Recommendation

Based on the regression analysis, leadership should focus on the variables that showed significant relationships with monthly sales.

* Increase investment in marketing activities that effectively attract customers.
* Implement initiatives to increase customer footfall, as it was one of the strongest positive predictors of sales.
* Review discount strategies carefully, since higher average discount percentages were associated with lower monthly sales in the final model.
* Prioritize investment in high-performing store types such as Airport and Mall stores.
* Continue monitoring business performance and update the model periodically as new data becomes available.

---

# Assumptions and Limitations

### Assumptions

* A linear relationship exists between the independent variables and monthly sales.
* Observations are independent of one another.
* The data used is accurate, complete, and representative of normal business operations.
* The selected variables capture the primary factors influencing monthly sales.

### Limitations

* Regression identifies **associations**, not cause-and-effect relationships.
* Approximately **20% of the variation in monthly sales** remains unexplained, suggesting that additional factors such as seasonality, local competition, customer demographics, weather, or economic conditions may also influence sales.
* The analysis is based on historical data and may not fully predict future performance.
* Results may change if new variables or additional data are included.

---

# Screenshots Included

The following screenshots are included as evidence of the analysis:

* simple_regression_output
* multiple_regression_output
* model_comparison_preview
* residuals_preview

These screenshots document the regression outputs, model comparison, and residual analysis completed during the project.



**Missing Values:** 14 missing values were identified in the customer_rating and competitor_distance_km columns. Since both are numerical predictor variables and the proportion of missing data was small, missing values were replaced using the respective column means. No rows were removed because the target variable (monthly_sales) contained no missing values.


**Business Conclusion for Multiple Regression Task**

* **Marketing spend** has a significant positive effect on monthly sales, suggesting that increased marketing investment can help drive revenue.
* **Footfall** is the strongest numerical predictor of sales, indicating that attracting more customers should be a key business priority.
* **Average discount percentage** has a significant negative relationship with sales, suggesting that excessive discounting may reduce overall sales revenue or reflect weaker-performing periods.
* **Store type** significantly influences sales. Airport and Mall stores outperform the reference store type, indicating that store location and format play an important role in sales performance.
* **Staff count** does not have a statistically significant impact in this model and may require further investigation.

