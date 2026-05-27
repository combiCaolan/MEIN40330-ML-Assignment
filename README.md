# ALL vs AML Leukemia Classification
### Machine Learning Mini-Project

<p align="center">
  <img src="assets/banner.png" width="48%" alt="Project graphic"/>
  &nbsp;
  <img src="https://www.kaggle.com/static/images/site-logo.png" width="48%" alt="Kaggle"/>
</p>

---

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF?style=flat&logo=kaggle&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat)

---

## Project Overview

**Research Question:**
> Can we classify ALL vs AML leukemia subtypes using gene expression data, and which genes are most informative for distinguishing them?

This project integrates two data types:
- **Gene expression data** (~7,000 gene measurements per patient) — the omics layer
- **Cancer subtype labels** (ALL or AML) — the clinical layer

---

## Dataset

- **Source:** [Golub et al. (1999) — Kaggle](https://www.kaggle.com/datasets/crawford/gene-expression)
- **Samples:** 72 patients (38 training, 34 test)
- **Features:** 7,129 gene expression measurements per sample
- **Classes:** ALL (Acute Lymphoblastic Leukemia) vs AML (Acute Myeloid Leukemia)

---

## Methods

| Step | Method | Purpose |
|------|--------|---------|
| Preprocessing | Normalisation, variance filtering | Clean and reduce the feature space |
| Feature Selection | Variance threshold + classifier importance | Identify informative genes |
| Unsupervised | PCA | Explore natural structure in the data |
| Supervised | Random Forest / SVM | Classify ALL vs AML |
| Evaluation | Accuracy, confusion matrix, ROC curve | Assess model performance |

---

## Repository Structure

```
├── assets/                # Images and graphics (banner.png etc.)
├── data/                  # Raw data downloaded via Kaggle API
├── notebook.ipynb         # Main Jupyter Notebook (analysis + report)
├── README.md
└── requirements.txt       # Python dependencies
```

---

## Requirements

```
kaggle
pandas
numpy
scikit-learn
matplotlib
seaborn
scipy
jupyter
```

Install with:
```bash
pip install -r requirements.txt
```

---

## Usage

1. Set up Kaggle API credentials (`~/.kaggle/kaggle.json`)
2. Run the notebook:
```bash
jupyter notebook notebook.ipynb
```

---

## Report Structure

The Jupyter Notebook follows the assignment report structure:
1. **Background** — omics data, leukemia subtypes, research question, methods
2. **Results** — PCA plot, classifier performance, top informative genes, conclusion
3. **Methods/Code** — well-commented Python code throughout

---

## References

- Golub, T.R. et al. (1999). *Molecular Classification of Cancer: Class Discovery and Class Prediction by Gene Expression Monitoring.* Science, 286(5439), 531–537.
