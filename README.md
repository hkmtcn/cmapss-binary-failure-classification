# cmapss-binary-failure-classification
Binary failure classification on NASA C-MAPSS with ML &amp; DL.


# Predictive Maintenance in Aircraft Engine Maintenance Using the C-MAPSS Dataset: Performance Comparison and Evaluation of Machine Learning Classification Algorithms

## Abstract
This study assesses classification-based predictive maintenance (PdM) for aircraft engines on the NASA Commercial Modular Aero-Propulsion System Simulation dataset and addresses the lack of wide-scope, unified benchmarks. PdM is cast as a short-term binary task – predicting whether an engine will fail within the next 30 cycles – and a comparison is conducted across 10 machine learning models (Logistic Regression, Decision Tree, Random Forest, Support Vector Machine, k-Nearest Neighbor, Naïve Bayes, Extreme Gradient Boosting, LightGBM, CatBoost, and Gradient Boosting) and 3 deep learning models (Multilayer Perceptron, Gated Recurrent Unit, and Long Short-Term Memory). A leakage-aware pipeline applies Min–Max scaling; class imbalance is handled with Synthetic Minority Over sampling Technique where appropriate; hyperparameters are tuned via GridSearchCV/BayesSearchCV; and performance is reported with accuracy, precision, recall, F1-score, and receiver operating characteristic–area under the curve (ROC–AUC), complemented by Shapley Additive Explanations (SHAP) explainability and nonparametric significance tests. Sequence models delivered the strongest performance: LSTM achieved Accuracy = 0.981 (Macro-F1 = 0.92; ROC–AUC = 0.96), and GRU achieved ROC–AUC = 0.97 with Accuracy = 0.975. Among classical learners, LightGBM reached Accuracy = 0.972 (Macro-F1 = 0.86; ROC–AUC = 0.93). These gains over weaker baselines were statistically significant across folds. Framing PdM as near-term failure classification yields operationally interpretable alerts. Models that explicitly capture temporal dependencies (GRU/LSTM) best track short-horizon failure dynamics, while gradient boosted trees offer competitive, lightweight alternatives. The benchmark and analysis (including SHAP) provide a reproducible reference for model selection in aviation PdM.
---

## Keywords
Aircraft engines, C-MAPSS, Classification Algorithms, Machine Learning, Model Comparison, Performance Analysis, Predictive Maintenance.
---

## Cite APA

Özcan, H. (2026). Predictive maintenance in aircraft engine maintenance using the C-MAPSS dataset: performance comparison and evaluation of machine learning classification algorithms. Artificial Intelligence for Engineering Design, Analysis and Manufacturing, 40, e4. doi:10.1017/S0890060426100249
---

## Cite BibteX


@article{Özcan_2026, title={Predictive maintenance in aircraft engine maintenance using the C-MAPSS dataset: performance comparison and evaluation of machine learning classification algorithms}, volume={40}, DOI={10.1017/S0890060426100249}, journal={Artificial Intelligence for Engineering Design, Analysis and Manufacturing}, author={Özcan, Hikmetcan}, year={2026}, pages={e4}}
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


