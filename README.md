# Ex-03EDA

## AIM
To perform EDA on the given data set. 

# Explanation
The primary aim with exploratory analysis is to examine the data for distribution, outliers and 
anomalies to direct specific testing of your hypothesis.
 

# ALGORITHM
### STEP 1

### STEP 2

### STEP 3

### STEP 4



# CODE:

import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("titanic_dataset.csv")
df.info()
df.head()
df.isnull().sum()
df["Age"]=df["Age"].fillna(df["Age"].median())
df.boxplot()
df.isnull()
df["Embarked"]=df["Embarked"].fillna(df["Embarked"].mode()[0])
df["Embarked"].value_counts()
df["Pclass"].value_counts()
df["Survived"].value_counts()
sns.countplot(x="Survived",data=df)
sns.countplot(x="Pclass",data=df)
df.info()
sns.displot(df["Fare"])
sns.countplot(x="Pclass",hue="Survived",data=df)
sns.countplot(x="Sex",hue="Survived",data=df)
sns.displot(df[df["Survived"]==0]["Age"])
sns.displot(df[df["Survived"]==1]["Age"])
pd.crosstab(df["Pclass"],df["Survived"])
pd.crosstab(df["Sex"],df["Survived"])
df.corr()
sns.heatmap(df.corr(),annot=True)

# OUTPUT:
![1](https://user-images.githubusercontent.com/94169318/162114883-7a5bb328-a60e-498f-9e44-0c699c7511c9.jpg)
![2](https://user-images.githubusercontent.com/94169318/162114900-7ff01a17-5bd6-4ff2-b576-570d9abfa011.jpg)
![3](https://user-images.githubusercontent.com/94169318/162114925-1137e093-9ea5-455c-9e7c-a30d2574ac64.jpg)
![4](https://user-images.githubusercontent.com/94169318/162114993-b3b7dc8e-18ac-43d0-a524-3fabfdc3ffb3.jpg)
![5](https://user-images.githubusercontent.com/94169318/162115007-7be07f90-ddc6-40e2-9eda-729aa9a840cd.jpg)
![6](https://user-images.githubusercontent.com/94169318/162115023-c4cae850-1e69-465c-8deb-81412c4ee77f.jpg)
![7](https://user-images.githubusercontent.com/94169318/162115042-59936845-2b7c-4fbe-832d-0373d27ed836.jpg)
![8](https://user-images.githubusercontent.com/94169318/162115056-f18cb4d0-18c9-4f34-850f-df88d15e7020.jpg)
![9](https://user-images.githubusercontent.com/94169318/162115065-e725d2c3-fe31-4163-bf40-1b0e5219db2e.jpg)
![10](https://user-images.githubusercontent.com/94169318/162115080-aae768be-f949-4497-9ef1-dbb1210ffec7.jpg)
![11](https://user-images.githubusercontent.com/94169318/162115103-af6f82c9-97b2-44fa-926c-85e33a7d7f36.jpg)
![12](https://user-images.githubusercontent.com/94169318/162115116-3978bb4b-4148-4805-86fd-87d050718475.jpg)
![13](https://user-images.githubusercontent.com/94169318/162115129-bb9d5342-db68-4342-a8a2-6c651a4d0a01.jpg)
![14](https://user-images.githubusercontent.com/94169318/162115147-d5e162cd-0487-4afc-8912-1c7cd832aa37.jpg)
![15](https://user-images.githubusercontent.com/94169318/162115172-181c42e2-2432-4a83-904f-dc0c25ca9485.jpg)
![16](https://user-images.githubusercontent.com/94169318/162115183-3de20650-af3d-48d7-a75b-9c4c1d47d2a4.jpg)


