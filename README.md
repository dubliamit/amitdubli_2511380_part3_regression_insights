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


Missing Values: 14 missing values were identified in the customer_rating and competitor_distance_km columns. Since both are numerical predictor variables and the proportion of missing data was small, missing values were replaced using the respective column means. No rows were removed because the target variable (monthly_sales) contained no missing values.

