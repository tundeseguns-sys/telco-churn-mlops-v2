# Telco Customer Churn MLOps

An end-to-end machine learning operations project for predicting customer churn using the IBM Telco Customer Churn dataset.

The project is being developed incrementally using reproducible MLOps practices, including data validation, automated preprocessing, experiment tracking, testing, CI, deployment, monitoring and retraining planning.

## Project objective

The objective is to build a reproducible machine learning system that predicts whether a telecommunications customer is likely to churn.

This project will cover the complete lifecycle:

1. Data ingestion
2. Data inspection and validation
3. Data cleaning
4. Exploratory data analysis
5. Train/test splitting
6. Feature preprocessing
7. Model training and comparison
8. Experiment tracking with MLflow
9. Model evaluation and registration
10. Prediction pipelines
11. Automated testing
12. Pipeline automation
13. Batch predictions
14. FastAPI deployment
15. Dockerisation
16. Monitoring and retraining planning
17. Final documentation and model card

## Technology stack

- Python 3.11
- pandas
- NumPy
- scikit-learn
- JupyterLab
- matplotlib
- MLflow
- pytest
- Ruff
- FastAPI
- Docker
- GitHub Actions

Some tools will be introduced later.

## Project structure

```text
telco-churn-mlops-v2/
│
├── .github/
│   └── workflows/
├── configs/
├── data/
│   ├── raw/
│   ├── interim/
│   └── processed/
├── docs/
├── models/
├── notebooks/
├── reports/
│   └── figures/
├── scripts/
├── src/
│   └── telco_churn/
│       ├── data/
│       ├── features/
│       ├── models/
│       ├── pipelines/
│       └── utils/
├── tests/
├── .gitignore
├── README.md
├── requirements.in
├── requirements.txt
├── requirements-dev.in
└── requirements-dev.txt
```

## Data policy

The original dataset is stored locally in:

```text
data/raw/
```

Raw, interim and processed datasets are excluded from Git because data files should not normally be stored directly in the source-code repository.

The original raw file will be preserved unchanged.

Generated datasets will be stored separately:

```text
data/interim/
data/processed/
```

## Local environment setup

Clone the repository:

```cmd
git clone https://github.com/tundeseguns-sys/telco-churn-mlops-v2.git
cd telco-churn-mlops-v2
```

Create the virtual environment:

```cmd
py -3.11 -m venv .venv
```

Activate it in Windows CMD:

```cmd
.venv\Scripts\activate
```

Install the complete development environment:

```cmd
python -m pip install --upgrade pip
python -m pip install -r requirements-dev.txt
```

Verify the environment:

```cmd
python -c "import pandas, sklearn; print(pandas.__version__); print(sklearn.__version__)"
```

## Dependency management

Direct dependencies are declared in:

```text
requirements.in
requirements-dev.in
```

Locked dependencies are generated in:

```text
requirements.txt
requirements-dev.txt
```

The generated lock files should not be edited manually.

## Current project status

- Project setup and folder structure — completed
- Git and environment setup — completed
- Data ingestion — next