# Deamnd Forecasting Hacakthon analytics Vidhya


##  Problem statement
One of the largest retail chains in the world wants to use their vast data source to build an efficient forecasting model 
to predict the sales for each SKU in its portfolio at its 76 different stores using historical sales data for the past 
3 years on a week-on-week basis. Sales and promotional information is also available for each week - product and store wise. 
We are trying to forecast the sales values for every such product/SKU-store combination for the next 12 weeks.
We are predicting units_sold which is the target variable

## Correlation matrix
![alt text](https://github.com/SHINE1607/demand_forecasting/blob/master/images/correlation_heatmap.png)

## Feature Importance
below image shows the faetures witth most imaportance in the prediction
![alt text](https://github.com/SHINE1607/demand_forecasting/blob/master/images/feature_importance.png)


## Model Used and Approach

### Random forest Regression
* The model is using tuned using randomized search CV library 
* The best paramters are
{'n_estimators': 700,
  'min_samples_split': 15,
  'min_samples_leaf': 1,
  'max_features': 'auto',
  'max_depth': 20}
 * the mae score obatained using the above model is **920.9326941229832**
 
 ### XGBRegressor
 * The model is trained using arbndomized search CV
 * the best parameterts obtaiend are:
 {'colsample_bytree': 0.8,
  'learning_rate': 0.05,
  'max_depth': 7,
  'min_child_weight': 4,
  'n_estimators': 1000,
  'nthread': 4,
  'objective': 'reg:linear',
  'silent': 1,
  'subsample': 0.7}
  * The mae score obtained for the validation data is **697.3051615051615**
  
  The final model used XGBRegresor and score for final prediction was 477.8929651611 which placed me 77 out of 262 partciplants, i know, not the best!!

