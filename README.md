# clustering
# Clustering Analysis on the Wine Dataset

This project performs clustering analysis on the **Wine Dataset** using three algorithms: K-Means, Hierarchical Clustering (AgglomerativeClustering), and Gaussian Mixture Models (GMM). The goal is to evaluate the impact of preprocessing techniques and determine the optimal clustering configuration.

---

## 📁 Repository Structure

---

## 📊 Dataset Details
- **Name**: Wine Dataset (from scikit-learn)
- **Link**: [sklearn.datasets.load_wine](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_wine.html)
- **Features**: 13 (e.g., alcohol, malic acid, ash)
- **Rows**: 178

---

## 🛠️ Clustering Algorithms
Three algorithms were implemented:
1. **K-Means**
2. **Hierarchical Clustering (AgglomerativeClustering)**
3. **Gaussian Mixture Models (GMM)**

---

## 🔄 Preprocessing Methods Tested
The following preprocessing techniques were evaluated:
| Preprocessing Method       | Description                                  |
|----------------------------|----------------------------------------------|
| **No Preprocessing**        | Raw data without modifications              |
| **Normalize**               | Data normalized using L2 normalization       |
| **PCA**                     | Dimensionality reduction to 2 components    |
| **T+N**                     | Normalization                                |
| **T+N+PCA**                 | Normalization followed by PCA               |

---

## 📈 Results
### Best Configuration:
- **Algorithm**: Hierarchical Clustering (AgglomerativeClustering)  
- **Preprocessing**: PCA  
- **Number of Clusters**: 3  
- **Silhouette Score**: 0.659  

### Summary of Key Findings:
1. **Hierarchical Clustering** outperformed K-Means and GMM across all preprocessing methods.
2. **PCA** preprocessing improved clustering quality by reducing noise and focusing on key features.
3. **3 clusters** consistently delivered the best results, aligning with the dataset’s ground truth (3 wine classes).
4. **Gaussian Mixture Models** had the lowest performance, likely due to non-Gaussian data distribution.

For detailed metrics (Silhouette, Calinski-Harabasz, Davies-Bouldin), see [compared_results.csv](./compared_results.csv).

---

## 🚀 How to Reproduce
1. **Install Dependencies**:
   ```bash
   pip install numpy pandas scikit-learn jupyter
   Run the Jupyter Notebook:
bash
jupyter notebook 102103784_Clustering.ipynb
View Results: The notebook generates CSV files with evaluation scores, which are also provided in this repository.
📝 Conclusion

This project demonstrates the importance of preprocessing and algorithm selection in clustering tasks. Hierarchical clustering with PCA preprocessing emerged as the most effective strategy for the Wine dataset. Future work could explore additional preprocessing techniques or hybrid models for improved performance.

🔍 Note: All results are based on silhouette scores, which measure cluster cohesion and separation. Higher values indicate better-defined clusters.

