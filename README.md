## Goal

Choosing a specific time of the year where it’s typical for customers to be consuming, means you already have an active and engaged market to work with. To help the planning team to allocate marketing budgets based on seasonal patterns (can be seen as a precursor/complimentary approach to MMM)

## Approach

- Exploratory Data Analysis:  Improved the process to make it more organized, comprehensive, and reproducible
- Investigating KPIs: Analyzed and suggested the most suitable KPI for identifying seasonal patterns and relationships between variables
- Feature Selection: Reviewed the list of features, both internal and indicator variables, and tested out approaches for feature selection, which includes Random Forest, TSfresh (Benjamini-Yekutieli procedure), and Principal Component Analysis (PCA)
- Feature Importance: Identified top 30 most important features using the output from Random Forest model
- Multicollinearity: Detected and analyzed highly correlated features with Variance Inflation Factor (VIF) approach
- Modeling: Following modeling approaches were tried out, of which SARIMAX was decided to use finally
    - EWMA
    - XGBoost
    - SARIMAX
- Improving the SARIMAX model: Based on the business objectives/logic, following steps were taken in order to find the most optimal model
    - Built incremental SARIMAX models in conjunction with Random Forest feature importance, of which the best model was selected based on AIC score
    - Manually curated some features from the above best model to improve overall accuracy
    - Tested feature level weights to improve forecasting accuracy
    - Tested within feature weights for seasonal variation (e.g. some months might be more important than others), which leads to better predictions and explainability
    - Tested indicator level variable weights to further adjust seasonal importance


