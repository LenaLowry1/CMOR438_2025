# DBSCAN

DBSCAN is a density-based clustering algorithm that groups together points that are closely packed and marks as outliers points that lie alone in low-density regions. It is particularly effective at discovering clusters of arbitrary shape and handling noise.

![dbscan_vs_kmeans.png](dbscan_vs_kmeans.png)

DBSCAN can also perform better than K-Means Clustering when the clusters are nested, because it focuses on finding a center and working outwards, while K-Means only considers distance, without taking into account the shape of the data. 

### DBSCAN Algorithm:

- Takes from the user its parameters
    - a radius, ε (epsilon)
    - the number of points that must fall within a point's radius for it to be considered a core point (core points form a dense region)
- Defines core points, working outwards through points within the predecessor's radius, until points are non-core
    - a non-core point can be defined in a cluster, but it cannot extend the cluster
- The points without a cluster are called **outliers** and they fall in low-density regions

### Advantages
- Identifies Arbitrary Shapes: Can find clusters of any shape based on density.
- No Need to Specify k: Unlike K‑means, you don’t need to predefine the number of clusters
- Noise Handling: Explicitly identifies outliers as noise.

### Disadvantages
- Parameter Sensitivity: Results depend heavily on ε and MinPts settings.
- Variable Density Limitation: Struggles with clusters of differing densities.
- High Dimensionality: Distance measures become less meaningful in high dimensions (curse of dimensionality).
- Computational Cost: Can be slow for large datasets without spatial indexing (e.g., k‑d tree).

### The datset

We will use the pengiuns dataset.

### Packages

In addition to previous packages, we use:

- [`sklearn.cluster`](https://scikit-learn.org/stable/api/sklearn.cluster.html)

