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

## Repository Structure

```
Student-Performance-ML-Project/
│
├── data/               # Dataset storage
│   ├── raw/            # Original, unmodified dataset (e.g., student-mat.csv)
│   └── processed/      # Cleaned dataset and preprocess dataset ready for modeling
│
├── notebooks/                        # Google Colab notebooks for each stage
│   ├── 01_data_preprocessing.ipynb   # Data cleaning, encoding, normalization
│   ├── 02_feature_selection.ipynb    # Feature analysis and selection
│   ├── 03_model_training.ipynb       # Model implementation and training
│   ├── 04_model_evaluation.ipynb     # Metrics, confusion matrix, evaluation
│   └── 05_final_pipeline.ipynb       # End-to-end pipeline for final demo
│
├── results/                  # Output results and visualizations
│   ├── plots/                # Graphs (accuracy, feature importance, etc.)
│   ├── confusion_matrices/   # Confusion matrix images
│   └── metrics.csv           # Summary of model performance metrics
│
├── models/                 # Saved trained models
│   ├── logistic_model.pkl  # Logistic Regression model
│   └── random_forest.pkl   # Random Forest model
│
├── .gitignore
├── CONTRIBUTING.md
├── LICENSE.md
├── README.md
└── SECURITY.md
```

---
## Getting Started

### Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/Student-Performance-ML-Project.git
```
### Running the Project in Google Colab
1. Go to Google Drive  
2. Click **New → More → Google Colaboratory**  
   *(If not visible: New → More → Connect more apps → search “Colab”)*  
3. Rename the notebook and place it inside your project folder  
4. Click **“Connect”** (top right) to start a runtime  
5. Upload or copy code from the `notebooks/` folder into the Colab notebook  
6. Run the notebook:
   - Click **Runtime → Run all**, or  
   - Click the **▶️ play button** next to each code cell  

---

## Dataset

* **Source:** UCI Machine Learning Repository – Student Performance Dataset
* **Size:** 649 student records
* **Features:** 30 variables (demographic, academic, behavioral)

The dataset can be accessed by cloning the repository and loading it locally.
  ```bash
  git clone https://github.com/YOUR_USERNAME/Student-Performance-ML-Project.git  
      
  ### Load the Dataset
  data = pd.read_csv('data/raw/student-mat.csv')
  display(data)
  ```

### Key Features Used

* Study time
* Absences
* Social and daily habits
* First period grade (G1)

### Important Note

To ensure early prediction, the feature G2 (second period grade) is excluded from the model.

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

| Member | Role | Task(s) |
|--------|------|---------|
| **Kenneth** | Integrator | Model implementation and training |
| **Edward** | — | Data acquisition, preprocessing, feature selection |
| **Lauren** | — | Model evaluation and visualization |

---

## Expected Outcomes

* Accurate early prediction of student performance
* Identification of at-risk students
* Insights into factors affecting academic success

---

## References

* UCI Machine Learning Repository – Student Performance Dataset
* P. Cortez and A. Silva, *Using Data Mining to Predict Secondary School Student Performance*, 2008

---

## Notes

This project demonstrates the feasibility of early academic performance prediction using machine learning and highlights the importance of data-driven decision-making in education.
