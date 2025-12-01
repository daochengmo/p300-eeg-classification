# P300 EEG Classification

This project builds a full end-to-end pipeline for classifying P300 event-related potentials (ERP) using EEG data.  
It includes preprocessing, epoch extraction, feature construction, model training, cross-validation, and visualization.

Although this project is based on neurocognitive signal data, the analytic workflow reflects general skills relevant to data science and research assistant work:
- cleaning and structuring raw data  
- implementing reproducible analysis pipelines  
- evaluating models through cross-validation  
- documenting results clearly and visually  

---

## 📘 Project Overview

The goal is to distinguish **target vs. non-target** ERP responses using classical machine-learning models (LDA, Logistic Regression).  
The pipeline is modular and organized to reflect best practices in reproducible analysis.

---

## 📂 Repository Structure

```
p300-eeg-classification/
│
├── notebook/
│   └── p300_classification.ipynb        # main analysis notebook
│
├── src/
│   ├── preprocessing.py                 # filtering, epoching, baseline correction
│   ├── feature_extraction.py            # time-window features
│   ├── modeling.py                      # LDA / Logistic Regression pipelines
│   └── utils.py                         # helpers, plotting, CV functions
│
├── results/
│   ├── figures/                         # ROC curves, coefficient plots, etc.
│   └── metrics_summary.csv              # cross-validation metrics
│
└── README.md
```


---

## 🧠 Methods

### 1. Preprocessing
- Epoch extraction  
- Baseline correction  
- Channel selection  
- Exclusion of low-quality trials  

### 2. Feature Engineering
- Mean amplitude in P300 window (300–600 ms)  
- Optional multichannel concatenation  
- Standardization with scikit-learn  

### 3. Modeling
Models:
- **LDA**
- **Logistic Regression**

### 4. Evaluation
- Stratified cross-validation  
- ROC curves per fold  
- Average AUC  
- Confusion matrices  

---

## 📈 Sample Results

Example:
Average AUC ≈ 0.84
Std ≈ 0.06

(Additional figures included in `results/figures/`.)

---

## 🔧 Technologies Used

- Python  
- pandas / NumPy  
- scikit-learn  
- Matplotlib  
- MNE (partial)

---

## 📄 Notes

Dataset is not included due to licensing restrictions.  
All code and analysis steps are fully reproducible with comparable ERP data.

---

## 📬 Contact

Daocheng (Jacky) Mo  
Learning Analytics @ Teachers College, Columbia University  
dm4096@tc.columbia.edu  

