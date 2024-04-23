# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn->

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm :
1.Import pandas module and import the required data set.
2.Find the null values and count them.

3.Count number of left values.

4.From sklearn import LabelEncoder to convert string values to numerical values.

5.From sklearn.model_selection import train_test_split.

6.Assign the train dataset and test dataset.

7.From sklearn.tree import DecisionTreeClassifier.

8.Use criteria as entropy.

9.From sklearn import metrics. 10.Find the accuracy of our model and predict the require values.

## Program:
```
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: sanjay m
RegisterNumber:  212222110038

->
import pandas as pd
data=pd.read_csv("/content/Employee.csv")

data.head()

data.info()

data.isnull().sum()

data["left"].value_counts()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()

data["salary"]=le.fit_transform(data["salary"])
data.head()


x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()

y=data["left"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)

from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
accuracy= metrics.accuracy_score(y_test,y_pred)
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]])

```

## Output:
### data.head()

![image](https://github.com/Pradeeppachiyappan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118707347/e8da4b95-d0b5-436d-a35b-91f2e504ca1b)

### data.info()

![image](https://github.com/Pradeeppachiyappan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118707347/14d2f18c-0948-41d5-bd27-22c93074bed2)

### isnull() and sum()

![image](https://github.com/Pradeeppachiyappan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118707347/f31626db-628d-4019-8ac4-f09b4b3d932a)

### data value counts()

![image](https://github.com/Pradeeppachiyappan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118707347/30be4c48-a71d-42ce-8584-38d9a1829c09)

### data head() for salary

![image](https://github.com/Pradeeppachiyappan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118707347/b4b2cf26-7169-4412-9c0b-69f359d2ea37)

### x.head()

![image](https://github.com/Pradeeppachiyappan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118707347/c202755f-1aa3-4100-b5bf-e40987fafc9d)

### accuracy value

![image](https://github.com/Pradeeppachiyappan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118707347/69ac7139-f3c7-48e0-9557-d2ebf5919af3)

### data prediction

![image](https://github.com/Pradeeppachiyappan/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118707347/f4d7648b-8d52-4ce3-810d-c04fee575682)


## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
