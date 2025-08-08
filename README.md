# 🎵 Music Genre Clustering with PCA & KMeans

This project applies unsupervised learning techniques, including **data scaling**, **Principal Component Analysis (PCA)**, and **KMeans clustering**, to a dataset of Nigerian songs. The goal is to group songs based on numerical features and evaluate clustering performance using the **silhouette score** and optionally **accuracy** (if labeled classes are present).

---

## 📁 Dataset

- **File**: `nigerian-songs.csv`
- **Type**: Tabular
- **Content**: Contains various features (numerical and possibly categorical) for songs.
- **Target**: Optional column `target` representing the true label/class of the songs.

---

## ⚙️ Steps Performed

### 1. Preprocessing

- **Dropped non-numeric columns** to focus on features usable by clustering algorithms.
- **Handled missing values** by removing rows with `NaN`s.
- **Scaled** the numeric data using `StandardScaler` to normalize feature distributions.

### 2. PCA (Principal Component Analysis)

- Reduced the dataset to **5 principal components**.
- PCA helps to:
  - Reduce dimensionality
  - Capture the most significant variance in data
  - Improve clustering quality and performance

### 3. KMeans Clustering

- Applied `KMeans` with the number of clusters equal to the number of known classes (`target`) if available.
- Labels assigned to each song based on cluster association.

### 4. Evaluation

- **Silhouette Score**: Measures how well samples are clustered, ranges from -1 to +1.
  - Higher score = better-defined clusters.
- **Accuracy Score** *(optional)*: If a `target` column is present, aligns cluster labels with true labels using `mode` of each cluster to estimate accuracy.


## 📦 Requirements

- Python 3.7+
- pandas
- numpy
- scikit-learn
- scipy

Install dependencies:

```bash
pip install pandas numpy scikit-learn scipy
