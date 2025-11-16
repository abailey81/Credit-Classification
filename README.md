# Credit Classification

Supervised learning project to predict whether a loan will default using tabular customer and loan features. The aim is to build a clear, reproducible baseline credit-risk model that can be extended to more advanced approaches.

## 1. Overview

This repository contains a small end-to-end workflow for loan default prediction:

* Exploratory data analysis of the loan dataset
* Data cleaning and feature engineering
* Training and evaluation of supervised learning models
* Interpretation of model performance and limitations

The work was originally developed as part of a university assignment, but the structure is organised to resemble a real data science project rather than a single notebook.

## 2. Data

The project assumes a single CSV file with one row per loan and a binary target variable indicating default vs non-default, together with customer and loan attributes.

The dataset is stored locally and not committed to the repository. A typical local layout is:

* `data/raw/dataset.csv` – original dataset
* `data/processed/` – any cleaned or engineered versions

You can adjust the paths inside the notebook or scripts if your filenames differ.

## 3. Methodology

The modelling workflow follows a standard supervised learning pipeline for credit risk:

1. **Preprocessing and feature engineering**

   * Handling missing values
   * Encoding categorical variables
   * Scaling or normalising numerical features where appropriate

2. **Model training**

   * Baseline models such as logistic regression
   * Optionally, comparison with tree-based methods (for example random forests or gradient boosting)

3. **Evaluation**

   * Train/validation split or cross-validation
   * Metrics including ROC-AUC, accuracy, precision, recall and confusion matrices
   * Qualitative discussion of where the model performs well or poorly

Most of the experimentation currently lives in `notebooks/Loan prediction.ipynb`. As the project evolves, more logic can be refactored into reusable modules under `src/`.

## 4. Repository structure

```text
.
├── notebooks/          # Jupyter notebooks for exploration and modelling
│   └── Loan prediction.ipynb
├── src/                # Python modules (data prep, training, evaluation)
├── requirements.txt    # Python dependencies
├── .gitignore          # Ignore rules (data, caches, IDE files, etc.)
└── README.md           # Project documentation
```

The `data/`, `report/` and `docs/` folders are expected to exist locally but are not tracked by git, so they do not appear in the GitHub view.

## 5. Getting started

1. **Clone the repository**

   ```bash
   git clone git@github.com:abailey81/Credit-Classification.git
   cd Credit-Classification
   ```

2. **(Optional) Create and activate a virtual environment**

   ```bash
   python -m venv .venv
   source .venv/bin/activate    # macOS / Linux
   # .venv\Scripts\activate     # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Add the dataset**

   Place your CSV in `data/raw/dataset.csv` (or update the notebook path accordingly).

5. **Run the analysis**

   ```bash
   jupyter notebook notebooks/Loan\ prediction.ipynb
   ```

   From there you can reproduce the analysis, adjust features, or try alternative models.

## 6. Reproducibility and next steps

* Dependencies are listed in `requirements.txt`.
* Data files are kept out of version control to avoid exposing sensitive information.
* Random seeds can be fixed in the notebook to make results more stable between runs.

Planned improvements include refactoring more code into `src/`, adding configuration files for experiments, logging model outputs, and extending evaluation to include calibration, scorecards and monitoring.
