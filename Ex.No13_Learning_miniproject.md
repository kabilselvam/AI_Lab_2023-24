# Ex.No: 13  Stock Market predection
### DATE:  13/05/25                                                                   
### REGISTER NUMBER : 212222040067
### AIM: 
To develop a stock market prediction model using Random Forest and XGBoost algorithms
###  Algorithm:
Step 1:  Start the program.<br>
Step 2 : Import required packages.<br>
Step 3:  Load and preprocess historical stock data.<br>
Step 4:  Split the dataset into training and testing sets, and normalize if needed. <br>
Step 5:  Train the models using Random Forest and XGBoost on training data.<br>
Step 6:  Predict the stock prices or movement using the trained models on test data.<br>
Step 7:  Combine model predictions using averaging or voting strategy.<br>
Step 8:  Print the final prediction and optionally visualize the results.<br>
Step 9:  Stop the program.
### Program:
```
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error

lr = LinearRegression()
lr.fit(X_train, y_train)
pred_lr = lr.predict(X_test)

print("Linear Regression MSE:", mean_squared_error(y_test, pred_lr))

from sklearn.ensemble import RandomForestRegressor

rf = RandomForestRegressor(n_estimators=100, random_state=42)
rf.fit(X_train, y_train)
pred_rf = rf.predict(X_test)

print("Random Forest MSE:", mean_squared_error(y_test, pred_rf))

import xgboost as xgb

xg = xgb.XGBRegressor(objective='reg:squarederror', n_estimators=100)
xg.fit(X_train, y_train)
pred_xg = xg.predict(X_test)

print("XGBoost MSE:", mean_squared_error(y_test, pred_xg))

import matplotlib.pyplot as plt

plt.figure(figsize=(14,6))
plt.plot(y_test.values, label='Actual')
plt.plot(pred_rf, label='Random Forest Prediction')
plt.plot(pred_xg, label='XGBoost Prediction')
plt.legend()
plt.title("Stock Price Prediction")
plt.xlabel("Days")
plt.ylabel("Price")
plt.show()

```
### Output/Plan:
![kfhdfjl](https://github.com/user-attachments/assets/8b9c4458-5438-4c6f-a8a7-144302223f48)


### Result:
The stock market prediction model was successfully implemented using Random Forest and XGBoost algorithms.
