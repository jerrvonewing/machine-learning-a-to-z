# **Project Overview** ##
![Clustering](https://1.bp.blogspot.com/-fHdsJ8Q5TFU/WjqTHcKqZ-I/AAAAAAAAAic/_tVg-_c5XjcU96uWkMlzvkJ-yY3kyx2JgCLcBGAs/s1600/K-Means-Clustering-In-Machine-Learning.jpg)

This section contains a Jupyter Notebook that takes in a CSV file containing mock data from a mall with info about their customers. The data contains customer annual income, age, gender, spending score, and customer ID. Finding the best clustering model will help group customers. 

---
## [Table of Contents](#Clustering-Models)
- [01 - K-Nearest Means Clustering](#01---K-Nearest-Means-Clustering)
- [02 - Hierarchial Clustering](#02---Hierarchial-Clustering)

---
## **Clustering Models**
### **[01 - K-Nearest Means Clustering](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/clustering/01-k-means/k_means_clustering.ipynb)**
#### **Getting Started** 
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install scikit-learn
```   
#### **Section Overview**
This section demonstrates:

- Reading data from a CSV file using **pandas**
- Training the dataset using the **scikit-learn** module **KMeans**
- Determining the optimal amount of clusters using **the Elbow Method**
- Visualization the data using the **matplotlib** module

#### **K-Means Cluster**
![K-Means Cluster](/clustering/01-k-means/k_means_clustering.png)

---
### **[02 - Hierarchial Clustering](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/clustering/02-hierarchial/hierarchial_clustering.ipynb)**


#### **Getting Started**   
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install scikit-learn
pip install scipy
```   
#### **Section Overview**
This section demonstrates:

- Reading data from a CSV file using **pandas**
- Creating a dendrogram using the **scipy** module
- Training the dataset using the **scikit-learn** module **AgglomerativeClustering**
- Visualization the data using the **matplotlib** module

#### **Hierarchial Clustering**
![Hierarchial Clustering](/clustering/02-hierarchial/hierarchial_clustering.png)

---

## Conclusion
### K-Means
#### Pros
- Simple to understand, easily adaptable, works well on small or large datasets, fast, efficient and performant

#### Cons
- Need to choose the number of clusters

### Hierarchial Clustering
#### Pros
- The optimal number of clusters can be obtained by the model itself, practical visualization with the dendrogram
#### Cons
- Not appropriate for large datasets

