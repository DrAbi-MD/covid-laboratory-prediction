# Are COVID-19 Laboratory-Based Prediction Models Reproducible?

# A Methodological Reproduction of Cabitza et al.

A reproducible clinical machine-learning project evaluating whether published machine-learning models for predicting COVID-19 status from routinely available laboratory and demographic data can be reproduced using the publicly available dataset.

# Project Overview

This project is a methodological reproduction of the machine-learning study by Cabitza et al., Development, evaluation, and validation of machine learning models for COVID-19 detection based on routine blood tests

The primary objective is to reproduce the reported modelling approach, compare reproduced performance with the published findings, and assess model performance across development, internal-external, and historical external validation.

The available dataset contains 1,736 observations, comprising:

- 1,624 OSR development cases
- 58 IOG internal-external validation cases
- 54 historical external validation cases

The reproduction uses 34 predictors corresponding to the COVID-specific feature set.

# Reproduction Workflow

1. Dataset and cohort reconstruction
2. Data-quality and missing-data assessment
3. K-nearest-neighbour imputation (k = 5)
4. Feature normalization
5. Recursive Feature Elimination (RFE)
6. Stratified 80:20 development/hold-out splitting
7. Five-fold stratified cross-validation
8. Hyperparameter optimization
9. Model development
10. Hold-out performance evaluation
11. Internal-external validation
12. Historical external validation
13. Published-versus-reproduced comparison
14. Model interpretation and reproducible reporting

# Models

The five machine-learning classifiers evaluated in the original study are being reproduced:

- Logistic Regression
- Random Forest
- K-Nearest Neighbours
- Naive Bayes
- Support Vector Machine

Logistic Regression and Random Forest have currently been reproduced and validated.

# Current Results

Development performance was broadly comparable with the published COVID-specific models.

| Model | Published AUC | Reproduced AUC |
| --- | ---: | ---: |
| Logistic Regression | 0.83 | 0.877 |
| Random Forest | 0.84 | 0.881 |

During internal-external validation, mean AUC was 0.895 for Logistic Regression and 0.836 for Random Forest.

On the 54 historical COVID-negative external cases, specificity was 90.7% for Logistic Regression and 98.1% for Random Forest.

Detailed results and interpretation are available in `results/reproduction/`.

# Reproducibility Approach

This project aims for methodological reproduction rather than exact computational replication.

Some details of the original implementation, including the complete hyperparameter search spaces, are not publicly available. Where necessary, implementation decisions are specified independently and documented transparently.

Published and reproduced results are compared to identify both similarities and areas of difference.

# Repository Structure

```text
covid-laboratory-prediction/
├── data/
│   ├── raw/
│   ├── processed/
│   └── external/
├── models/
├── notebooks/
├── results/
│   └── reproduction/
├── tests/
├── app/
├── .gitignore
├── README.md
└── requirements.txt
```

# Data

This project uses the publicly available dataset associated with the original study by Cabitza et al.

The dataset contains 1,736 observations and the laboratory and demographic variables required for the reproduction analyses.

To preserve the original source of the data and avoid unnecessary redistribution, the dataset is not duplicated in this repository. Users wishing to reproduce the analyses should obtain the dataset directly from the original public data source.

Original dataset: [INSERT ORIGINAL DATASET LINK]

After downloading, place the dataset as:

```text
data/raw/all_training.csv
```

The `data/` directory is excluded from Git tracking.

# Clinical Prediction Principles

The project prioritizes:

- Prevention of data leakage
- Reproducible preprocessing
- Appropriate handling of missing data
- Transparent hyperparameter optimization
- Discrimination and calibration
- Appropriate internal and external validation
- Transparent comparison with published findings
- Reproducible reporting

# Environment

The project is developed using Python 3.12 in an isolated virtual environment, primarily using pandas, NumPy, scikit-learn, SciPy, imbalanced-learn, and related scientific Python tools.

# Status

Current stage: Logistic Regression and Random Forest reproduction completed, including development hold-out, internal-external validation, and historical external validation.

Next: Reproduction and validation of K-Nearest Neighbours, Naive Bayes, and Support Vector Machine, followed by complete five-model comparison.

# Author

Israel Oheji Abi, MBBS, MSPH, MD (Orthopaedics & Trauma)

Physician-AI-Scientist | AI in Orthopaedics & Spine | AI in Healthcare| Digital Health technologies

GitHub: https://github.com/DrAbi-MD
