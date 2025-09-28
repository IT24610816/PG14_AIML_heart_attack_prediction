# PG14_AIML_heart_attack_prediction

Project Overview

This project focuses on building a leak-safe preprocessing pipeline for the Heart Attack Prediction dataset, where each group member contributed a distinct data preparation technique. The workflow covers handling missing data, encoding categorical variables, detecting and treating outliers, scaling features, performing feature engineering (via Mutual Information and PCA), and addressing class imbalance with SMOTE. At each step, we included visualizations (bar charts, boxplots, histograms, MI plots, PCA variance curves, before/after class distributions) to interpret the transformations. The final integrated pipeline produces clean, consistent, and model-ready datasets, ensuring collaboration, logical flow, and robustness for predictive modeling.



Dataset Details

Name: Heart Attack Prediction Dataset

Source: Kaggle (by Sourav Banerjee)

Size: 8,763 records × 25 columns (after removing IDs, 24 features + 1 target)

Contents: Patient demographic, lifestyle, medical history, and clinical variables (e.g., Age, Sex, Cholesterol, Blood Pressure, Diabetes, Family History, Exercise, Diet, BMI, Country/Continent, etc.), with the target column “Heart Attack Risk” indicating the likelihood of heart attack.



Group members roles

1. Abishakar G. - IT24610811 (Handling Missing Data)
Identified missing values and placeholders (e.g., “?”, “Unknown/Invalid”).
Replaced or imputed missing values using appropriate strategies (median for numeric, mode for categorical).

2. Kavibarath. S - IT24104109 (Encoding Categorical Variables)
Detected categorical features (e.g., Sex, cp, fbs) and transformed them into numeric format using One-Hot Encoding.
Ensured no false ordinality and consistent feature space by fitting encoder on train only.

3. Daranagama D.A.D.U. - IT24610820 (Outlier Detection & Treatment)
Analyzed continuous numeric variables (e.g., Cholesterol, Blood Pressure) using IQR method.
Removed or adjusted extreme values, supported with boxplots before and after treatment.

4. Dilsha W.K.C. - IT24104107 (Feature Scaling)
Standardized numeric variables (e.g., Cholesterol, BMI, Blood Pressure) to comparable ranges using StandardScaler/RobustScaler.
Visualized distributions with histograms before and after scaling to show normalization effect.

5. Nisal A.T.H.A. – IT24610816 (Feature Engineering)
Ranked features by importance using Mutual Information (MI) scores to identify most predictive variables.
Applied PCA to reduce dimensionality while retaining ~95% variance; visualized MI bar plots and PCA variance curves.

6. Punchinilame. U . P . I. S - IT24610821 (Class Imbalance Handling)
Checked target variable distribution to identify imbalance between classes (0: No Risk vs 1: Risk).
Applied SMOTE oversampling on train set to balance classes, with bar charts before and after resampling.



How to Run the Code

1.Clone or download this repository.

2.Place the dataset inside: data/raw/heart_attack_prediction_dataset.csv

3.Open the individual notebooks from the notebooks/ folder to view each member’s preprocessing technique:
     ITxxxxxxx_Preprocessing_technique.ipynb
     
4.Run the combined pipeline notebook:
  FinalPipeline.ipynb → integrates all preprocessing steps into one flow.
  
5.All results will be saved in:
  results/eda_visualizations/ → plots & charts (PNG/JPEG)
  results/outputs/ → cleaned datasets & processed outputs
  
