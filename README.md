# Lab 5: Clustering Techniques Using DBSCAN and Hierarchical Clustering

**Course:** MSCS-634-B01 — Advanced Big Data and Data Mining  
**Student:** Xhon Pelushi  
**University:** University of the Cumberlands

## Purpose

This lab explores density-based (DBSCAN) and agglomerative hierarchical
clustering on the Wine dataset from scikit-learn. Both algorithms are
compared using silhouette, homogeneity, and completeness scores.

## Key Insights

- **Hierarchical Clustering** with Ward linkage and `n_clusters=3`
  produced clusters closely matching the true wine classes, with the
  highest silhouette score among tested configurations.
- **DBSCAN** required careful tuning of `eps` and `min_samples`. Small
  eps values classified most points as noise, while larger values merged
  distinct classes. The Wine dataset's roughly globular clusters favor
  centroid-based methods over density-based ones.
- The **dendrogram** clearly shows three natural groupings, confirming
  that three clusters is the appropriate cut point for this data.
- DBSCAN's advantage — detecting arbitrary-shaped clusters and
  automatically identifying outliers — is less impactful here because
  the Wine classes are compact and similarly dense.

## Challenges

- DBSCAN parameter sensitivity: the algorithm's output changed
  dramatically across `eps` values, making it difficult to find a
  single configuration that works well across all classes.
- Visualizing 13-dimensional data required PCA reduction to 2D,
  which loses some cluster separation visible in higher dimensions.

## Files

| File | Description |
|------|-------------|
| `Lab5_DBSCAN_Hierarchical_Clustering.ipynb` | Jupyter Notebook with all clustering code, metrics, and visualizations |
| `README.md` | This file |
