# BLENDED_LEARNING
# Implementation of Decision Tree Model for Tumor Classification

## AIM:
To implement and evaluate a Decision Tree model to classify tumors as benign or malignant using a dataset of lab test results.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. Start the program.
2. Import the required Python libraries such as pandas, sklearn, seaborn, and matplotlib.
3. Load the tumor dataset using read_csv() into a dataframe.
4. Separate the dataset into input features (X) and target variable (Class).
5. Split the dataset into training and testing sets using train_test_split().
6. Create a Decision Tree Classifier model.
7. Train the model using the training data (model.fit).
8. Predict the tumor class for the test data using model.predict().
9. Evaluate the model using accuracy score, classification report, and confusion matrix.
10. Display the results and visualize the confusion matrix, then stop the program.

## Program:
```
/*
Program to  implement a Decision Tree model for tumor classification.
Developed by: Lohith V
RegisterNumber: 25013313

import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix
data=pd.read_csv('tumor.csv')
print(data.head())
print(data.columns)
X=data.drop(columns=['Class'])
y=data['Class']
X_train,X_test,y_train,y_test=train_test_split(X,y,test_size=0.3,random_state=42)
model=DecisionTreeClassifier()
model.fit(X_train,y_train)
y_pred=model.predict(X_test)
accuracy=accuracy_score(y_test,y_pred)
print("Name: Lohith V")
print("Register Number: 25013313")
print("Accuracy:",accuracy)
print("Classification Report:\n",classification_report(y_test,y_pred))
conf_matrix=confusion_matrix(y_test,y_pred)
sns.heatmap(conf_matrix,annot=True,fmt="d",cmap="Blues")
plt.xlabel("Predicted")
plt.ylabel("Actual")
plt.title("Confusion Matrix")
plt.show()

*/
```

## Output:
![alt text](<Screenshot 2026-03-24 091846.png>)


![alt text](<Screenshot 2026-03-24 091853.png>)


![alt text](<Screenshot 2026-03-24 091905.png>)

## Result:
Thus, the Decision Tree model was successfully implemented to classify tumors as benign or malignant, and the model’s performance was evaluated.
