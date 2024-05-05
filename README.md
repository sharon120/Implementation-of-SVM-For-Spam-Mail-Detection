# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary packages.

2.Read the given csv file and display the few contents of the data.Assign the features for x and y respectively.

3.Split the x and y sets into train and test sets.Convert the Alphabetical data to numeric using CountVectorizer.

4.Predict the number of spam in the data using SVC (C-Support Vector Classification) method of SVM (Support vector machine) in sklearn library.

5.Find the accuracy of the model.
## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Sharon Harshini L M
RegisterNumber: 212223040193

import chardet
file = '/content/spam.csv'
with open(file,'rb') as rawdata:
  result = chardet.detect(rawdata.read(100000))
result

import pandas as pd
data= pd.read_csv("/content/spam.csv",encoding='Windows-1252')

data.head()

data.info()

x=data["v1"].values

y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()

x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
*/
```

## Output:
Result Output:

![327053129-8edf97bf-d362-4e05-a777-2f139b423d46](https://github.com/sharon120/Implementation-of-SVM-For-Spam-Mail-Detection/assets/149555539/26bf789f-37b1-4ef3-9a5c-3c08b1b44b6c)

data.head()

![327053200-dec92239-9bb4-42f5-b85a-a79e602c4f32](https://github.com/sharon120/Implementation-of-SVM-For-Spam-Mail-Detection/assets/149555539/db69f354-6103-42b8-8c6a-15383ab39ecc)

data.info()

![327053262-7b40980c-c631-4fc0-b674-e8bb128cd295](https://github.com/sharon120/Implementation-of-SVM-For-Spam-Mail-Detection/assets/149555539/cdc2c637-a34d-4e30-83f3-4ee9a35ccf36)

data.isnull().sum()

![327053359-b5eb1005-6ecb-46c7-960c-a953b24910fe](https://github.com/sharon120/Implementation-of-SVM-For-Spam-Mail-Detection/assets/149555539/19f6a698-9189-4b65-8261-34234c6e5a56)

Y_Prediction Value

![327053413-4faf2464-134f-4b73-bdd7-37be7eae681e](https://github.com/sharon120/Implementation-of-SVM-For-Spam-Mail-Detection/assets/149555539/d4ae2cdb-e7c9-465a-b2d5-5da1d0295e22)

Accuracy Value

![327053467-fd1b94fe-87de-41cd-a89e-4ca47b865cd8](https://github.com/sharon120/Implementation-of-SVM-For-Spam-Mail-Detection/assets/149555539/081e0a85-d0c1-4e4e-971d-acd39a16b7e7)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
