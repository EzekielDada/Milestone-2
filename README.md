# PCA Analysis for Cancer Dataset - Milestone 2 Assignment

## Project Overview

This project demonstrates Principal Component Analysis (PCA) on the breast cancer dataset from sklearn to identify essential variables for the Anderson Cancer Center. The analysis aims to support donor funding decisions by revealing which diagnostic features are most critical for cancer diagnosis.

**Dataset**: Breast Cancer Dataset (30 features, 569 samples from sklearn.datasets)  
**Objective**: Reduce dimensionality to 2 principal components and implement predictive model

---

## Features

### Core Requirements
✅ **PCA Implementation** - Applies Principal Component Analysis to the cancer dataset  
✅ **Dimensionality Reduction** - Reduces 30 features to 2 principal components  
✅ **Bonus: Logistic Regression** - Trains predictive model using PCA components  

### Analysis Includes
- Dataset exploration and statistical summary
- Data standardization (required for PCA)
- Variance analysis and explained variance visualization
- Feature loadings analysis (which features contribute most to each component)
- PCA results visualization in 2D space
- Model evaluation with accuracy, precision, recall, and F1-score
- Confusion matrix and detailed classification report

---

## Installation & Setup

### Requirements
- Python 3.7 or higher
- Jupyter Notebook
- Required packages: numpy, pandas, scikit-learn, matplotlib, seaborn

### Install Dependencies

```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```

---

## Running the Analysis

### Option 1: Run Jupyter Notebook (Recommended)

```bash
jupyter notebook pca_cancer_analysis.ipynb
```

Then click through each cell from top to bottom to execute the analysis.

### Option 2: Run All Cells at Once

```bash
jupyter nbconvert --to notebook --execute --inplace pca_cancer_analysis.ipynb
```

---

## Project Structure

```
MILESTONE 2/
├── pca_cancer_analysis.ipynb    # Main analysis notebook
├── README.md                      # This file
```

---

## Notebook Sections Explained

### 1. Import Required Libraries
Loads all necessary Python packages for data manipulation, machine learning, and visualization.

### 2. Load and Explore the Cancer Dataset
- Loads the breast cancer dataset from sklearn
- Displays dataset shape, features, and target distribution
- Lists all 30 features used in the analysis

### 3. Data Preprocessing and Standardization
- Checks for missing values
- Standardizes features using StandardScaler
- Prepares data for PCA (critical: PCA requires standardized data)

### 4. Implement PCA with 2 Components
- Applies PCA reducing 30 features to 2 components
- Demonstrates 93% dimensionality reduction
- Preserves approximately 63% of original variance

### 5. Visualize PCA Results
- Scatter plot showing data separation in 2D PCA space
- Points color-coded by target class (malignant vs benign)
- Shows explained variance for each component

### 6. Analyze Principal Components
- **Explained Variance Ratio**: Shows percentage of variance captured by each component
- **Feature Loadings**: Identifies which original features contribute most to each principal component
- **Visualization**: Bar charts of feature contributions and cumulative variance plot

### 7. Logistic Regression for Prediction (Bonus)
- Trains logistic regression model using 2 PCA components
- Splits data into 70% training, 30% testing
- Demonstrates that reduced dimensions maintain predictive power

### 8. Model Evaluation and Results
- Calculates accuracy, precision, recall, and F1-score
- Presents confusion matrix analysis
- Visualizes model performance metrics
- Detailed classification report for both cancer classes

### Summary and Conclusions
- Key findings and recommendations
- Practical implications for the cancer center

---

## Key Results & Interpretation

### Dimensionality Reduction
- **Original Features**: 30
- **Reduced Components**: 2
- **Reduction Rate**: 93.33%
- **Variance Preserved**: ~63% (PC1 + PC2)

### Model Performance (Typical)
- **Test Accuracy**: ~95%+ (varies with random seed)
- **Precision**: High confidence in positive predictions
- **Recall**: Effectively identifies most positive cases
- **F1-Score**: Balanced measure of precision and recall

### Essential Variables
The analysis identifies that certain features (e.g., worst radius, worst texture, worst area) are the primary drivers of cancer diagnosis classification.

---

## Understanding PCA

**What is PCA?**
Principal Component Analysis is a dimensionality reduction technique that:
1. Identifies directions (principal components) of maximum variance in data
2. Projects data onto these new axes
3. Reduces feature count while preserving important information

**Why Use PCA?**
- Simplifies high-dimensional data
- Reduces computational cost
- Helps identify the most important features
- Improves model interpretability
- Reduces overfitting risk

**How PCA Works in This Project:**
1. Standardizes all 30 features to mean=0, std=1
2. Computes the covariance matrix
3. Finds the 2 eigenvectors with largest eigenvalues
4. Projects data onto these 2 new axes (PC1, PC2)

---

## Key Concepts Demonstrated

### Standardization (Why It Matters)
Features with larger scales would dominate PCA. StandardScaler ensures all features contribute equally.

### Variance Explained
- PC1 explains approximately 45% of variance
- PC2 explains approximately 19% of variance
- Together, ~63% of information is retained with 93% fewer dimensions

### Feature Loadings
Shows the contribution of original features to each principal component. Features with high loadings are most important.

### Model Validation
Using a test set ensures the model generalizes to unseen data, not just memorizing training data.

---

## Coding Standards & Best Practices

✓ Clear variable naming conventions  
✓ Comprehensive comments explaining each step  
✓ Logical flow from data loading to model evaluation  
✓ Proper handling of train/test splits  
✓ Visualizations for better understanding  
✓ Efficient use of sklearn utilities  
✓ Proper error handling and data validation  

---

## Troubleshooting

**Issue**: Jupyter notebook won't run
- **Solution**: Ensure all packages are installed: `pip install -r requirements.txt`

**Issue**: Plots not displaying
- **Solution**: Ensure `%matplotlib inline` is set (usually automatic in Jupyter)

**Issue**: Different results on each run
- **Solution**: Random seed is set to 42 in the code for reproducibility

---

## Assignment Checklist

- [x] PCA implementation on cancer dataset
- [x] Dimensionality reduction to 2 components
- [x] Variance analysis and visualization
- [x] Feature importance identification
- [x] Bonus: Logistic regression model
- [x] Bonus: Model evaluation metrics
- [x] Visualizations (PCA scatter, loadings, confusion matrix, metrics)
- [x] Comprehensive README with instructions
- [x] Coding standards and best practices
- [x] Clear, logical code structure

---

## References

- [Scikit-learn PCA Documentation](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html)
- [Breast Cancer Dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html)
- [Principal Component Analysis Theory](https://en.wikipedia.org/wiki/Principal_component_analysis)

---

## Author Notes

This analysis demonstrates how dimensionality reduction can effectively simplify complex medical datasets while maintaining their predictive power. The reduced feature space makes the model more interpretable and computationally efficient—key advantages for a healthcare institution.

The identified essential variables can help guide research priorities and funding allocation at the Anderson Cancer Center.

---

**Assignment**: Milestone 2 - PCA Analysis  
**Date**: 2026  
**Status**: Complete ✓
