# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.  Import pandas
2. Import Decision tree classifier
3. Fit the data in the model
4. Find the accuracy score


## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: 212225220035
RegisterNumber:  R.Gokulavani
import pandas as pd
data=pd.read_csv("Employee (1).csv")
print("data.head():")
data.head()
print("data.info():")
data.info()
print("isnull() and sum():")
data.isnull().sum()
print("data value counts():")
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
print("data.head() for Salary:")
data["salary"]=le.fit_transform(data["salary"])
data.head()
print("x.head():")
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident"]] 
x.head()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
print("Accuracy value:")
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
print("Data Prediction:")
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
from sklearn.tree import plot_tree
import matplotlib.pyplot as plt
plt.figure(figsize=(8,6))
plot_tree(dt, feature_names=x.columns, class_names=['salary', 'left'], filled=True)
plt.show()
*/
```

## Output:
<img width="1435" height="263" alt="image" src="https://github.com/user-attachments/assets/3417be0f-a707-4548-8348-411fa9253195" />
<img width="756" height="385" alt="image" src="https://github.com/user-attachments/assets/da8888c1-faed-4628-944e-f9b975e6e818" />
<img width="688" height="280" alt="image" src="https://github.com/user-attachments/assets/346eb702-d05a-4967-8f2a-8d8f568c8256" />
<img width="577" height="123" alt="image" src="https://github.com/user-attachments/assets/8b8fa2f2-c6e7-4190-a334-c25ba7b6b88e" />
<img width="1427" height="286" alt="image" src="https://github.com/user-attachments/assets/c19bc5db-81f8-44ea-bc43-4dc55d365464" />
<img width="1025" height="262" alt="image" src="https://github.com/user-attachments/assets/0eac75d5-c811-4941-adb9-d7a942626e10" />
<img width="401" height="65" alt="image" src="https://github.com/user-attachments/assets/559fada3-2237-4fdb-85aa-1b0a8d658606" />
<img width="958" height="587" alt="image" src="https://github.com/user-attachments/assets/354bff20-7677-4fd1-b043-5a17b644235e" />



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
