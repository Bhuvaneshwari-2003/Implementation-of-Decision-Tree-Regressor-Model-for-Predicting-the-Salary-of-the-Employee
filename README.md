# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Import the required libraries.
2.Upload the csv file and read the dataset.
3.Check for any null values using the isnull() function.
4.From sklearn.tree inport DecisionTreeRegressor.
5.Import metrics and calculate the Mean squared error.
6.Apply metrics to the dataset, and predict the output. 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by:bhuvaneshwari.s
RegisterNumber:212221240010  
*/

import pandas as pd
data = pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])
data.head()
x = data[["Position","Level"]]
y = data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_r2:state=2)
from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred = dt.predict(x_test)
from sklearn import metrics
mse = metrics.mean_squared_error(y_test,y_pred)
mse
r2 = metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])

```


## Output:
Data Head:
![169656021-2e081f0d-a5c2-4d2f-b006-f0757dea022d](https://user-images.githubusercontent.com/94828604/175781846-d861431a-ecb4-40a9-bda5-6b3c9fa45be3.png)
Data Info:
![169656031-3d0eda48-b2fe-4e42-92c3-41591af7fdd7](https://user-images.githubusercontent.com/94828604/175781858-49898218-0105-42eb-8f21-6da27d1fb23c.png)
Data Head after applying LabelEncoder():
![169656036-9eed47a3-fdb7-446a-91c4-3f8cd9c2e651](https://user-images.githubusercontent.com/94828604/175781906-3429799b-4797-4a59-9a79-4c0454cd6dae.png)
MSE:
![169656087-043a3571-99ae-4d4c-9942-73fe272df191](https://user-images.githubusercontent.com/94828604/175782030-272ba4e6-df64-48a9-9ad7-db60bb2d0670.png)
r2:
![169656118-b5ab0ed6-be06-43d6-a8d9-21668753e14d](https://user-images.githubusercontent.com/94828604/175782094-c7a79510-b112-469a-b6d8-99833455f8fd.png)
Data Prediction:
![169656131-0f3d0c51-c184-4127-a506-c93361ee4c8d](https://user-images.githubusercontent.com/94828604/175782127-cd530775-7b94-44cd-9eaa-c8e4c045afa4.png)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.


