## Dummy Variable Creation

The variables `region` and `store_type` are categorical and cannot be used directly in a linear regression model. Therefore, they were converted into dummy (binary) variables in Excel using IF() formulas.

For the `region` variable, the categories were North, South, East, and West. Three dummy variables (Region_East, Region_South, and Region_West) were created, while North was selected as the reference category.

For the `store_type` variable, the categories were Residential, High Street, Airport and Mall. 3 dummy variables (Store_High_Street, Store_Airport and Store_Mall) were created, while Residential was used as the reference category.

The reference categories were intentionally omitted to avoid the dummy variable trap (perfect multicollinearity), ensuring that the regression model could estimate coefficients correctly.
