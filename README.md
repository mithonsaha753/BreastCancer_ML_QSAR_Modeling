# 🧬 Machine Learning-Driven QSAR Modeling & Virtual Screening for CDK1/AURKA Inhibitors

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

This repository provides the reproducible machine learning-driven Quantitative Structure-Activity Relationship (ML-QSAR) pipeline developed to identify novel, potent inhibitors against **Cyclin-Dependent Kinase 1 (CDK1)** and **Aurora Kinase A (AURKA)** in breast cancer therapeutics.

---

## 📌 Workflow Highlights
* **Data Curation:** Automated ChEMBL data extraction (Target IDs: `CHEMBL308`, `CHEMBL4722`), salt stripping, and bioactivity normalization ($pIC_{50}$).
* **Feature Representation:** Hybrid descriptors combining 1024-bit Morgan Fingerprints (ECFP4) and RDKit physicochemical properties.
* **Model Optimization:** Automated Bayesian hyperparameter tuning via **Optuna** for XGBoost, LightGBM, Random Forest, and a Stacking Ensemble Regressor.
* **Validation (OECD Compliant):**
  * 5-fold cross-validation ($Q^2_{cv}$) & external test set validation ($R^2_{test}$).
  * Model robustness verification via **Y-Randomization** ($cR_p^2$).
  * **Applicability Domain (AD)** defined via Leverage analysis and **Williams Plot**.
* **Model Explainability:** Feature impact assessment using **SHAP (SHapley Additive exPlanations)**.
* **Virtual Screening:** Sequential screening cascade of seaweed-derived metabolites prioritizing potent dual-target lead candidates.

---
This computational pipeline was adapted and extended from the ML-QSAR framework established by Ali et al. (*Digital Discovery*, 2026, https://doi.org/10.1039/d6dd00045b). We gratefully acknowledge the authors for their open-science contribution.

---

## 📂 Repository Structure
```text
├── ML_QSAR_CDK1.ipynb       # Main reproducible workflow for CDK1
├── ML_QSAR_AURKA.ipynb      # Reproducible workflow for AURKA
├── requirements.txt         # Environment dependencies
├── data/                    # Curated ChEMBL datasets & seaweed screening library
└── figures/                 # Parity plots, Williams plot, SHAP summary plots
