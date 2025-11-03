# Liver Disease Prediction – MATLAB Project

## Overview
This project focuses on predicting the presence of **liver disease** using machine learning techniques applied to a medical dataset of patient records.  
The work was developed as a group project for an academic course.

**Team Members:**  
Catalina Vasiliu · Camilla Petrungaro · Simindokht Mahmoudian · Giulia Di Giovan Paolo

---

## Project Context
Liver disease incidence is increasing worldwide due to several lifestyle and environmental factors such as alcohol consumption, exposure to toxic substances, and use of certain medications.  
The dataset used contains **583 patient records** from the North-East region of Andhra Pradesh (India), including both individuals with and without liver disease.  
The goal was to analyze biochemical parameters and develop machine learning models capable of predicting the presence of liver disease.

---

## Dataset Description
The dataset includes 11 features:
- Age  
- Gender  
- Total Bilirubin  
- Direct Bilirubin  
- Alkaline Phosphatase  
- Alamine Aminotransferase  
- Aspartate Aminotransferase  
- Total Proteins  
- Albumin  
- Albumin and Globulin Ratio  
- Dataset (class label: 1 = liver disease, 2 = no disease)

---

## Objectives
**Main Task:**  
Design and evaluate a **classification algorithm** able to predict if an individual has liver disease.

**Additional Tasks:**  
- Identify the most relevant features influencing the classification  
- Develop a **regression model** to predict *Total Proteins* based on other features  
- Explore how data preprocessing affects model accuracy  

---

## Methods
The MATLAB Live Script `presentation.mlx` implements the following workflow:

1. **Data Cleaning and Preprocessing**
   - Removal of missing values  
   - Outlier detection and handling through *winsorising*  
   - Creation of new variables through transformations  

2. **Classification**
   - Data split: 80% training, 20% testing  
   - Algorithms tested:  
     - Naïve Bayes  
     - Decision Tree  
     - K-Nearest Neighbors (KNN)  
     - Support Vector Machine (SVM)  
     - Neural Network  
   - Evaluation performed using accuracy and confusion matrices (via the custom function `cMetrics`)

3. **Regression Analysis**
   - A regression model was developed to predict **Total Proteins** using the most significant predictors.

---

## Custom Functions
The script uses two custom MATLAB functions:
- `winsorising.m` – limits extreme values to reduce the impact of outliers  
- `cMetrics.m` – computes classification metrics such as accuracy and confusion matrix statistics  

---

## Results Summary
- The **Naïve Bayes classifier** achieved the best performance among the tested models.  
- Feature transformations and rebalancing of healthy subjects improved classification accuracy.  
- The **regression model** for Total Proteins showed good predictive performance, confirming the relationship between protein levels and liver function indicators.

---

## Future Work
Further improvements could include:
- Feature selection based on statistical tests  
- Cross-validation and hyperparameter optimization  
- Exploration of ensemble methods or deep learning architectures  

---

## Repository Content
- `presentation.mlx` – main MATLAB Live Script  
- `winsorising.m` – function for handling outliers  
- `cMetrics.mlx` – function for classification metrics  
- `README.md` – current file describing the project
- `LICENSE` – open-source license (MIT) defining permissions and terms of use
 

---

*Developed as part of a Machine Learning course project.*
