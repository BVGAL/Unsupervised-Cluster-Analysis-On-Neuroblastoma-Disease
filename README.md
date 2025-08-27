
## 🧬 Identification of Patient Profiles Associated with Improved Neuroblastoma Survival

### A Clustering-Based Exploratory Analysis

This repository contains an unsupervised clustering study focused on identifying patient subgroups with different **survival outcomes** in **neuroblastoma**, based on clinical and biological features.

---

### 🎯 Project Aim

To explore whether unsupervised clustering techniques can uncover patterns related to **survival probability** in neuroblastoma patients by analyzing factors such as:

* **MYCN amplification**
* **Tumor risk level**
* **Cell differentiation**
* **Follow-up duration (time\_months)**

The study builds on data from the peer-reviewed article [“Neuroblastomas in Eastern China” (Ma et al., PeerJ, 2018)](https://peerj.com/articles/5665/), and includes **169 patient records** with 12 key features.

---

### 🧠 Methods Used

The following unsupervised algorithms were applied:

* **Hierarchical Clustering** (Ward linkage, tree-based grouping)
* **K-Means** (validated by highest silhouette score)
* **Mean Shift** (tested but excluded due to redundancy)
* **DBSCAN/Birch** (excluded due to instability on small datasets)

Data were standardized (mean = 0) to optimize cluster separation and minimize scale bias across heterogeneous features.

---

### 📊 Key Findings

* **Three clusters** (C1, C2, C3) showed distinct survival profiles:

  * **C1**: High-risk, high MYCN amplification, **27.5% survival**
  * **C2**: Mixed-risk, intermediate outcomes, **71.7% survival**
  * **C3**: Intermediate risk, low MYCN amplification, **90% survival**
* **Time under observation ("time\_months")** was longer in high-survival clusters, raising questions about follow-up bias vs. survival causality.
* **MYCN amplification** and **low tumor differentiation** were strongly associated with poor prognosis.

---

### 📉 Visual Insights

* **Box plots**: Cluster comparison of survival, MYCN, risk level, tumor differentiation
* **Bar charts**: Distribution of clinical labels across clusters
* **Silhouette scores**: Used to optimize K-Means cluster count
* **Cluster tree**: From hierarchical method for structure visualization

---

### ✅ Conclusion

This exploratory study confirms that **unsupervised clustering** can effectively reveal patient profiles associated with different neuroblastoma outcomes. While limited by sample size, the findings suggest the value of combining biological markers with clustering approaches to support **personalized oncology** and **risk stratification** in pediatric cancer.

