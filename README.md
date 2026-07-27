# Predicting Online Shoppers' Purchasing Intentions
**Data Mining and Machine Learning Project — A.Y. 2025-26**

## Project Overview
This repository contains the final project for the Data Mining and Machine Learning course. The study addresses the challenge of predicting online shoppers' purchasing intentions to optimize e-commerce conversion strategies. 

Using the **"Online Shoppers Purchasing Intention"** dataset, the problem is framed as a binary classification task. Due to the high cost of missing potential buyers in an e-commerce environment (False Negatives), the project focuses on maximizing **Recall** and the **F1-score**, deliberately prioritizing them over global Accuracy.

## Repository Structure
The project is divided into three sequential Jupyter Notebooks, forming a complete Machine Learning pipeline:

* **`DMML1.ipynb`**: Data loading, Exploratory Data Analysis (EDA), and data preprocessing.
* **`DMML2.ipynb`**: Model selection and hyperparameter tuning utilizing a 10×10 Nested Cross-Validation strategy.
* **`DMML3.ipynb`**: Final model training, performance evaluation on an unseen test set, and Explainable AI (XAI) analysis.

## Methodology & Key Techniques
* **Handling Class Imbalance:** The dataset presents a severe class imbalance, which is effectively addressed using the **SMOTENC** oversampling technique.
* **Ablation Study:** Initial feature importance analysis revealed indirect target leakage from opaque Google Analytics metrics. An ablation study was conducted to remove these features, forcing the model to rely strictly on genuine browsing behavior.
* **Algorithm Comparison:** Five different algorithms were compared using Nested CV. **CatBoost** consistently outperformed the alternatives.
* **Explainable AI (XAI):** Global and local interpretability is provided using **SHAP (SHapley Additive exPlanations)** to understand the true drivers of online purchasing intent.

## Main Results
The final ablated CatBoost model ensures robust generalization on unseen data. By relying purely on behavioral signals such as engagement metrics, seasonality, and traffic sources, the model successfully avoids algorithmic shortcuts while achieving a realistic final F1-score of 0.37 and an AUC of 0.72.

## Authors
* **Dario Falaschi** 
* **Chiara Masiero**
