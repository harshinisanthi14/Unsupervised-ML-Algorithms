# Unsupervised-ML-Algorithms

## 1. K-Means Clustering

**Definition:**  
K-Means is a centroid-based clustering algorithm that partitions the dataset into **K distinct clusters** based on the distance to the cluster's centroid.

**Steps:**
1. Choose the number of clusters `K`.
2. Initialize `K` centroids randomly.
3. Assign each data point to the nearest centroid.
4. Recalculate centroids as the mean of points in each cluster.
5. Repeat steps 3-4 until centroids stop changing (convergence).

**Best Use Case:**  
When clusters are well-separated and approximately spherical.


## 2. Hierarchical Clustering

**Definition:**  
Hierarchical clustering builds a hierarchy of clusters using either:
- **Agglomerative approach** (bottom-up): start with each point as a single cluster, then merge closest pairs until one cluster remains.
- **Divisive approach** (top-down): start with one cluster, then split recursively.

**Key Term:** Dendrogram – a tree-like diagram showing merges/splits.

**Best Use Case:**  
When understanding the hierarchical relationships between clusters is important.


## 3. DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

**Definition:**  
DBSCAN groups together points that are close in terms of density, and marks points in low-density areas as outliers.

**Parameters:**
- **eps**: Maximum distance between two samples for them to be considered neighbors.
- **min_samples**: Minimum number of points to form a dense region.

**Steps:**
1. For each point, count neighbors within `eps`.
2. If number of neighbors >= `min_samples`, mark as a core point.
3. Expand cluster from core points by including directly reachable points.
4. Mark points not reachable from any core point as noise.


**Best Use Case:**  
When clusters have irregular shapes and dataset contains noise.
