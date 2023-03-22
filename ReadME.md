# **Machine Learning A to Z** #
![Thinking AI](https://www.analyticsinsight.net/wp-content/uploads/2020/03/AI_Animated.gif)

## **Project Overview** ##
This repository documents my machine learning journey. This repository consists of files demonstrating the work, as well as template files that help kickstart machine learning applications

---
##  Table of Contents ###
### [Regression](https://github.com/jerrvonewing/machine-learning-a-to-z/tree/main/regression)
- [01 - Data Preprocessing](#01---Data-Preprocessing)
- [02 - Simple Linear Regression](#02---Simple-Linear-Regression)
- [03 - Multiple Linear Regression](#03---Multiple-Linear-Regression)
- [04 - Polynomial Regression](#04---Polynomial-Regression)
- [05 - Support Vector Regression](#05---Support-Vector-Regression)
- [06 - Decision Tree Regression](#06---Decision-Tree-Regression)


### Template Files ###
- [01 - Data Preprocessing Template](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/01-data-preprocessing/data_preprocessing_template.ipynb)
---

## **[01 - Data Preprocessing](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/01-data-preprocessing/data_preprocessing.ipynbb)**

### **Getting Started** ###
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install sklearn
```

### **Section Overview** ###

This section contains a Jupyter Notebook that takes in a CSV file containing mock data to determine if a customer would make a purchase using our machine learning model

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Importing missing values using **SimpleImputer** from the **sklearn** module
- Updating matrices using the **SimpleImputer** transform method
- Encoding all rows in a column using **OneHotEncoder** and **ColumnTransformer** from the **sklearn** module
- Encoding on a single column using **LabelEncoder** from the **sklearn** module
- Splitting the data into training and test sets using **train_test_split** from the **sklearn** module
- Feature Scaling using and Standardization using **StandardScaler** from the **sklearn** module

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

### **Template Files** ###

- [01 - Data Preprocessing Template](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/01-data-preprocessing/data_preprocessing_template.ipynb)

---

## **[02 - Simple Linear Regression](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/02-simple-linear-regression/simple_linear_regression.ipynb)**

### **Getting Started** ###
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install sklearn
```

### **Section Overview** ###
This section contains a Jupyter Notebook that takes in a CSV file containing mock data to determine if there is a linear relationship between years of experience and salary.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Splitting the data into training and test sets using **train_test_split** from the **sklearn** module
- Creating a linear regression model using the **LinearRegression** class from the **sklearn** module
- Predicting the dependent variable based on the training set
- Visualizing the actual vs predicted results for both the test set and data set

### **Assumptions of Linear Regression** ###
![Assumptions of Linear Regression Graphic](https://sds-platform-private.s3-us-east-2.amazonaws.com/uploads/B97-Header-Image.jpg)

---

## **[03 - Multiple Linear Regression](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/03-multiple-linear-regression/multiple_linear_resgression.ipynb)**


### **Getting Started** ###
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install sklearn
```

### **Section Overview** ###
This section contains a Jupyter Notebook that takes in a CSV file containing data of 50 startup companies. We have how much was spent on research & developent, administration, marketing, what state they are based out of, and profit. We want to determine if there is a linear relationship between these varaibles compared to profit.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Splitting the data into training and test sets using **train_test_split** from the **sklearn** module
- Encoding categorical data using **OneHotEncoder**
- Training multiple linear regression model on training set using the **LinearRegression** method
- Using our linear regression model to predict results using the **predict** method
- Calculating the linear regression equation using the **coef_** and **intercept** method
---

## **[04 - Polynomial Regression](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/04-polynomial-regression/polynomial_regression.ipynb)**
### **Getting Started** ###
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install sklearn
```

### **Section Overview** ###
This section contains a Jupyter Notebook that takes in a CSV file containing mock data to determine if there is a linear or polynomial relationship between job level and salary.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Training multiple linear regression model on the dataset using the **LinearRegression** method
- Training polynomial linear regression model on the dataset using the **PolynomialFeatures** method
- Using our polynomial linear regression model to predict results using the **predict** method
- Visualizing data using the **matplotlib** module
---

## **[05 - Support Vector Regression](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/05-support-vector-regression/support_vector_regression.ipynb)**


### **Getting Started** ###
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install sklearn
```

### **Section Overview** ###
This section contains a Jupyter Notebook that takes in a CSV file containing mock data to determine if there is a SVR relationship between job level and salary.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Feature Scaling using and Standardization using **StandardScaler** from the **sklearn** module
- Training the dataset using the **sklearn** module
- Predicting single and multiple values
- Visualization the data using the **matplotlib** module
---

## **[06 - Decision Tree Regression](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/06-decision-tree-regression/decision_tree_regression.ipynb)**

### **Getting Started** ###
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install sklearn
```
### **Section Overview** ###
This section contains a Jupyter Notebook that takes in a CSV file containing mock data to determine if there is a Decision Tree relationship between job level and salary.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Training the dataset using the **sklearn** module
- Predicting single and multiple values
- Visualization the data using the **matplotlib** module
---

## **[07 - Random Forest Regression](https://github.com/jerrvonewing/machine-learning-a-to-z/blob/main/regression/07-random-forest-regression/random_forest_regression.ipynb)**

### **Getting Started** ###
This section is written using a Jupyter framework, where all packages are installed in  Google Collab. If you need to install the packages used in this section, copy the following commands:

```powershell
pip install numpy
pip install matplotlib
pip install pandas
pip install sklearn
```
### **Section Overview** ###
This section contains a Jupyter Notebook that takes in a CSV file containing mock data to determine if there is a Random Forest Regression relationship between job level and salary.

This section demonstrates:

- Reading data from a CSV file using **pandas**
- Training the dataset using the **sklearn** module
- Predicting single and multiple values
- Visualization the data using the **matplotlib** module

![](data:image/png;base64,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)