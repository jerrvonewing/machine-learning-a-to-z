# **Machine Learning A to Z** #
![Thinking AI](https://www.analyticsinsight.net/wp-content/uploads/2020/03/AI_Animated.gif)

## **Project Overview** ##
This repository documents my machine learning journey. This repository consists of files demonstrating the work, as well as template files that help kickstart machine learning applications

---
##  Table of Contents 
### [Regression Models](#Regression-models-1)
- [01 - Data Preprocessing](#01---Data-Preprocessing)
- [02 - Simple Linear Regression](#02---Simple-Linear-Regression)
- [03 - Multiple Linear Regression](#03---Multiple-Linear-Regression)
- [04 - Polynomial Regression](#04---Polynomial-Regression)
- [05 - Support Vector Regression](#05---Support-Vector-Regression)
- [06 - Decision Tree Regression](#06---Decision-Tree-Regression)
- [07 - Random Forest Regression](#07---Random-Forest-Regression)

#### Regression Template Files 
- [01 - Data Preprocessing Template](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/01-data-preprocessing/data_preprocessing_template.ipynb)
- [03 - Multiple Linear Regression Template](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/03-multiple-linear-regression/multiple_linear_regression_template.ipynb)
- [04 - Polynomial Regression Template](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/04-polynomial-regression/polynomial_regression_template.ipynb)
- [05 - Support Vector Regression Template](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/05-support-vector-regression/support_vector_regression_template.ipynb)
- [06 - Decision Tree Regression Template](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/06-decision-tree-regression/decision_tree_regression_template.ipynb)
- [07 - Random Forest Regression Template](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/07-random-forest-regression/random_forest_regression_template.ipynb)

### [Classification Models](#Classification-models-1)
- [01 - Logistic Regression](#01---Logistic-Regression)
- [02 - K-Nearest Regression](#02---K-Nearest-Regression)
- [03 - Support Vector Machine](#03---Support-Vector-Machine)
- [04 - Kernel SVM](#04---Kernel-SVM)
- [05 - Naive Bayes](#05---Naive-Bayes)

#### Classification Template Files 
- 


---
## **Regression Models**

### **[01 - Data Preprocessing](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/01-data-preprocessing/data_preprocessing.ipynbb)**

#### **Getting Started** 
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install scikit-learn
```

#### **Section Overview** 

This section contains a Jupyter Notebook that takes in a CSV file containing mock data to determine if a customer would make a purchase using our machine learning model

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Importing missing values using **SimpleImputer** from the **scikit-learn** module
- Updating matrices using the **SimpleImputer** transform method
- Encoding all rows in a column using **OneHotEncoder** and **ColumnTransformer** from the **scikit-learn** module
- Encoding on a single column using **LabelEncoder** from the **scikit-learn** module
- Splitting the data into training and test sets using **train_test_split** from the **scikit-learn** module
- Feature Scaling using and Standardization using **StandardScaler** from the **scikit-learn** module

```python
# Original Dataset
[['France' 44.0 72000.0]
 ['Spain' 27.0 48000.0]
 ['Germany' 30.0 54000.0]
 ['Spain' 38.0 61000.0]
 ['Germany' 40.0 nan]
 ['France' 35.0 58000.0]
 ['Spain' nan 52000.0]
 ['France' 48.0 79000.0]
 ['Germany' 50.0 83000.0]
 ['France' 37.0 67000.0]]
```

```python
# Encoded Dataset after getting missing values
[[1.0 0.0 0.0 44.0 72000.0]
 [0.0 0.0 1.0 27.0 48000.0]
 [0.0 1.0 0.0 30.0 54000.0]
 [0.0 0.0 1.0 38.0 61000.0]
 [0.0 1.0 0.0 40.0 63777.77777777778]
 [1.0 0.0 0.0 35.0 58000.0]
 [0.0 0.0 1.0 38.77777777777778 52000.0]
 [1.0 0.0 0.0 48.0 79000.0]
 [0.0 1.0 0.0 50.0 83000.0]
 [1.0 0.0 0.0 37.0 67000.0]]
```
---

### **[02 - Simple Linear Regression](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/02-simple-linear-regression/simple_linear_regression.ipynb)**

#### **Getting Started** 
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install scikit-learn
```

#### **Section Overview** 
This section contains a Jupyter Notebook that takes in a CSV file containing mock data to determine if there is a linear relationship between years of experience and salary.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Splitting the data into training and test sets using **train_test_split** from the **scikit-learn** module
- Creating a linear regression model using the **LinearRegression** class from the **scikit-learn** module
- Predicting the dependent variable based on the training set
- Visualizing the actual vs predicted results for both the test set and data set

### **Linear Regression Model**
![Linear Regression](/regression/02-simple-linear-regression/linear-regression.png)

#### **Assumptions of Linear Regression** ###
![Assumptions of Linear Regression Graphic](https://sds-platform-private.s3-us-east-2.amazonaws.com/uploads/B97-Header-Image.jpg)

---

### **[03 - Multiple Linear Regression](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/03-multiple-linear-regression/multiple_linear_resgression.ipynb)**


#### **Getting Started** 
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install scikit-learn
```

#### **Section Overview** 
This section contains a Jupyter Notebook that takes in a CSV file containing data of 50 startup companies. We have how much was spent on research & developent, administration, marketing, what state they are based out of, and profit. We want to determine if there is a linear relationship between these varaibles compared to profit.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Splitting the data into training and test sets using **train_test_split** from the **scikit-learn** module
- Encoding categorical data using **OneHotEncoder**
- Training multiple linear regression model on training set using the **LinearRegression** method
- Using our linear regression model to predict results using the **predict** method
- Calculating the linear regression equation using the **coef_** and **intercept** method
---

### **[04 - Polynomial Regression](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/04-polynomial-regression/polynomial_regression.ipynb)**
#### **Getting Started** 
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install scikit-learn
```

#### **Section Overview** 
This section contains a Jupyter Notebook that takes in a CSV file containing mock data to determine if there is a linear or polynomial relationship between job level and salary.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Training multiple linear regression model on the dataset using the **LinearRegression** method
- Training polynomial linear regression model on the dataset using the **PolynomialFeatures** method
- Using our polynomial linear regression model to predict results using the **predict** method
- Visualizing data using the **matplotlib** module

### **Polynomial Regression Model**
![Polynomial Regression](/regression/04-polynomial-regression/polynomial-regression.png)
---

### **[05 - Support Vector Regression](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/05-support-vector-regression/support_vector_regression.ipynb)**


#### **Getting Started** 
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install scikit-learn
```

#### **Section Overview** 
This section contains a Jupyter Notebook that takes in a CSV file containing mock data to determine if there is a SVR relationship between job level and salary.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Feature Scaling using and Standardization using **StandardScaler** from the **scikit-learn** module
- Training the dataset using the **scikit-learn** module
- Predicting single and multiple values
- Visualization the data using the **matplotlib** module

### **Support Vector Regression Model**
![Support Vector Regression](/regression/05-support-vector-regression/support-vector-regression.png)

---

### **[06 - Decision Tree Regression](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/06-decision-tree-regression/decision_tree_regression.ipynb)**

#### **Getting Started** 
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install scikit-learn
```
#### **Section Overview** 
This section contains a Jupyter Notebook that takes in a CSV file containing mock data to determine if there is a Decision Tree relationship between job level and salary.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Training the dataset using the **scikit-learn** module
- Predicting single and multiple values
- Visualization the data using the **matplotlib** module

### **Decision Tree Regression Model**
![Decision Tree Regression](/regression/06-decision-tree-regression/decision_tree_regression.png)

---

### **[07 - Random Forest Regression](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/07-random-forest-regression/random_forest_regression.ipynb)**

#### **Getting Started** 
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install scikit-learn
```
#### **Section Overview** 
This section contains a Jupyter Notebook that takes in a CSV file containing mock data to determine if there is a Random Forest Regression relationship between job level and salary.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Training the dataset using the **scikit-learn** module
- Predicting single and multiple values
- Visualization the data using the **matplotlib** module

### **Random Forest Regression Model**
![Random Forest Regression](/regression/06-decision-tree-regression/decision_tree_regression.png)

---

### Regression Conclusion: 
To determine which regression model is best for a given dataset, run the following code snippet to get the r squared value. The closer r squared is to 1, the better the regression model is.

```python
from sklearn.metrics import r2_score
r2_score(y_test, y_pred)
```

For the dataset we were given, random forest regression model has the highest r2 score.

---
## **Classification Models**
### **[01 - Logistic Regression](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/classification/01-logistic-regression/logistic_regression.ipynb)**
#### **Getting Started** 
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install scikit-learn
```   
#### **Section Overview**
This section contains a Jupyter Notebook that takes in a CSV file a dataset of previous customer info from a popular car dealership. We want to determine if a customer will purchase a new vehicle based on age and salary.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Training the dataset using the **scikit-learn** module (**LogisticRegression**)
- Splitting the data into training and test sets using **train_test_split** from the **scikit-learn** module
- Feature Scaling using and Standardization using **StandardScaler** from the **scikit-learn** module
- Creation of a **confusion matrix** and calulating the accuracy score
- Predicting single and multiple values
- Visualization the data using the **matplotlib** module

### **Logistic Regression Model**
![Logistic Regression](/classification/01-logistic-regression/logistic_regression.png)

---
### **[02 - K-Nearest Regression](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/classification/02-k-nearest/k_nearest_regression.ipynb)**


#### **Getting Started**   
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install scikit-learn
```   
#### **Section Overview**
This section contains a Jupyter Notebook that takes in a CSV file a dataset of previous customer info from a popular car dealership. We want to determine if a customer will purchase a new vehicle based on age and salary.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Training the dataset using the **scikit-learn** module (**KNeighborsClassifier**)
- Splitting the data into training and test sets using **train_test_split** from the **scikit-learn** module
- Feature Scaling using and Standardization using **StandardScaler** from the **scikit-learn** module
- Creation of a **confusion matrix** and calulating the accuracy score
- Predicting single and multiple values
- Visualization the data using the **matplotlib** module

### **K-Nearest Regression Model**
![K-Nearest Regression](/classification/02-k-nearest/k_nearest_regression.png)

---


### **[03 - Support Vector Machine](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/classification/03-support-vector-machine/support_vector_machine.ipynb)**
#### **Getting Started**   
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install scikit-learn
```   
#### **Section Overview**
This section contains a Jupyter Notebook that takes in a CSV file a dataset of previous customer info from a popular car dealership. We want to determine if a customer will purchase a new vehicle based on age and salary.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Training the dataset using the **scikit-learn** module (**SVC**)
- Splitting the data into training and test sets using **train_test_split** from the **scikit-learn** module
- Feature Scaling using and Standardization using **StandardScaler** from the **scikit-learn** module
- Creation of a **confusion matrix** and calulating the accuracy score
- Predicting single and multiple values
- Visualization the data using the **matplotlib** module

### **Support Vector Machine Model**
![Support Vector Machine](/classification/03-support-vector-machine/support_vector_machine.png)

---

### **[04 - Kernel SVM](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/classification/04-kernel-svm/kernel_svm.ipynb)**

#### **Getting Started** 
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install scikit-learn
```   
#### **Section Overview**
This section contains a Jupyter Notebook that takes in a CSV file a dataset of previous customer info from a popular car dealership. We want to determine if a customer will purchase a new vehicle based on age and salary.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Training the dataset using the **scikit-learn** module (**SVC**)
- Splitting the data into training and test sets using **train_test_split** from the **scikit-learn** module
- Feature Scaling using and Standardization using **StandardScaler** from the **scikit-learn** module
- Creation of a **confusion matrix** and calulating the accuracy score
- Predicting single and multiple values
- Visualization the data using the **matplotlib** module

### **Kernel SVM Model**
![Kernel SVM](/classification/04-kernel-svm/kernel_svm.png)
---

### **[05 - Naive Bayes](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/classification/04-naive-bayes/naive_bayes.ipynb)**
#### **Getting Started** 
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install scikit-learn
``` 

#### **Section Overview**
This section contains a Jupyter Notebook that takes in a CSV file a dataset of previous customer info from a popular car dealership. We want to determine if a customer will purchase a new vehicle based on age and salary.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Training the dataset on Naive Bayes using the **scikit-learn** module (**GaussianNB**)
- Splitting the data into training and test sets using **train_test_split** from the **scikit-learn** module
- Feature Scaling using and Standardization using **StandardScaler** from the **scikit-learn** module
- Creation of a **confusion matrix** and calulating the accuracy score
- Predicting single and multiple values
- Visualization the data using the **matplotlib** module

### **Naive Bayes Model**
![Naive Bayes](/classification/05-naive-bayes/naive_bayes.png)
---

### **[06 - Next Section]()**
#### **Getting Started** 
#### **Section Overview**
### **Support Vector Machine Model**
![Model Name]()
---