
# K-Means Clustering on Iris Dataset

This repository contains the implementation of K-Means Clustering on the Iris dataset for the CS4038D Data Mining course assignment. The goal of this experiment was to perform clustering on the Iris dataset and evaluate both intrinsic and extrinsic clustering performance using various metrics.

## Problem Statement
The objective of this experiment is to:
1. Find the optimal number of clusters for the Iris dataset.
2. Explore the most suitable distance measures for clustering.
3. Evaluate the clusters formed based on provided labels.

### Dataset Overview
The Iris dataset contains 150 samples with the following features:
- **Features**: Sepal Length, Sepal Width, Petal Length, Petal Width
- **Class Labels**: Iris-setosa, Iris-versicolor, Iris-virginica

## Experiment Details

### 1. Finding the Optimal Number of Clusters

#### Elbow Method
- The optimal number of clusters is 3, where the SSE begins to plateau.

#### Silhouette Analysis
- The optimal number of clusters is 2, with a score of 0.58. However, 3 clusters with a score of 0.46 is also a reasonable choice.

#### Calinski-Harabasz Index
- The optimal number of clusters is 2, with a score of 248.9, although 3 clusters with a score of 239.2 is close.

#### V-Measure
- The optimal number of clusters is 2, with a score of 0.73.

### 2. Distance Measures and Custom Clustering
We explored four distance measures for clustering:
- **Manhattan Distance**: Sum of absolute differences between coordinates.
- **Euclidean Distance**: Straight-line distance between two points.
- **Cosine Similarity**: Measures the cosine of the angle between two vectors.
- **Chebyshev Distance**: Measures the greatest absolute difference between coordinates.

### 3. Performance Summary of Distance Measures
| Metric           | Manhattan | Euclidean | Cosine | Chebyshev |
|------------------|-----------|-----------|--------|-----------|
| **Purity Score** | 0.83      | 0.82      | 0.826  | 0.83      |

### 4. Model Parameters Used
- **n_clusters**: 3 (number of clusters to form)
- **random_state**: 3 (for reproducibility)
- **init**: 'k-means++' (for better initialization)
- **tol**: 1e-4 (tolerance for convergence)
- **n_init**: 200 (number of initializations)
- **max_iter**: 500 (maximum number of iterations)

### 5. Intrinsic and Extrinsic Cluster Evaluation
#### Intrinsic Measures:
- **Silhouette Score**: 0.51
- **Davies-Bouldin Index**: 0.74
- **WCSS (Inertia)**: 140.97

#### Extrinsic Measures:
- **Adjusted Rand Index**: 0.62
- **Normalized Mutual Info**: 0.66
- **Fowlkes-Mallows Score**: 0.75

### Final Clustering
The Iris dataset is separable into 2 or 3 clusters. Iris Setosa is easily distinguishable from the other two classes, while Iris Versicolor and Iris Virginica share similar features and are harder to distinguish.

### Conclusion
- The dataset can be effectively clustered into 2 or 3 groups.
- Distance measures such as Manhattan, Euclidean, Cosine, and Chebyshev show similar performance in terms of clustering quality.

## Requirements
- Python 3.x
- Libraries: `numpy`, `pandas`, `matplotlib`, `seaborn`, `sklearn`

## How to Run
1. Run this file in a Jupyter Notebook or Google Colab environment.
   ```

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
