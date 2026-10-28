# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: Carlton Maximus A
RegisterNumber:212225040052
import pandas as pd
import numpy as np 
import matplotlib.pyplot as plt
from sklearn.metrics import mean_absolute_error, mean_squared_error
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
df = pd.read_csv('exp_2_dataset_student_scores.csv')   # CSV should have two columns, e.g. "Hours","Scores"
print("First 5 rows:\n", df.head(), "\n")
print("Last 5 rows:\n", df.tail(), "\n")
X = df.iloc[:, :-1].values   
Y = df.iloc[:, -1].values   
print("X (features):", X.flatten())
print("Y (targets):", Y)
X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size=1/3, random_state=0)
print("\nTraining samples:", len(X_train), " Testing samples:", len(X_test))
regressor = LinearRegression()
regressor.fit(X_train, Y_train)
Y_pred = regressor.predict(X_test)
print("\nPredicted values:", np.round(Y_pred, 2))
print("Actual values   :", Y_test)
plt.figure(figsize=(6,4))
plt.scatter(X_train, Y_train, color="orange", label="Training data")
plt.plot(X_train, regressor.predict(X_train), color="red", label="Fitted line")
plt.title("Hours vs Scores (Training set)")
plt.xlabel("Hours")
plt.ylabel("Scores")
plt.legend()
plt.grid(True)
plt.show()
order = np.argsort(X_test.flatten())
X_test_sorted = X_test.flatten()[order]
Y_test_sorted = Y_test[order]
Y_pred_sorted = Y_pred[order]
plt.figure(figsize=(6,4))
plt.scatter(X_test, Y_test, color="blue", label="Test data")
plt.plot(X_test_sorted, Y_pred_sorted, color="green", label="Predictions")
plt.title("Hours vs Scores (Testing set)")
plt.xlabel("Hours")
plt.ylabel("Scores")
plt.legend()
plt.grid(True)
plt.show()
mae = mean_absolute_error(Y_test, Y_pred)
mse = mean_squared_error(Y_test, Y_pred)
rmse = np.sqrt(mse)
print("\nMean Absolute Error (MAE):", mae)
print("Mean Squared Error (MSE):", mse)
print("Root Mean Squared Error (RMSE):", rmse)
new_hours = np.array([[2.5], [8.0]])  
pred_new = regressor.predict(new_hours)
print("\nPredictions for new hours", new_hours.flatten(), "=>", np.round(pred_new,2))  
*/
```

## Output:
![simple linear regression model for predicting the marks scored](sam.png)
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/35794e8a-682f-4983-94b1-5eb345675885" />
<img width="1026" height="561" alt="image" src="https://github.com/user-attachments/assets/abc1f694-efb7-4334-9e89-eb1f04d0a5aa" />
<img width="820" height="507" alt="image" src="https://github.com/user-attachments/assets/0a5409f1-39ed-4e83-81b8-4b8ac1422064" />
<img width="937" height="517" alt="image" src="https://github.com/user-attachments/assets/0ce564c2-81ba-4c43-9a9f-3ef0908b7934" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b6fc06b0-d87b-40ae-b013-df49a0f05604" />


## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
