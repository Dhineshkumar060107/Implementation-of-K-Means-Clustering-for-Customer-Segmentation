# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import dataset and print head,info of the dataset  
2.check for null values   
3.Import kmeans and fit it to the dataset    
4.Plot the graph using elbow method    
5.Print the predicted array    
6.Plot the customer segments  

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by:Dhineshkumar.L
RegisterNumber:212224230066

import pandas as pd

import matplotlib.pyplot as plt

data=pd.read_csv("/content/Mall_Customers (1).csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans

wcss=[]

for i in range(1,11):

kmeans=KMeans(n_clusters=i,init="k-means++")

kmeans.fit(data.iloc[:,3:])

wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)

plt.xlabel("No_of_Clusters")

plt.ylabel("wcss")

plt.title("Elbow Method")

km=KMeans(n_clusters=5)

km.fit(data.iloc[:,3:])

y_pred=km.predict(data.iloc[:,3:])

y_pred

data["cluster"]=y_pred

df0=data[data["cluster"]==0]

df1=data[data["cluster"]==1]

df2=data[data["cluster"]==2]

df3=data[data["cluster"]==3]

df4=data[data["cluster"]==4]

plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")

plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")

plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")

plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")

plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")

plt.legend()

plt.title("Customer Segment")
*/
```

## Output:
### 1.DATA.HEAD():

<img width="653" height="247" alt="ml101" src="https://github.com/user-attachments/assets/38a2b3df-6ec6-44cc-9473-b39e4dc99bcd" />


### 2.DATA.INF0():

<img width="522" height="263" alt="ml102" src="https://github.com/user-attachments/assets/04ef251b-84ad-4ec1-a6b7-4545bbaaa167" />


### 3.DATA.ISNULL().SUM():

<img width="291" height="150" alt="103" src="https://github.com/user-attachments/assets/89334a10-7823-482b-bd07-a100e4e9d3fe" />


### 4.PLOT USING ELBOW METHOD:

<img width="877" height="613" alt="ml104" src="https://github.com/user-attachments/assets/e6bbabc3-aff9-48b3-a52f-c75196a74eb4" />


### 5.K-MEANS CLUSTERING:

<img width="252" height="91" alt="ml105" src="https://github.com/user-attachments/assets/ae66e730-b1e4-485f-a458-3defa507e9b8" />


### 6.Y_PRED ARRAY:

<img width="752" height="226" alt="106" src="https://github.com/user-attachments/assets/db0e347d-662f-4a11-bfaa-3519a600c5c7" />


### 7.CUSTOMER SEGMENT:

<img width="740" height="555" alt="107" src="https://github.com/user-attachments/assets/d50db9e4-84a0-49a0-a0e6-dc0a1144408f" />


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
