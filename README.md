# 🎓 Student Performance Prediction Using Machine Learning

## 📌 Overview

This project develops a machine learning system to **predict student academic performance early in the semester** using limited initial data such as attendance, study time, and early grades.

Unlike traditional models that rely on complete datasets, this approach focuses on **early indicators** to identify students at risk of poor performance, enabling timely intervention and improved academic outcomes.

---

## 🎯 Objectives

* Predict final student performance (low, medium, high)
* Use only **early-semester features**
* Identify students at risk of failure
* Analyze which factors most influence academic success

---

## 📂 Project Structure

```
Student-Performance-ML/
│
├── data/
│   ├── raw/                # Original dataset
│   └── processed/          # Cleaned dataset
│
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_feature_selection.ipynb
│   ├── 03_model_training.ipynb
│   ├── 04_model_evaluation.ipynb
│   └── 05_final_pipeline.ipynb
│
├── results/
│   ├── plots/
│   ├── confusion_matrices/
│   └── metrics.csv
│
├── models/
│   ├── logistic_model.pkl
│   └── random_forest.pkl
│
├── README.md
└── requirements.txt
```

---

## 📊 Dataset

* **Source:** UCI Machine Learning Repository – Student Performance Dataset
* **Size:** 649 student records
* **Features:** 30 variables (demographic, academic, behavioral)

### 🔑 Key Features Used

* Study time
* Absences
* Social and daily habits
* First period grade (G1)

### ⚠️ Important Note

To ensure **early prediction**, the feature **G2 (second period grade)** is excluded from the model.

---

## 🛠️ Technologies Used

* Python
* Google Colab
* pandas, numpy
* matplotlib, seaborn
* scikit-learn
* joblib

---

## ⚙️ Methodology

### 1. Data Preprocessing

* Handle missing values
* Encode categorical variables
* Normalize numerical features
* Remove non-early indicators (e.g., G2)

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

## 📈 Results

The models are evaluated to determine:

* Prediction accuracy using early data
* Most influential features
* Best-performing algorithm

Results include:

* Confusion matrix visualizations
* Feature importance plots
* Model comparison charts

---

## 🚀 How to Run

### Option 1: Google Colab

1. Open notebooks from the `notebooks/` folder
2. Mount Google Drive:

```python
from google.colab import drive
drive.mount('/content/drive')
```

3. Run cells sequentially

---

### Option 2: Local Environment

1. Clone repository:

```bash
git clone https://github.com/YOUR_USERNAME/student-performance-ml.git
cd student-performance-ml
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run notebooks using Jupyter or VS Code

---

## 👥 Team Members

* **Edward** – Data acquisition, preprocessing, feature selection
* **Kenneth** – Model implementation and training
* **Lauren** – Model evaluation and visualization

---

## 📌 Expected Outcomes

* Accurate early prediction of student performance
* Identification of at-risk students
* Insights into factors affecting academic success

---

## 🔮 Future Improvements

* Hyperparameter tuning
* Additional models (SVM, Neural Networks)
* Comparison with full dataset (including G2)
* Interactive prediction interface

---

## 📚 References

* UCI Machine Learning Repository – Student Performance Dataset
* P. Cortez and A. Silva, *Using Data Mining to Predict Secondary School Student Performance*, 2008

---

## ⭐ Notes

This project demonstrates the feasibility of **early academic performance prediction** using machine learning and highlights the importance of data-driven decision-making in education.
