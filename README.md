# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required packages and print the present data.

2.Print the placement data and salary data.

3.Find the null and duplicate values.

4.Using logistic regression find the predicted values of accuracy , confusion matrices.

5.Display the results.

## Program:
```python
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: VARUN J  C
RegisterNumber:  212224240179
import pandas as pd 
data = pd.read_csv('Placement_Data.csv')
data.head()
data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis = 1)
data.head()
data1.isnull().sum()
data1.duplicated().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1["gender"]=le.fit_transform(data1["gender"])
data1["ssc_b"]=le.fit_transform(data1["ssc_b"])
data1["hsc_b"]=le.fit_transform(data1["hsc_b"])
data1["hsc_s"]=le.fit_transform(data1["hsc_s"])
data1["degree_t"]=le.fit_transform(data1["degree_t"])
data1["workex"]=le.fit_transform(data1["workex"])
data1["specialisation"]=le.fit_transform(data1["specialisation"] )     
data1["status"]=le.fit_transform(data1["status"])
data1 
x=data1.iloc[:,:-1]
x
y=data1["status"]
y
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size = 0.2,random_state = 0)
from sklearn.linear_model import LogisticRegression
lr = LogisticRegression(solver = "liblinear") 
lr.fit(x_train,y_train)
y_pred = lr.predict(x_test)
y_pred
from sklearn.metrics import accuracy_score
accuracy = accuracy_score(y_test,y_pred)
accuracy
from sklearn.metrics import confusion_matrix
confusion = (y_test,y_pred)
confusion
from sklearn.metrics import classification_report
classification_report1 = classification_report(y_test,y_pred)
print(classification_report1)
lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]]) 
*/
```

## Output:
HEAD:
![Screenshot 2025-04-14 115658](https://github.com/user-attachments/assets/50986d78-afec-49e7-a387-39383911fa25)
COPY:
![Screenshot 2025-04-14 115710](https://github.com/user-attachments/assets/f4512cf9-49b8-41a2-8702-f0f8faa11602)
FIT TRANSFORM:
![Screenshot 2025-04-14 115730](https://github.com/user-attachments/assets/ad165f59-c708-442f-af77-a4d1b1ae2b87)
LOGISTIC REGRESSION:
![Screenshot 2025-04-14 115745](https://github.com/user-attachments/assets/cc817905-d58d-491c-967c-a3136eaab879)

ACCURACY SCORE:

![Screenshot 2025-04-14 115806](https://github.com/user-attachments/assets/1f952cdb-5805-46ae-8ed9-901ca393e5da)

MATRIX:

![Screenshot 2025-04-14 115828](https://github.com/user-attachments/assets/43100d1a-e880-453b-870d-1b2f9656ad11)

![Screenshot 2025-04-14 115840](https://github.com/user-attachments/assets/5a291eb6-5301-4d25-9bd8-7e0fb82aa3fb)

CLASSIFICATION REPORT: 
![Screenshot 2025-04-14 115850](https://github.com/user-attachments/assets/d2d58b51-f9c4-4bad-88f4-2ba6f25ec6ce)
PREDICTION:
![Screenshot 2025-04-14 120101](https://github.com/user-attachments/assets/9359ed8a-dce2-4d91-b1f9-20d4b4665332)


## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
