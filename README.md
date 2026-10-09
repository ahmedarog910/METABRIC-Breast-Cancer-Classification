# METABRIC Breast Cancer Classification

## Project Overview

This project applies machine learning techniques to the METABRIC breast cancer dataset to explore patient classification, dimensionality reduction, and clustering.

## Objectives

* Perform data cleaning and exploratory data analysis (EDA).
* Preprocess numerical and categorical features using Scikit-learn pipelines.
* Train and compare multiple classification models.
* Apply Stratified Cross-Validation and hyperparameter tuning.
* Use PCA for dimensionality reduction and visualization.
* Apply K-Means clustering to explore patient groups.
* Evaluate model performance using classification metrics.
* Save the trained model and preprocessing pipeline for future predictions.

## Models

* Logistic Regression
* Support Vector Classifier (SVC)
* Random Forest
* Extra Trees Classifier

The best model is selected based on cross-validation ROC-AUC.

## Technologies

* Python
* Pandas and NumPy
* Matplotlib and Seaborn
* Scikit-learn
* Joblib
* Jupyter Notebook

## Repository Contents

* `Final_ML_project.ipynb` — Main project notebook.
* `metabric_best_model.joblib` — Saved classification pipeline.
* `metabric_pca.joblib` — Saved PCA model.
* `metabric_kmeans.joblib` — Saved K-Means model.
* `metabric_metadata.joblib` — Model metadata.
* `cross_validation_results.csv` — Cross-validation results.
* `hyperparameter_tuning_results.csv` — Hyperparameter tuning results.
* `clustering_scores.csv` — Clustering evaluation results.

## Usage

Load the saved model using Joblib and provide new patient data with the same feature names and compatible data types used during training.

```python
import joblib

model = joblib.load("metabric_best_model.joblib")
predictions = model.predict(new_patient_data)
```

## Dataset

METABRIC breast cancer gene expression and clinical data. The dataset must be obtained from an authorized source and supplied separately.

## Disclaimer

This project is for educational and research purposes only. It is not intended for clinical diagnosis or treatment decisions.
