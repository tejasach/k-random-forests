# K-Random Forest Clustering

A comprehensive implementation of **K-Random Forest clustering algorithm** compared with traditional K-Means clustering as baseline.

Based on: Bicego, M. (2019). K-Random Forests: a K-means style algorithm for Random Forest clustering. 2019 International Joint Conference on Neural Networks (IJCNN), Budapest, Hungary.[Original Paper](http://profs.sci.univr.it/~bicego/papers/2019_IJCNN.pdf)

## Key Contribution

This project introduces an **innovative clustering method** that leverages **Isolation Forests** for cluster assignment, offering a fresh perspective on unsupervised learning by combining clustering with anomaly detection principles.

## Overview

### **Algorithm Overview**
- **K-Random Forest Clustering**: Custom-designed algorithm using Isolation Forests as cluster representatives
- **Anomaly-Based Assignment**: Points are assigned to clusters based on anomaly scores rather than distance metrics
- **Iterative Convergence**: Algorithm iterates until label assignments stabilize

### **Comparative Analysis**
- **Baseline**: Traditional K-Means clustering
- **Evaluation Metrics**: Adjusted Rand Index (ARI) and Normalized Mutual Information (NMI)
- **Visualization**: PCA-based 2D visualization for intuitive comparison

## Methodology

### K-Random Forest Algorithm
Algorithm works through the following steps:

1. **Initialization**: Random cluster assignment of data points
2. **Forest Training**: Train an Isolation Forest for each cluster using assigned points
3. **Anomaly Scoring**: Compute anomaly scores for all points against each forest
4. **Reassignment**: Assign points to clusters where they appear least anomalous
5. **Iteration**: Repeat until convergence or maximum iterations reached

### Key Innovation
Unlike traditional distance-based clustering, K-Random Forest identifies clusters based on **data normality patterns**, making it potentially superior for:
- Non-spherical cluster shapes
- Outlier-robust clustering
- Complex data distributions

## Results

| Algorithm | ARI Score | NMI Score | Approach |
|-----------|-----------|-----------|----------|
| **K-Random Forest** | 0.8459 | 0.8109 | **Anomaly-based** |
| K-Means | 0.7163 | 0.7419 | Distance-based |

<img width="1800" height="500" alt="PCA_Comparison_K_RF" src="https://github.com/user-attachments/assets/d280a6e6-f695-411d-beb0-e17845eaa2b4" />

    
 **K-Random Forests method** has better performance compared to K-Means when both resulting clusters are compared with True value
