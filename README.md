# PCA Analysis - Cancer Dataset
## Milestone 2 Assignment

## Overview

This project uses Principal Component Analysis (PCA) on the breast cancer dataset from sklearn. The dataset has 30 features and 569 samples. The goal is to reduce it down to 2 principal components to identify the most essential variables, which can support donor funding decisions at the Anderson Cancer Center.

A logistic regression model is also included as the bonus requirement.

---

## Requirements

- Python 3.7 or higher
- numpy
- pandas
- scikit-learn
- matplotlib
- seaborn
- jupyter

Install everything at once:

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```

---

## How to Run

1. Open a terminal in the project folder
2. Launch Jupyter Notebook:

```bash
jupyter notebook pca_cancer_analysis.ipynb
```

3. Run each cell from top to bottom (Cell > Run All, or Shift+Enter through each cell)

---

## Project Structure

```
MILESTONE 2/
├── pca_cancer_analysis.ipynb   # Main analysis notebook
├── requirements.txt            # Required packages
└── README.md                   # This file
```

---

## Notebook Contents

1. **Import Libraries** - loads numpy, pandas, sklearn, matplotlib, seaborn
2. **Load Dataset** - loads breast cancer dataset and explores its structure
3. **Preprocessing** - standardizes features with StandardScaler before PCA
4. **PCA Implementation** - reduces 30 features to 2 principal components
5. **Visualization** - scatter plot showing the 2D PCA separation by class
6. **Component Analysis** - variance explained and feature loadings per component
7. **Logistic Regression (Bonus)** - trains a classifier using the 2 PCA components
8. **Model Evaluation** - accuracy, precision, recall, F1-score, confusion matrix

---

## Results

- PCA reduces the dataset from 30 features to 2 components
- The 2 components together capture roughly 63% of the total variance
- Logistic regression on the reduced data achieves around 95% accuracy on the test set
