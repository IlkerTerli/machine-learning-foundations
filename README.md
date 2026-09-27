# Machine Learning Foundations

This repository contains two introductory machine learning projects developed as part of a university course.

The projects represent my first practical application of machine learning workflows and cover two major supervised learning tasks:

- classification
- regression

The repository contains a larger classification project based on the Breast Cancer Wisconsin (Diagnostic) dataset and a smaller regression project based on the Boston Housing dataset.

The notebooks document the workflow from data exploration and preprocessing to model training, evaluation, visualization, and interpretation.

---

## Projects

### 1. Breast Cancer Classification

The main project focuses on binary classification using the Breast Cancer Wisconsin (Diagnostic) dataset.

The goal is to classify observations as malignant or benign based on numerical diagnostic features.

Main steps:

- data loading and exploration
- target-variable preparation
- data-quality checks
- exploratory data analysis
- outlier analysis using the IQR method
- correlation analysis
- dimensionality reduction with PCA
- train-test split
- feature scaling
- Logistic Regression baseline
- confusion matrix
- precision, recall, and F1-score evaluation
- ROC curve and AUC
- Random Forest comparison
- feature importance analysis
- hyperparameter tuning with GridSearchCV
- 5-fold cross-validation

Models used:

- Logistic Regression
- Random Forest Classifier

The Logistic Regression model achieved approximately 98% classification accuracy on the test set.

A 5-fold cross-validation resulted in a mean accuracy of approximately:

```text
0.9802
```

The project also demonstrates how preprocessing can be integrated into a scikit-learn `Pipeline` to avoid data leakage during cross-validation and hyperparameter optimization.

Notebook:

```text
breast_cancer_classification/breast_cancer_classification.ipynb
```

Dataset:

```text
breast_cancer_classification/data/data.csv
```

---

### 2. Boston Housing Regression

The second project demonstrates a basic regression workflow using the Boston Housing dataset.

The goal is to predict the target variable `medv` using several numerical housing and regional features.

Main steps:

- data loading and exploratory analysis
- feature and target separation
- train-test split
- Linear Regression
- RMSE calculation
- R-squared evaluation
- predicted-vs-actual visualization
- analysis of the relationship between room count and the target variable
- discussion of possible model improvements

Model used:

- Linear Regression

The model achieved approximately:

```text
RMSE:      4.84
R-squared: 0.74
```

The project serves as a baseline regression example and illustrates how model predictions can be evaluated numerically and visually.

Notebook:

```text
boston_housing_regression/boston_regression.ipynb
```

Dataset:

```text
boston_housing_regression/data/train.csv
```

---

## Repository Structure

```text
machine-learning-foundations/
|
|-- breast_cancer_classification/
|   |-- breast_cancer_classification.ipynb
|   `-- data/
|       `-- data.csv
|
|-- boston_housing_regression/
|   |-- boston_regression.ipynb
|   `-- data/
|       `-- train.csv
|
|-- .gitignore
|-- requirements.txt
`-- README.md
```

---

## Machine Learning Methods

The projects use several common machine learning and data-analysis techniques.

### Data Preparation

- pandas for data handling
- train-test splitting
- feature scaling with `StandardScaler`
- target-variable preparation
- basic data-quality checks

### Exploratory Data Analysis

- descriptive statistics
- histograms
- boxplots
- correlation analysis
- scatter plots

### Classification

- Logistic Regression
- Random Forest
- confusion matrix
- precision
- recall
- F1-score
- ROC curve
- AUC

### Regression

- Linear Regression
- Root Mean Squared Error (RMSE)
- coefficient of determination (R-squared)

### Model Validation

- train-test split
- 5-fold cross-validation
- GridSearchCV
- scikit-learn pipelines

### Dimensionality Reduction

- Principal Component Analysis (PCA)

---

## Technologies

The projects were implemented in Python using Jupyter notebooks.

Main libraries:

- Python
- NumPy
- pandas
- matplotlib
- seaborn
- scikit-learn
- JupyterLab

The exact package versions used for the repository are documented in `requirements.txt`.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/IlkerTerli/machine-learning-foundations.git
```

Navigate to the project directory:

```bash
cd machine-learning-foundations
```

Install the required Python packages:

```bash
pip install -r requirements.txt
```

Then start JupyterLab:

```bash
jupyter lab
```

Alternatively, the notebooks can be opened directly in Visual Studio Code with Jupyter support.

---

## Reproducibility

Both notebooks use fixed random seeds where applicable.

For example:

```python
random_state=42
```

This allows data splits and selected model results to be reproduced consistently.

The Breast Cancer project additionally uses scikit-learn pipelines during cross-validation and hyperparameter tuning so that preprocessing is performed independently within each training fold.

---

## Notes on the Datasets

### Breast Cancer Wisconsin Dataset

The Breast Cancer Wisconsin dataset is used here solely for educational machine learning purposes.

The resulting model is a demonstration of classification methods and is not intended for clinical or medical decision-making.

### Boston Housing Dataset

The Boston Housing dataset is a historical dataset that has frequently been used for teaching regression techniques.

It is included here as a legacy educational dataset because this project was originally created as an introductory machine learning exercise.

The dataset contains historically problematic demographic variables and should therefore not be interpreted as a suitable modern dataset for real-world housing-policy applications.

---

## Project Context

These projects were created as part of my first practical machine learning coursework.

The larger Breast Cancer classification project demonstrates a more complete machine learning workflow, including exploratory analysis, multiple models, validation, and hyperparameter optimization.

The smaller Boston Housing project focuses on the fundamentals of regression and model evaluation.

Together, the projects document my progression from introductory supervised learning concepts toward more structured machine learning workflows.