# Unsupervised Learning

Unsupervised learning is a class of machine learning techniques that finds patterns or structure in data **without labeled responses**. Unlike supervised learning, there is no target variable or ground truth to guide the algorithm. Instead, the model explores the data to discover hidden relationships.

![unsupervised.png](unsupervised.png)

## What It Does

Given a dataset of input features:

X = {x₁, x₂, ..., xₙ}, where xᵢ ∈ ℝᵈ

Unsupervised learning tries to find:
- **Clusters** of similar points (clustering)
- **Lower-dimensional representations** (dimensionality reduction)

### 1. Clustering
Group data into clusters based on similarity.
- Algorithms: K-Means, DBSCAN
- Example: Segmenting customers based on behavior

### 2. Dimensionality Reduction
Project high-dimensional data into a lower-dimensional space.
- Algorithms: PCA
- Example: Visualizing data in 2D for exploratory analysis

### Advantages
- Does not require labeled data (often expensive or unavailable)
- Useful for data exploration and pattern discovery
- Enables feature learning and preprocessing for downstream tasks

### Disadvantages
- No clear way to evaluate accuracy (no ground truth)
- Results can be sensitive to algorithm settings (e.g., number of clusters)
- Interpretation can be subjective