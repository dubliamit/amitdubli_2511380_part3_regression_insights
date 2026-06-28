
# Residual Analysis

## Method

Predicted monthly sales were calculated using the final multiple regression model. Residuals were computed as:

Residual = Actual Monthly Sales − Predicted Monthly Sales

Positive residuals indicate that the model under-predicted sales, while negative residuals indicate that the model over-predicted sales.

## Top 5 Largest Positive Residuals

| Store ID | Actual Sales | Predicted Sales | Residual |
|-----------|-------------:|----------------:|----------:|
| STR-1075 | 763,162.45 | 657,721.16 | 105,441.29 |
| STR-1028 | 713,611.16 | 608,976.35 | 104,634.81 |
| STR-1026 | 625,514.04 | 523,933.48 | 101,580.56 |
| STR-1027 | 795,153.84 | 696,706.05 | 98,447.79 |
| STR-1019 | 788,087.68 | 691,778.45 | 96,309.23 |

These stores performed substantially better than expected. Possible reasons include successful local promotions, strong customer loyalty, or other factors not included in the model.

## Top 5 Largest Negative Residuals

| Store ID | Actual Sales | Predicted Sales | Residual |
|-----------|-------------:|----------------:|----------:|
| STR-1012 | 595,467.60 | 722,352.89 | -126,885.29 |
| STR-1023 | 627,171.90 | 750,504.76 | -123,332.86 |
| STR-1017 | 685,379.08 | 807,534.27 | -122,155.19 |
| STR-1009 | 641,865.03 | 752,440.77 | -110,575.74 |
| STR-1001 | 658,920.30 | 763,718.12 | -104,797.82 |

These stores performed worse than expected. Possible reasons include operational issues, local competition, stock shortages, or other external influences not captured by the model.

## Business Interpretation

The residual analysis indicates that although the regression model explains a large proportion of the variation in monthly sales, some stores still show substantial prediction errors. This suggests that additional variables—such as local market conditions, competitor promotions, seasonal events, or store-specific operational factors—may improve the model's predictive performance.

Overall, the residuals do not indicate a consistent pattern of over-prediction or under-prediction across all stores, although certain store types may warrant further investigation if they appear repeatedly among the largest residuals.
