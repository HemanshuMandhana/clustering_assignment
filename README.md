# Clustering Performance Evaluation on Different Preprocessing Techniques

This report analyzes the performance of three clustering algorithms (KMeans, Hierarchical, and Mean Shift) on a dataset using different preprocessing techniques. The evaluation metrics used include **Silhouette Score**, **Calinski-Harabasz Index**, and **Davies-Bouldin Index**. Each experiment was conducted for cluster sizes c = 3, 4, and 5.

---

## 📊 Clustering Performance Tables

### ✅ KMeans Clustering

| Parameters      | No Data Processing |                    |                    | Using Normalization |                    |                    | Using Standardization |                    |                    | Using PCA |          |          | Using T+N |          |          | T+N+PCA |          |          |
|-----------------|--------------------|--------------------|--------------------|----------------------|--------------------|--------------------|------------------------|--------------------|--------------------|-----------|----------|----------|-----------|----------|----------|---------|----------|----------|
|                 | c=3                | c=4                | c=5                | c=3                  | c=4                | c=5                | c=3                    | c=4                | c=5                | c=3       | c=4      | c=5      | c=3       | c=4      | c=5      | c=3     | c=4      | c=5      |
| **Silhouette**       | 0.5528             | 0.4981             | 0.4887             | 0.5048               | 0.4451             | 0.3526             | 0.4599                 | 0.3869             | 0.3419             | 0.5092    | 0.4413   | 0.4156   | 0.4906    | 0.4392   | 0.3290   | 0.5508  | 0.5195   | 0.4291   |
| **Calinski-Harabasz** | 561.63             | 530.77             | 495.54             | 359.85               | 314.47             | 289.51             | 241.90                 | 207.27             | 203.27             | 293.86    | 263.81   | 278.55   | 439.85    | 364.36   | 342.73   | 574.51  | 509.11   | 526.96   |
| **Davies-Bouldin**   | 0.6620             | 0.7803             | 0.8060             | 0.7603               | 0.9004             | 0.9570             | 0.8336                 | 0.8698             | 0.9530             | 0.7099    | 0.7560   | 0.7712   | 0.7760    | 0.9033   | 1.0211   | 0.6468  | 0.6954   | 0.7802   |

---

### 🧩 Hierarchical Clustering

| Parameters      | No Data Processing |                    |                    | Using Normalization |                    |                    | Using Standardization |                    |                    | Using PCA |          |          | Using T+N |          |          | T+N+PCA |          |          |
|-----------------|--------------------|--------------------|--------------------|----------------------|--------------------|--------------------|------------------------|--------------------|--------------------|-----------|----------|----------|-----------|----------|----------|---------|----------|----------|
|                 | c=3                | c=4                | c=5                | c=3                  | c=4                | c=5                | c=3                    | c=4                | c=5                | c=3       | c=4      | c=5      | c=3       | c=4      | c=5      | c=3     | c=4      | c=5      |
| **Silhouette**       | 0.5543             | 0.4890             | 0.4844             | 0.5048               | 0.4330             | 0.3493             | 0.4467                 | 0.4006             | 0.3306             | 0.5111    | 0.4487   | 0.4042   | 0.4766    | 0.4223   | 0.3176   | 0.5330  | 0.5025   | 0.4089   |
| **Calinski-Harabasz** | 558.06             | 515.08             | 488.48             | 349.25               | 301.10             | 272.02             | 222.72                 | 201.25             | 192.68             | 286.33    | 254.09   | 255.00   | 406.37    | 347.70   | 323.14   | 504.33  | 479.35   | 476.46   |
| **Davies-Bouldin**   | 0.6563             | 0.7953             | 0.8204             | 0.7480               | 0.8486             | 0.9058             | 0.8035                 | 0.9788             | 0.9742             | 0.7054    | 0.7226   | 0.7913   | 0.7697    | 0.8827   | 1.0020   | 0.5927  | 0.6240   | 0.7217   |

---

### 🌀 Mean Shift Clustering

| Parameters      | No Data Processing |                    |                    | Using Normalization |                    |                    | Using Standardization |                    |                    | Using PCA |          |          | Using T+N |          |          | T+N+PCA |          |          |
|-----------------|--------------------|--------------------|--------------------|----------------------|--------------------|--------------------|------------------------|--------------------|--------------------|-----------|----------|----------|-----------|----------|----------|---------|----------|----------|
|                 | c=3                | c=4                | c=5                | c=3                  | c=4                | c=5                | c=3                    | c=4                | c=5                | c=3       | c=4      | c=5      | c=3       | c=4      | c=5      | c=3     | c=4      | c=5      |
| **Silhouette**       | NaN                | NaN                | NaN                | 0.4770               | NaN                | NaN                | 0.4325                 | NaN                | NaN                | 0.4852    | NaN      | NaN      | 0.5444    | NaN      | NaN      | NaN     | 0.4236   | NaN      |
| **Calinski-Harabasz** | NaN                | NaN                | NaN                | 290.47               | NaN                | NaN                | 163.71                 | NaN                | NaN                | 167.41    | NaN      | NaN      | 278.23    | NaN      | NaN      | NaN     | 255.82   | NaN      |
| **Davies-Bouldin**   | NaN                | NaN                | NaN                | 0.7616               | NaN                | NaN                | 0.8131                 | NaN                | NaN                | 0.6060    | NaN      | NaN      | 0.6702    | NaN      | NaN      | NaN     | 0.7447   | NaN      |

---

## 📈 Visualization

![Clustering Performance Charts - KMeans, Hierarchical, Mean Shift](![image](https://github.com/user-attachments/assets/148ca0f8-aa6b-4f04-8052-952af940fd84)![image](https://github.com/user-attachments/assets/fb8820fa-4eb7-4a6c-a362-f8bf189d6cc5)![image](https://github.com/user-attachments/assets/751f402d-7791-487b-978d-efa203ba72a2)

)

---

## 🔍 Observations

- **KMeans with T+N+PCA** preprocessing performed best overall with high **Silhouette Score (0.5508)** and low **Davies-Bouldin Index (0.6468)**.
- **Hierarchical clustering** showed consistent results with PCA and T+N+PCA, especially for **c=3** clusters.
- **Mean Shift clustering** had fewer valid results due to clustering instability or insufficient cluster separation, but preprocessing significantly improved performance.
- Using **PCA and combined preprocessing (T+N+PCA)** helps in improving clustering compactness and separation across methods.

---

## ✅ Conclusion

From the experimental analysis:

- **T+N+PCA preprocessing** is consistently beneficial for most clustering techniques.
- **KMeans and Hierarchical clustering** outperform Mean Shift in terms of available metrics and consistent results.
- **PCA alone** also provides better separation and compactness for some clustering methods.

This analysis provides clear guidance on choosing preprocessing methods to enhance clustering performance for downstream applications.
