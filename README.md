# Parkinson's Disease Detection Using Voice Analysis

![Image Description](https://github.com/aysh34/Parkinsons-Disease-Detection/blob/main/assets/parkinsons-disease.png)

This is my machine learning [project](https://www.kaggle.com/code/ayeshasal89/parkinson-s-disease-detection) focused on detecting Parkinson’s disease (PD) using acoustic features extracted from voice recordings. The motivation behind this work comes from my interest in developing **non-invasive, accessible, and early detection methods** for neurodegenerative disorders. Speech is one of the earliest and most affected aspects of PD, and analyzing its acoustic properties provides a practical way to support diagnosis.


## What is Parkinson’s Disease?

Parkinson’s disease (PD) is a progressive neurodegenerative disorder in which **dopamine-producing neurons in the substantia nigra** (a region of the basal ganglia responsible for motor control) are gradually lost. Dopamine is essential for smooth communication between brain cells, and its depletion leads to tremors, rigidity, slowed movements, and speech impairments.  

- Around **7.5 million people worldwide** are living with PD.  
- About **0.3% of people aged 40 and above** are affected.  
- Early detection can significantly improve patient management and quality of life.  

In healthy brains, dopamine neurons are abundant and regulate normal motor activity. In PD patients, their decline results in both motor symptoms and non-motor impairments such as changes in speech and voice.  

### Dopamine Levels: Normal vs Parkinson’s Disease
![Image Description](https://github.com/aysh34/Parkinsons-Disease-Detection/blob/main/assets/dopamine-difference.png)

## Why Voice Analysis?

Voice and speech are strongly affected in PD due to disruptions in muscle control and coordination. Patients often develop:  

- Reduced pitch variability  
- Lower vocal intensity  
- Irregularities in tone and rhythm  

These measurable changes in speech acoustics allow **machine learning algorithms** to detect patterns that may not be immediately noticeable to human listeners. This forms the foundation of my project.  

## Project Pipeline & Methodology  

The [dataset](https://www.kaggle.com/datasets/shreyadutta1116/parkinsons-disease) I used is available on kaggle. The goal was to classify individuals as either **healthy controls** or **Parkinson’s patients**.  

This project followed a systematic machine learning workflow to ensure robust and reproducible results.  

### 1. Data Exploration & Cleaning  
- **Initial Checks**: Verified data types, identified missing values, and checked class distribution (healthy vs Parkinson’s).  
- **Preprocessing**:  
  - Explored correlations between acoustic features to identify multicollinearity.  
  - Removed some highly correalted features to avoid overfitting.  
  - Standardized numerical features using **StandardScaler** to ensure all features contributed equally.  

### 2. Feature Engineering & Selection  
- **Statistical Analysis**: Evaluated which features showed significant differences between healthy and PD groups.  
- **Correlation Heatmaps**: Used to detect overlapping information among features.  

### 3. Model Development  
Implemented multiple machine learning models for comparative analysis:  
- **Decision Tree** – baseline interpretability model.  
- **Random Forest** – ensemble bagging approach, robust against overfitting.  
- **XGBoost** – gradient boosting model optimized for tabular data.  
- **Support Vector Machine (SVM)** – effective for small datasets with high-dimensional features.  
- **Gradient Boosting Classifier** – boosting-based ensemble method for sequential learning.  

Each model was trained using **5-fold cross-validation** to avoid overfitting and ensure generalization.  

### 4. Model Evaluation  
- **Metrics Used**: Accuracy, Precision, Recall, F1-score, ROC-AUC.  
- **Confusion Matrix Analysis**: Checked for false negatives.  
- **Cross-validation Statistics**: Recorded mean and standard deviation of F1-scores for stability insights.  
- **Comparative Analysis**: Tabulated and visualized the performance of all models for clear interpretation.  

## 5. Results Summary

| Model            | CV_Mean_F1 | Test_Accuracy | Test_F1 | ROC_AUC | Confusion Matrix                  |
|------------------|------------|---------------|---------|---------|-----------------------------------|
| RandomForest     | 1.0000     | 0.9969        | 0.9969  | 1.0000  | [[284, 1], [0, 36]]               |
| DecisionTree     | 0.9410     | 0.9969        | 0.9969  | 0.9982  | [[284, 1], [0, 36]]               |
| XGBoost          | 1.0000     | 1.0000        | 1.0000  | 1.0000  | [[285, 0], [0, 36]]               |
| SVM              | 1.0000     | 1.0000        | 1.0000  | 1.0000  | [[285, 0], [0, 36]]               |
| GradientBoosting | 0.9882     | 0.9969        | 0.9969  | 1.0000  | [[284, 1], [0, 36]]               |

This demonstrates the **potential of voice analysis as a diagnostic tool** for Parkinson’s disease.  

## Feature Importance

Using XGBoost, the **top 10 features** were identified, highlighting which acoustic measures contribute most to Parkinson’s detection.  
