# Unsupervised Anomaly Detection in Medical Thyroid Data

This project presents a structured comparative analysis of unsupervised anomaly detection methods applied to real-world medical thyroid data.

The objective is to identify atypical patient observations using distance-based and geometric anomaly detection techniques.

---

## Problem Overview

Medical datasets often contain rare and heterogeneous anomalies that do not form clear clusters but appear locally isolated in feature space.  

This project focuses on detecting such local anomalies in a thyroid disease dataset using unsupervised learning methods.

Dataset source:
Kaggle – *Thyroid Disease Unsupervised Anomaly Detection*

---

## Data Preprocessing

The preprocessing pipeline includes:

- Removal of irrelevant columns
- Defensive numeric conversion
- Missing value handling (median imputation)
- Feature standardization using `StandardScaler`
- Statistical exploration and visualization
- Correlation analysis

All features were scaled to ensure comparability across hormonal measurements and binary medical indicators.

---

## Methods Implemented

The following unsupervised anomaly detection algorithms were implemented using the PyOD framework:

### 1. K-Nearest Neighbors (KNN)
- Distance-based detection
- Sensitive to local data structure
- Hyperparameters optimized:
  - `n_neighbors`
  - `contamination`
  - distance aggregation method

### 2. Angle-Based Outlier Detection (ABOD)
- Geometric method based on angle variance
- More robust in higher-dimensional spaces
- Hyperparameter optimized:
  - `n_neighbors`

### 3. LODA (baseline comparison)

---

## Experimental Design

A structured evaluation framework was built to:

- Compare anomaly scores across models
- Perform hyperparameter sensitivity analysis
- Monitor number of detected outliers
- Evaluate cluster separation using **Silhouette Score**
- Visualize anomaly structure using **PCA (2D projection)**

---

## Key Results

- KNN Silhouette Score: **0.5117**
- ABOD Silhouette Score: **0.4942**

Results indicate that anomalies in this dataset are predominantly local, making distance-based methods slightly more effective.

PCA visualizations confirm that detected anomalies lie near the boundary of the main distribution rather than forming distinct clusters.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- PyOD
- Seaborn
- Matplotlib

---

## Repository Structure

- `anomaly_detection.ipynb` – Full experimental pipeline
- `README.md` – Project overview

---

## Conclusion

This project demonstrates a complete unsupervised anomaly detection workflow, including preprocessing, algorithm comparison, hyperparameter optimization, quantitative evaluation, and geometric interpretation.

It reflects a structured and analytical approach to applied machine learning and numerical modeling.
