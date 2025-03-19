# Project_ML

## Overview
Project_ML is a machine learning project designed to analyze and model data using various machine learning techniques. The project includes data preprocessing, exploratory data analysis (EDA), feature engineering, model training, and evaluation.

## Repository Structure
```
Project_ML/
│── src/                    # Source code directory
│   │── data/data/         # Raw and processed datasets
│   │── models/            # Saved machine learning models
│   │── notebooks/         # Jupyter notebooks for analysis
│   │── results_notebook/  # Notebooks containing results and evaluations
│   │── utils/             # Utility functions and scripts
│── README.md              # Project documentation
```

## Installation
To use this project, clone the repository and install the required dependencies.
```bash
git clone https://github.com/Kathry1/Project_ML.git
cd Project_ML
pip install -r requirements.txt
```

## Usage
### Running Jupyter Notebooks
To explore the notebooks and run the machine learning models, use:
```bash
jupyter notebook
```

### Training Models
The training scripts and notebooks in the `notebooks_results/` directory allow you to train models using preprocessed data.

### Evaluating Results
Evaluation results, including performance metrics and feature importance analysis, can be found in the `results_notebook/` directory.

## Machine Learning Models Used
- **Logistic Regression** - Baseline model
- **Random Forest** - Ensemble learning method
- **XGBoost** - Optimized gradient boosting
- **Blending Ensemble** - Combination of multiple models for improved performance

## Contributions
If you would like to contribute to this project, feel free to fork the repository and submit a pull request.

## License
This project is open-source and available under the MIT License.

### ** MUSIC Dataset: Sudden Cardiac Death in Chronic Heart Failure**

#### **Overview**
The **MUSIC dataset** is a publicly available medical dataset from **PhysioNet**, containing **clinical data from 992 patients** with **chronic heart failure (CHF)**. It includes **103 variables**, covering demographics, vital signs, lab results, medical history, and medications.

#### **Dataset Source**
- **Name:** MUSIC (Muerte Súbita en Insuficiencia Cardíaca Crónica)  
- **Source:** [PhysioNet](https://physionet.org/)  
- **Access:** Free for research and educational purposes  

#### **Key Features**
The dataset contains **numerical and categorical features**, categorized into:
1. **Patient Demographics** – Age, gender, patient ID.
2. **Clinical Follow-up** – Study duration, patient exit, cause of death.
3. **Target Variable (Multiclass Classification)** – Patients classified into **four categories**:
   - `0` → Survivor (Alive)
   - `1` → Non-cardiac death
   - `2` → Sudden Cardiac Death (SCD)
   - `3` → Pump failure death
4. **Vital Signs & Lab Results** – Blood pressure, BMI, heart rate, key lab test values (e.g., Troponin, Creatinine).
5. **Medical History & Risk Factors** – Diabetes, hypertension, prior myocardial infarction.
6. **Medications** – Beta blockers, ACE inhibitors, diuretics, anticoagulants.

#### **Objective of Machine Learning Model**
The goal is to develop a **multiclass classification model** to predict the **cause of death** based on clinical features.  
- **Target Variable:** `Cause of death` (four categories)
- **Approach:** Supervised Machine Learning (e.g., Logistic Regression, Random Forest, XGBoost)
- **Evaluation Metrics:** Accuracy, Precision, Recall, F1-Score  

This README provides an overview of the dataset and project objectives, ensuring clarity for researchers and developers working on predictive modeling for heart failure outcomes. 


