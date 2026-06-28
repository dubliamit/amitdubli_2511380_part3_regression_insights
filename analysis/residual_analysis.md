
# Residual Analysis

## Method

Predicted monthly sales were calculated using the final multiple regression model. Residuals were computed as:

Residual = Actual Monthly Sales − Predicted Monthly Sales

Positive residuals indicate that the model under-predicted sales, while negative residuals indicate that the model over-predicted sales.

## Largest Positive Residuals

The following records had the largest positive residuals:

*  | store_id	|  monthly_sales	|  Predictive sales	 |   Residual   |
*  | STR-1075	|    763162.45	  |     657721.1622	   |  105441.2878 |
*  | STR-1028	|    713611.16	  |     608976.3466	   |  104634.8134 |
*  | STR-1026	|    625514.04	  |     523933.4838	   |  101580.5562 |
*  | STR-1027	|    795153.84	  |     696706.0486	   |  98447.79135 |
*  | STR-1019	|    788087.68	  |     691778.4456	   |  96309.23444 |

## Top 5 Largest Positive Residuals

| Store ID | Actual Sales | Predicted Sales | Residual |
|-----------|-------------:|----------------:|----------:|
| STR-1075 | 763,162.45 | 657,721.16 | 105,441.29 |
| STR-1028 | 713,611.16 | 608,976.35 | 104,634.81 |
| STR-1026 | 625,514.04 | 523,933.48 | 101,580.56 |
| STR-1027 | 795,153.84 | 696,706.05 | 98,447.79 |
| STR-1019 | 788,087.68 | 691,778.45 | 96,309.23 |


These stores performed substantially better than expected. Possible reasons include successful local promotions, strong customer loyalty, or other factors not included in the model.

## Largest Negative Residuals

The following records had the largest negative residuals:

| store_id	|  monthly_sales	|  Predictive sales  |	  Residual   |
| STR-1012	|    595467.6	    |    722352.8882	   |  -126885.2882 |
| STR-1023	|    627171.9	    |    750504.7605	   |  -123332.8605 |
| STR-1017	|    685379.08	  |    807534.2692	   |  -122155.1892 |
| STR-1009	|    641865.03	  |    752440.7681	   |  -110575.7381 |
| STR-1001	|    658920.3	    |    763718.1178	   |  -104797.8178 |


These stores performed worse than expected. Possible reasons include operational issues, local competition, stock shortages, or other external influences not captured by the model.

## Business Interpretation

The residual analysis indicates that although the regression model explains a large proportion of the variation in monthly sales, some stores still show substantial prediction errors. This suggests that additional variables—such as local market conditions, competitor promotions, seasonal events, or store-specific operational factors—may improve the model's predictive performance.

Overall, the residuals do not indicate a consistent pattern of over-prediction or under-prediction across all stores, although certain store types may warrant further investigation if they appear repeatedly among the largest residuals.
