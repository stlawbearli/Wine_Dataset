# Wine_Dataset
# Wine Dataset — Unsupervised Clustering

## Overview
Unsupervised clustering of Italian wines based on chemical analysis.
Built as part of my Specialist Diploma in Data Science (AI) at Singapore Polytechnic.

**Best Model: K-Means (k=3) | Silhouette Score: 0.42**

---

## Dataset
- Source: [UCI Wine Dataset](https://archive.ics.uci.edu/ml/datasets/wine)
- 178 wine samples, 13 chemical features
- 3 known wine classes (used for reference only — not for training)

---

## Approach

### 1. Feature Selection
- Used Random Forest feature importances to identify top 5 features:
  flavanoids, color_intensity, alcohol, proline, od280/od315_of_diluted_wines

### 2. Optimal k Selection
- Elbow Method and Silhouette Scores tested for k=2 to 13
- Best k=3 confirmed by highest Silhouette Score (0.42)

### 3. Algorithms Compared
| Algorithm | Silhouette Score | Davies-Bouldin Index |
|---|---|---|
| K-Means (k=3) | 0.2849 | 1.389 |
| Agglomerative (k=3) | 0.2774 | 1.419 |
| DBSCAN | Not applicable (mostly noise) |

### 4. Visualisation
- PCA 2D projection of cluster assignments
- Pairplots across top features coloured by cluster

---

## Key Findings
- K-Means slightly outperforms Agglomerative Clustering
- DBSCAN is not well-suited to this dataset due to uniform density
- Top discriminating features: flavanoids, proline, alcohol

---

## Files
| File | Description |
|---|---|
| `Wine_Dataset__THR.ipynb` | Full clustering notebook |
| `wine.data` | Raw dataset |
| `wine.names` | Feature descriptions |

---

## Tools & Libraries
- Python, Pandas, NumPy
- scikit-learn (KMeans, AgglomerativeClustering, DBSCAN, PCA)
- Matplotlib, Seaborn

---

## Author
**Tan Han Rong**
Specialist Diploma in Data Science (AI), Singapore Polytechnic
