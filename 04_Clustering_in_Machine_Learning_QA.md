# Clustering in Machine Learning — Professional Q&A

---

## Q1: What is clustering in machine learning?

**A:**  
Clustering is an unsupervised learning technique used to group similar data points together based only on their features, without using any labels. The aim is to find natural groupings or patterns within the data.

**Examples:**  
- Market segmentation (grouping customers by behavior)
- Image segmentation (grouping pixels/objects)
- Document/topic clustering

---

## Q2: What are the main clustering algorithms?

| Algorithm           | Description                                  | Typical Use-Case             |
|---------------------|----------------------------------------------|------------------------------|
| K-Means             | Assigns points to K centroids (clusters)     | Customer segmentation        |
| Hierarchical        | Builds a tree (dendrogram) of clusters       | Genetics, document clustering|
| DBSCAN              | Finds dense regions, robust to outliers      | Geospatial, anomaly detection|
| Gaussian Mixture    | Probabilistic clusters with overlap          | Soft clustering, anomaly     |

---

## Q3: How does K-Means clustering work?

- Choose the number of clusters (K)
- Randomly place K centroids
- Assign each point to the nearest centroid
- Move centroids to the mean of assigned points
- Repeat until centroids stop moving

---

## Q4: How do you evaluate clustering results?

| Metric          | Description                        |
|-----------------|------------------------------------|
| Silhouette Score| Measures how similar a point is to its cluster vs others |
| Inertia         | Sum of squared distances to centroid (lower is better)  |
| Davies–Bouldin  | Lower = better separation          |

---

## Q5: Challenges in clustering?

- Choosing the right number of clusters (K)
- Sensitivity to initial conditions and outliers
- Different algorithms suit different data shapes
- Hard to interpret clusters without labels

---

## Q6: What does clustering look like in code (scikit-learn example)?

```python
from sklearn.cluster import KMeans
kmeans = KMeans(n_clusters=3)
clusters = kmeans.fit_predict(X)
```

---

## Q7: Visual Memory

```
[Data Points] → [Clustering Algorithm] → [Groups/Clusters]
```

---

# End of Q&A
