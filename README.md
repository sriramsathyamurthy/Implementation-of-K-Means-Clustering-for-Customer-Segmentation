# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Choose the number of clusters (K).

2.Randomly initialize K centroids.

3.Assign each data point to the nearest centroid.

4.Recalculate the centroids.

5.Repeat steps 3 and 4 until centroids do not change
## Program:
```
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
data = pd.read_csv("Mail_Customers.csv")
X = data[['Annual Income (k$)', 'Spending Score (1-100)']]
print(data.head())
kmeans = KMeans(n_clusters=5, random_state=42)
y_kmeans = kmeans.fit_predict(X)


data['Cluster'] = y_kmeans

print("\nClustered Data:")
print(data.head())


plt.figure()
plt.scatter(X[y_kmeans == 0]['Annual Income (k$)'], 
            X[y_kmeans == 0]['Spending Score (1-100)'], label='Cluster 0')

plt.scatter(X[y_kmeans == 1]['Annual Income (k$)'], 
            X[y_kmeans == 1]['Spending Score (1-100)'], label='Cluster 1')

plt.scatter(X[y_kmeans == 2]['Annual Income (k$)'], 
            X[y_kmeans == 2]['Spending Score (1-100)'], label='Cluster 2')

plt.scatter(X[y_kmeans == 3]['Annual Income (k$)'], 
            X[y_kmeans == 3]['Spending Score (1-100)'], label='Cluster 3')

plt.scatter(X[y_kmeans == 4]['Annual Income (k$)'], 
            X[y_kmeans == 4]['Spending Score (1-100)'], label='Cluster 4')

# Plot centroids
plt.scatter(kmeans.cluster_centers_[:,0], 
            kmeans.cluster_centers_[:,1], 
            s=200, label='Centroids')

plt.title("Customer Segmentation using K-Means")
plt.xlabel("Annual Income (k$)")
plt.ylabel("Spending Score (1-100)")
plt.legend()
plt.show()

/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: SRIRAM S
RegisterNumber:  212225240155
*/
```

## Output:
![WhatsApp Image 2026-03-16 at 10 12 34 AM](https://github.com/user-attachments/assets/94ab3396-c5c4-404c-868c-2a5f3502a75f)
<img width="879" height="337" alt="image" src="https://github.com/user-attachments/assets/150b8a0d-fe2c-45f2-9b84-3277142f38b0" />
![WhatsApp Image 2026-03-16 at 10 12 56 AM](https://github.com/user-attachments/assets/0a03f7b9-abc9-49c5-8508-779f6040c6aa)


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
