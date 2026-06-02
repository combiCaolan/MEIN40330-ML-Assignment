# AML & ALL Classification via Gene Expression
### Machine Learning Mini-Project

<p align="center">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSlvS6gkhDa4pLpm7frcx_RfjOtN-MGH4Pg2A&s" width="18%" alt="Project graphic"/>
  &nbsp;
  <img src="https://www.kaggle.com/static/images/site-logo.png" width="48%" alt="Kaggle"/>
</p>

---

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF?style=flat&logo=kaggle&logoColor=white)

---

## Overview

Replication of Golub et al. (1999) — one of the most cited papers in computational biology — which demonstrated that gene expression profiling alone could classify leukaemia subtypes. This project applies modern Python tools to the same dataset to classify patients as ALL or AML.

**Research Question:** Can gene expression profiling alone accurately classify leukaemia patients into ALL or AML subtypes, and which genes are most informative for distinguishing between them?

---

## Results

### PCA — Unsupervised Analysis
<p align="center"><img src="results/pca_plot.png" width="70%"/></p>

### Classification — Random Forest & SVM (80/20 Split)
<p align="center"><img src="results/confusion_matrix_rf_8020.png" width="48%"/> <img src="results/confusion_matrix_svm_8020.png" width="48%"/></p>

### Feature Importance — Most Informative Genes
<p align="center"><img src="results/feature_importance.png" width="70%"/></p>

Both models achieved **80% accuracy**, closely replicating the original paper's 85%.

---

## Dataset

- **Source:** [Golub et al. (1999) — Kaggle](https://www.kaggle.com/datasets/crawford/gene-expression)
- **Samples:** 72 patients, 7,071 genes (after AFFX control probe removal)
- **Split:** 80/20 stratified — 57 training, 15 test

---

## Usage

1. Set up Kaggle API credentials (`~/.kaggle/kaggle.json`)
2. Install dependencies: `pip install -r requirements.txt`
3. Run: `jupyter notebook project.ipynb`

---

## References

- Golub, T.R. et al. (1999). *Molecular Classification of Cancer.* Science, 286(5439), 531–537.
- Crawford, J. (2017). *Gene Expression Dataset.* Kaggle.
