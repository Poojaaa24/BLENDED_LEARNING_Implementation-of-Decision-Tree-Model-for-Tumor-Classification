# BLENDED_LEARNING
# Implementation of Decision Tree Model for Tumor Classification

## AIM:
To implement and evaluate a Decision Tree model to classify tumors as benign or malignant using a dataset of lab test results.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required Python libraries and load the tumor dataset.

2. Select the feature columns and target column from the dataset.

3. Split the dataset into training and testing sets and train the Decision Tree model.

4. Predict the test data and evaluate the model using accuracy and a confusion matrix.  

## Program:
```
/*
Program to  implement a Decision Tree model for tumor classification.
Developed by: POOJA U
RegisterNumber:  212225230209
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import accuracy_score, classification_report,confusion_matrix
data=pd.read_csv('tumor.csv')
print(data.head())
print(data.columns)
features=['Clump','UnifSize','UnifShape','MargAdh','SingEpiSize','BareNuc','BlandChrom']
target='Class'
X=data[features]
y=data[target]
X_train,X_test,y_train,y_test=train_test_split(X,y,test_size=0.3,random_state=42)
model=DecisionTreeClassifier()
model.fit(X_train,y_train)
y_pred=model.predict(X_test)
accuracy=accuracy_score(y_test,y_pred)
print("AcurracyScore:",accuracy)
cm=confusion_matrix(y_test,y_pred)
sns.heatmap(cm,annot=True,fmt="d",cmap="Blues")
plt.title("Confusion Matrix")
plt.xlabel("Predicted")
plt.ylabel("Actual")
plt.show()
*/
```

## Output:
<img width="1266" height="394" alt="Screenshot 2026-03-11 123306" src="https://github.com/user-attachments/assets/e21d010b-dafb-46c8-a594-391bb28a8f6c" />
<img width="1374" height="136" alt="Screenshot 2026-03-11 123318" src="https://github.com/user-attachments/assets/cb3b1781-a6bf-4608-83d2-480def905c71" />

<img width="1254" height="760" alt="Screenshot 2026-03-11 123330" src="https://github.com/user-attachments/assets/ff82c1ed-782f-4962-be7f-72f95f1157e9" />


## Result:
Thus, the Decision Tree model was successfully implemented to classify tumors as benign or malignant, and the model’s performance was evaluated.
