# ML_Prediction_of_Cause_of_Death_in_CHF


## Overview
ML_Prediction_of_Cause_of_Death_in_CHF is a machine learning project designed to analyze and model data using various machine learning techniques. The project includes data preprocessing, exploratory data analysis (EDA), feature engineering, model training, and evaluation.

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

###  Model Results Summary (after data balancing)

####  Random Forest
- Accuracy: **0.84**
- Macro F1-score: **0.59**
- Class-wise Performance:
  - Class 0 (Alive): Precision **0.97**, Recall **0.96**, F1 **0.96**
  - Class 1 (SCD): Precision **0.50**, Recall **0.17**, F1 **0.25**
  - Class 2 (Non-CVD): Precision **0.45**, Recall **0.68**, F1 **0.54**
  - Class 3 (Other CVD): Precision **0.62**, Recall **0.59**, F1 **0.60**

####  Voting Classifier (Ensemble)
- Accuracy: **0.85**
- Macro F1-score: **0.63**
- Class-wise Performance:
  - Class 0 (Alive): Precision **0.95**, Recall **0.98**, F1 **0.96**
  - Class 1 (SCD): Precision **0.67**, Recall **0.33**, F1 **0.44**
  - Class 2 (Non-CVD): Precision **0.52**, Recall **0.58**, F1 **0.55**
  - Class 3 (Other CVD): Precision **0.57**, Recall **0.55**, F1 **0.56**

---

###  Interpretation
-  Both models improved compared to the imbalanced version, especially in minority class recall and F1-score.
-  **Class 1 (SCD)** performance remains challenging, but **recall increased from 0.07 → 0.33**.
-  Voting ensemble outperforms Random Forest slightly on macro-averaged metrics and class balance.

---

###  Conclusion
Balancing the dataset significantly improved model fairness across classes. The **Voting Classifier** is currently the best performing model in terms of **balanced accuracy and F1-score**, making it suitable for multiclass prediction in a medical context.




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


