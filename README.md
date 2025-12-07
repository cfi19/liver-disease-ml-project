# Liver Disease Classification Using Machine Learning

This repository contains my final project for CS4743 — Introduction to Machine Learning.

The goal of the project is to predict liver disease using routine clinical measurements from the Indian Liver Patient Dataset (ILPD) and compare several ML models.

---

## Project Overview

Liver disease can be difficult to diagnose early because it depends on interpreting multiple lab tests at once. In this project, I apply different ML models to classify patients as having liver disease or not based on 10 features such as: - bilirubin levels, - liver enzymes, - protein ratios.

The focus is not only on accuracy, but also on:

- Handling class imbalance (≈71% positive cases)
- Using:
  - recall,
  - F1-score,
  - ROC-AUC,
  - PR-AUC
- Understanding WHY some models perform better than others
- Exploring dimensionality reduction with PCA and a small autoencoder

This work is for academic purposes only and is not intended for clinical use or used as medical advice.

---

## Dataset

- Name: Indian Liver Patient Dataset (ILPD)
- Samples: 579 (after cleaning)
- Features: 10
  --> (Age, Gender, Bilirubin levels, SGOT/SGPT, Alkaline Phosphotase, Total Proteins, Albumin, A/G ratio)
- Target: `1 = liver disease`, `0 = no disease`
- Class distribution: ~71% positives

> ⚠️ The dataset is found in this repository, but the original one can be accessed & Downloaded from the UCI Machine Learning Repository

    or Kaggle by searching for “Indian Liver Patient Dataset (ILPD).

---

## Repository Structure

liver-disease-ml-project/
├── src/
│ └── liver_disease_ilpd.ipynb # Main analysis + models
├── results/
│ ├── ROC_Curves.png
│ ├── Precision-Recall-Curves.png
│ ├── CM_LogReg.png
│ ├── CM_NN.png
│ ├── PCA-Projection.png
│ ├── Autoencoder-Latent-Space.png
│ └── Performance-Comparison. png
├── deliverables/
│ └── Liver_Disease_ML_Technique_Report.pdf
│ └── Liver_Disease_ML_Presentation.pdf
└── README.md <------------------------------------- WE ARE HERE

## Models Implemented

The following models are implemented and evaluated in the notebook:
• Logistic Regression (baseline)
• K-Nearest Neighbors (KNN, k=5)
• Decision Tree
• Random Forest
• Gradient Boosting
• Neural Network (MLP with 2 hidden layers + dropout)
• Autoencoder + Logistic Regression (exploratory)

All models are evaluated on the same train/validation/test split using consistent metrics.

## Evaluation Metrics

Because the dataset is imbalanced, I used a range of metrics:
• Accuracy
• Precision
• Recall
• F1-score
• ROC-AUC
• PR-AUC
• Confusion matrices

The notebook also includes these visualizations:

- Combined ROC curves
- Combined Precision–Recall curves
- PCA visualization (2D projection)
- Autoencoder latent space visualization

These help explain why certain models performed better than others.

## How to Run the Notebook

\*\* I ran my code using Jupyter Notebook, so you can simply duplicate the entire folder and running it there OR you can run it using your preferred IDE (i.e., VS Code)

## FINAL NOTES

• This project was completed for CS4743 — Introduction to Machine Learning class at TXST.

• All results are based on academic exercises only and are not meant for real medical diagnosis.

• The autoencoder exploration is used for visualization and representation learning rather than performance improvement.
