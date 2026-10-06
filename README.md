# COVID-19 Laboratory-Based Prediction Model

A reproducible clinical machine learning project for developing and evaluating models that predict COVID-19 status from routinely available laboratory and demographic data.

## Project Overview

This project demonstrates an end-to-end clinical machine learning workflow using a publicly available labelled laboratory dataset.

The primary objective is to develop, validate, and interpret machine learning models for predicting COVID-19 status while following principles of reproducible and clinically responsible model development.

## Planned Workflow

1. Data quality assessment
2. Exploratory data analysis
3. Missing-data assessment and preprocessing
4. Target and feature definition
5. Leakage assessment
6. Train/test splitting
7. Baseline logistic regression
8. Machine learning model development
9. Cross-validation and model comparison
10. Performance evaluation
11. Calibration assessment
12. Model interpretability
13. Error analysis
14. Model validation
15. Reproducible reporting

## Clinical Prediction Principles

The project will prioritize:

- Prevention of data leakage
- Reproducible preprocessing
- Appropriate handling of missing data
- Class-imbalance assessment
- Discrimination and calibration
- Clinically meaningful threshold selection
- Transparent model interpretation
- Appropriate validation

## Repository Structure

covid-laboratory-prediction/
|-- data/
|   |-- raw/
|   |-- processed/
|   |-- external/
|-- models/
|-- notebooks/
|-- src/
|-- tests/
|-- app/
|-- .gitignore
|-- README.md
|-- requirements.txt

## Data

The patient-level dataset is intentionally NOT included in this repository.

Raw and processed datasets are excluded from Git tracking to protect data privacy and maintain responsible data-management practices.

## Environment

The project is developed using Python 3.12 in an isolated virtual environment.

Major tools include:

- Python
- pandas
- NumPy
- scikit-learn
- XGBoost
- LightGBM
- CatBoost
- SHAP
- PyTorch
- SciPy
- statsmodels
- lifelines
- scikit-survival
- Optuna

## Status

Project stage: Initial setup and data-quality assessment.

Model development has not yet been performed.

## Author

Israel Oheji Abi, MBBS, MSPH, MD (Orthopaedics & Trauma)

Clinical Researcher | Orthopaedics & Trauma | Health AI | Digital Health

GitHub: https://github.com/DrAbi-MD
