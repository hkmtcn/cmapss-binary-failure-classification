# cmapss-binary-failure-classification
Binary failure classification on NASA C-MAPSS with ML &amp; DL.


# Predictive Maintenance in Aircraft Engine Maintenance Using the C-MAPSS Dataset: Performance Comparison and Evaluation of Machine Learning Classification Algorithms

## Abstract
Objective. This study assesses classification‐based predictive maintenance (PdM) for aircraft engines on the NASA C ‐MAPSS dataset and addresses the lack of wide‐scope, unified benchmarks.
Methods. PdM is cast as a short‐term binary task—predicting whether an engine will fail within the next 30 cycles—and a comparison is conducted across 10 machine‐learning models (logistic regression, decision tree, random forest, SVM, KNN, Naïve Bayes, XGBoost, LightGBM, CatBoost, gradient boosting) and 3 deep‐learning models (MLP, GRU, LSTM). A leakage‐aware pipeline applies Min–Max scaling; class imbalance is handled with SMOTE where appropriate; hyperparameters are tuned via GridSearchCV/BayesSearchCV; and performance is reported with accuracy, precision, recall, F1‐score, and ROC–AUC, complemented by SHAP explainability and non‐parametric significance tests. Results. Sequence models delivered the strongest performance: LSTM achieved Accuracy = 0.981 (Macro‐F1 = 0.92; ROC–AUC = 0.96), and GRU achieved ROC–AUC = 0.97 with Accuracy = 0.975. Among classical learners, LightGBM reached Accuracy = 0.972 (Macro‐F1 = 0.86; ROC–AUC = 0.93). These gains over weaker baselines were statistically significant across folds. Conclusions. Framing PdM as near‐term failure classification yields operationally interpretable alerts. Models that explicitly capture temporal dependencies (GRU/LSTM) best track short‐horizon failure dynamics, while gradient‐boosted trees offer competitive, lightweight alternatives. The benchmark and analysis (including SHAP) provide a reproducible reference for model selection in aviation PdM.
---

## Keywords
Aircraft engines, C-MAPSS, Classification Algorithms, Machine Learning, Model Comparison, Performance Analysis, Predictive Maintenance.
---

## Cite


@article{YourKey2025,
  title   = {Predictive Maintenance in Aircraft Engine Maintenance Using the C-MAPSS Dataset: Performance Comparison and Evaluation of Machine Learning Classification Algorithms},
  author  = {Hikmetcan Özcan},
  year    = {2026},
  journal = {Artificial Intelligence for Engineering Design, Analysis and Manufacturing},
  doi     = {...}
}
---

## Repository Structure

```
.
├─ README.md
├─ LICENSE                # Code under MIT; figures/data artifacts under CC BY 4.0
├─ notebook/             # Reproducible analysis notebooks (Models, analysis)
│ └─ cmapss_binary_failure_classification_notebook.ipynb
```

This repository does not include the C-MAPSS dataset. Please download it externally and point the notebook to your local path.

Download link: https://www.nasa.gov/content/prognostics-center-of-excellence-data-set-repository

After downloading, open the notebook and set the data directory in the first configuration cell.

Note: Follow the dataset provider’s license/terms. Do not upload raw data to this repo.

## Reproducing the Experiments
1. Open:
notebooks/cmapss_binary_failure_classification_notebook.ipynb
2. In the first cell, set:
DATA_DIR (local path where you placed the dataset)
3. Run all cells.
The notebook itself renders metrics tables, ROC curves, confusion matrices, and (optionally) SHAP explanations inline.


