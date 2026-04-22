# Student Performance Prediction Using Machine Learning

**ECGR 4105/5105 — Introduction to Machine Learning (ML) Spring 2026**
**University of North Carolina at Charlotte**

---

## Overview

This project develops a machine learning system to predict student academic performance early in the semester using limited initial data such as attendance, study time, and early grades.

Unlike traditional models that rely on complete datasets, this approach focuses on early indicators to identify students at risk of poor performance, enabling timely intervention and improved academic outcomes.

---

## Objectives

* Predict final student performance (low, medium, high)
* Use only early-semester features
* Identify students at risk of failure
* Analyze which factors most influence academic success
  
---

## Dataset

* **Source:** UCI Machine Learning Repository – Student Performance Dataset
* **Size:** 649 student records
* **Features:** 30 variables

The dataset can be accessed by cloning the repository and loading it locally.
  ```python
  data = pd.read_csv('data/raw/student-mat.csv')
  ```

---

## Technologies Used

* Python
* Google Colab
* pandas, numpy
* matplotlib, seaborn
* scikit-learn
* joblib

---

## Methodology

### 1. Data Preprocessing

* Handle missing values
* Encode categorical variables
* Normalize numerical features
* Remove non-early indicators

---

### 2. Feature Selection

* Correlation analysis
* Feature importance ranking
* Optional dimensionality reduction (PCA)

---

### 3. Model Development

Implemented models:

* Logistic Regression
* Decision Tree
* Random Forest

---

### 4. Training Strategy

* Train/Test split: 80/20
* Cross-validation for robustness

---

### 5. Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

---

## Results

The models are evaluated to determine:

* Prediction accuracy using early data
* Most influential features
* Best-performing algorithm

Results include:

* Confusion matrix visualizations
* Feature importance plots
* Model comparison charts

---

## Team Members

| Member | Task(s) |
|--------|---------|
| **Kenneth** | Integrator | Model implementation and training |
| **Edward** |  Data acquisition, preprocessing, feature selection |
| **Lauren** |  Model evaluation and visualization |

---

## Expected Outcomes

* Accurate early prediction of student performance
* Identification of at-risk students
* Insights into factors affecting academic success

---

## References

* UCI Machine Learning Repository – Student Performance Dataset
* P. Cortez and A. Silva, *Using Data Mining to Predict Secondary School Student Performance*, 2008
