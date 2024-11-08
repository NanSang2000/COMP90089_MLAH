
# COMP90089

## Machine Learning For Health - Group 23

## Table of Repository Contents
1. [Group Contract](Team-23_Group_Contract.pdf)
2. [Group Proposal](ML4Health_proposal_Group23.pdf)
3. [Digital Phenotying and Dataset](Dataset)
4. [Data Processing Generic](Preprocessing)
5. [Exploratory Data Analysis](exploratory)
6. [Clustering Analysis](clustering_analysis)
7. [Predictive Analysis](predictive_analysis)
8. [Environment Setting Requirements](requirements.txt)
9. [Miscellaneous](misc)
10. [Project report](ML4Health_report_group23.pdf)

## Project Details

### Objective
This study aims to predict severity and mortality rate for hospitalized patients with high lipase and amylase levels to improve the clinical decision-making for patients with Acute pancreatitis and improve their lifestyle.


### Materials and Methods
We used the MIMIC-IV dataset to perform the digital phenotyping and create the patient cohort and evaluate multiple models on the same
ML models: Random Forest, XGBoost, AdaBoost, CatBoost, Gradient Boosting, Decision Tree, SVM, KNN, Logistic Regression, K-Means clustering and DBSCAN clustering. 
Due to the class imbalance in the dataset, we have employed SMOTE oversampling technique to improve performance. Hyperparameters for each model were optimized using grid search with
10-fold cross-validation, and feature importance was analyzed using ensemble methods.

### Results
This study evaluated six machine learning models (Logistic Regression, KNN, Random Forest, XGBoost, CatBoost, and DNN) to predict severity and mortality in patients with acute pancreatitis (AP) using a specific phenotype and ICD cohort. CatBoost achieved the best performance for severity prediction, with an accuracy of 0.75, precision of 0.72, recall of 0.75, F1 score of 0.73, and ROC AUC of 0.84, demonstrating strong predictive power without the need for oversampling. Logistic Regression and KNN showed moderate results, with improvements from SMOTE, though with limited overall accuracy and F1 scores.

For mortality prediction, Random Forest with SMOTE balanced precision and recall, achieving the highest F1 score (0.66). Logistic Regression, though simplistic, recorded high precision (0.81) and ROC-AUC (0.95), capturing patterns effectively. KNN with SMOTE attained the highest recall (0.69) but had the lowest ROC-AUC (0.82). The ROC curves for the models also verify that CatBoost and Random Forest with SMOTE provide the most robust classifications for severity and mortality, respectively.

In summary, CatBoost and Random Forest (with SMOTE) emerged as top-performing models for severity and mortality classification, highlighting the strengths of ensemble learning in handling complex patient data.

## Steps to Implement Codes
* Require access to MIMIC-IV database and finish Bigquery settings via the link: [MIMIC-IV Access](https://physionet.org/content/mimiciv/2.2/)
* Set the environment and versions according to the [Environment Setting Requirement](requirements.txt).
* Run the code of [Digital Phenotyping and Dataset](Dataset/AP_Lipase_VitalSigns_Com.ipynb), save the full cohort datasets, or use the [Pre-created Dataset for severity prediction](Dataset/AP_ICD_CCI_CC_dataset.csv) or [Pre-created Dataset for severity prediction](Dataset/AP_ICD_CCI_CC_dataset.csv).
* Input Dataset file and apply it by running [Data Processing Generic](Preprocessing/preprocessing.ipynb), which contains steps for data processing and feature selection, then perform EDA using [Exploratory Data Analysis](exploratory/EDA.ipynb), and finally [Clustering Analysis](clustering_analysis/clustering.ipynb), [Predictive Analysis](predictive_analysis/classification.ipynb), and [Predictive Analysis](predictive_analysis/Mortality_Predictor_final.ipynb) for modelling, evaluation and analysis.

## Conclusion & Future works
This study demonstrates the potential of machine learning models in predicting the severity and mortality of acute pancreatitis (AP) in hospitalized patients. Our findings show that CatBoost effectively predicts severity by capturing complex feature interactions without the need for data balancing techniques like SMOTE, while Random Forest achieves reliable mortality prediction by balancing accuracy and F1 scores with SMOTE. Leveraging a comprehensive range of clinical and biochemical data from the MIMIC-IV dataset, these models offer an early-warning system to support clinicians in prioritizing and personalizing care for AP patients. Future work should validate these models across diverse clinical settings, such as the ICU, and incorporate additional clinical features to enhance robustness and generalizability, ultimately aiming to improve patient outcomes in intensive care.

We have also developed a Graphical User Interface (GUI) using Streamlit as an external application for predicting mortality rates in patients diagnosed with Acute Pancreatitis. This tool, built with simple features, can be adapted to healthcare systems to assist in delivering personalized treatments, predicting disease severity, and enhancing overall patient care. The source code can be found under [Miscellaneous](misc) folder.


**Thanks**

Group 23
