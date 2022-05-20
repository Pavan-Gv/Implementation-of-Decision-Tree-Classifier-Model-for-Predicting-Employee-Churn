# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```python
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: G Venkata Pavan Kumar
RegisterNumber: 212221240013
*/
import pandas as pd
data = pd.read_csv("Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le =LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_monthly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=decisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```

## Output:
![ML1](https://user-images.githubusercontent.com/94827772/169458821-c2c6ad05-614e-421a-b139-061897a7df2a.png)
</br>
![ML2](https://user-images.githubusercontent.com/94827772/169458818-678e6f7e-1b59-4fbc-b504-0a78e8de4181.png)
</br>
![ML3](https://user-images.githubusercontent.com/94827772/169458812-1f76f1b2-2670-4262-b6bc-b786750fc320.png)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
