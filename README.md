# cmapss-binary-failure-classification
Binary failure classification on NASA C-MAPSS with ML &amp; DL.


# Predictive Maintenance in Aircraft Engine Maintenance Using the C-MAPSS Dataset: Performance Comparison and Evaluation of Machine Learning Classification Algorithms

## Abstract
This study investigates the effectiveness of data-driven predictive maintenance (PdM) approaches in aircraft engine maintenance by systematically comparing the performance of ten widely-used machine learning algorithms (SVM, Decision Tree, KNN, XGBoost, Logistic Regression, Random Forest, Naive Bayes, LightGBM, CatBoost, Gradient Boosting) and three deep-learning model (MLP, GRU, LSTM) on the C-MAPSS dataset. While traditional maintenance methods rely on fixed intervals and can lead to unnecessary costs and safety risks, PdM utilizes real-time sensor data to predict potential failures, allowing timely intervention. The study addresses a critical gap in the literature by offering a comprehensive performance comparison of classification algorithms based on accuracy, precision, recall, and F1-score metrics. The results provide a scientifically grounded reference for selecting appropriate ML models in PdM applications, aiming to optimize operational efficiency, reduce costs, and enhance aviation safety.
---
## Cite


@article{YourKey2025,
  title   = {Predictive Maintenance in Aircraft Engine Maintenance Using the C-MAPSS Dataset: Performance Comparison and Evaluation of Machine Learning Classification Algorithms},
  author  = {Hikmetcan Özcan},
  year    = {2025},
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
notebooks/Statistical_Validation_DL_Imbalance.ipynb
2. In the first cell, set:
DATA_DIR (local path where you placed the dataset)
3. Run all cells.
The notebook itself renders metrics tables, ROC curves, confusion matrices, and (optionally) SHAP explanations inline.


