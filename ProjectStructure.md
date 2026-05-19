# Avito Demand Prediction

## Project Overview

This project focuses on predicting the probability that an advertisement posted on Avito, a Russian online classifieds platform, will generate demand or engagement.

The goal is to build a machine learning pipeline that:

- Processes structured and text-based advertisement data
- Engineers predictive features
- Trains multiple machine learning models
- Evaluates business impact
- Provides explainability and insights
- Demonstrates an end-to-end analytics workflow

This repository is structured to simulate a real-world collaborative machine learning project using:

- Jupyter notebooks
- Modular Python code
- GitHub collaboration workflows
- Kanban task management
- Reusable ML pipelines

---

# Business Problem

Online marketplaces like Avito need to determine:

- Which advertisements are likely to succeed
- Which listings require optimization
- How sellers can improve conversion
- How ranking and recommendation systems can be improved

This project predicts advertisement demand using:

- Ad metadata
- Pricing information
- Textual descriptions
- Temporal features
- User-related information

---

# Machine Learning Objective

## Problem Type

Binary Classification

## Target Variable

Ad demand / conversion indicator

## Primary Evaluation Metrics

- ROC-AUC
- F1 Score
- Precision
- Recall

---

# Repository Structure

```bash
avito-demand-prediction/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── submissions/
│
├── notebooks/
│   ├── 01_project_setup.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_preprocessing.ipynb
│   ├── 04_feature_engineering.ipynb
│   ├── 05_baseline_models.ipynb
│   ├── 06_advanced_models.ipynb
│   ├── 07_model_evaluation.ipynb
│   ├── 08_explainability.ipynb
│   ├── 09_business_insights.ipynb
│   └── 10_final_pipeline_demo.ipynb
│
├── src/
│   ├── __init__.py
│   ├── preprocessing.py
│   ├── feature_engineering.py
│   ├── train.py
│   ├── predict.py
│   ├── evaluate.py
│   ├── visualization.py
│   └── utils.py
│
├── models/
├── reports/
├── app/
│   └── streamlit_app.py
│
├── tests/
│
├── requirements.txt
├── README.md
└── Makefile
```

---

# Team Structure

This project is designed for a 3-person team.

| Team Member | Role | Main Focus |
|---|---|---|
| Person 1 | Data Engineer / Feature Engineering | EDA, preprocessing, feature engineering |
| Person 2 | Machine Learning Engineer | Modeling, training, optimization |
| Person 3 | Analytics / Product / Evaluation | Evaluation, explainability, dashboards, business insights |

---

# Notebook Planning

---

# 01_project_setup.ipynb

## Purpose

Initial project setup and dataset understanding.

## Contains

- Project objective
- Dataset description
- Environment setup
- Package imports
- Loading raw datasets
- Verifying schema
- Target variable inspection
- Project roadmap

## Owner

Entire team

---

# 02_eda.ipynb

## Purpose

Exploratory Data Analysis (EDA).

## Contains

### Dataset Exploration

- Shape of train/test sets
- Data types
- Duplicate checks

### Missing Values

- Missing value percentages
- Null visualizations

### Target Analysis

- Target distribution
- Imbalance inspection

### Numerical Features

- Distributions
- Outlier detection
- Correlation heatmaps

### Categorical Features

- Category frequency
- Regional distributions

### Text Exploration

- Title length
- Description length
- Most frequent words

### Initial Business Insights

- Pricing behavior
- Successful ad categories
- Posting trends

## Owner

Person 1

---

# 03_preprocessing.ipynb

## Purpose

Create preprocessing workflow.

## Contains

### Missing Value Handling

- Numerical imputation
- Categorical imputation

### Categorical Encoding

- One-hot encoding
- Label encoding
- Target encoding experiments

### Text Cleaning

- Lowercase conversion
- Punctuation removal
- Stopword removal
- Stemming/Lemmatization

### Date Processing

- Extract month
- Extract weekday
- Extract posting hour

### TF-IDF Vectorization

- Title TF-IDF
- Description TF-IDF

### Train/Test Split

## Important

Reusable preprocessing logic should be moved into:

```python
src/preprocessing.py
```

## Owner

Person 1

---

# 04_feature_engineering.ipynb

## Purpose

Develop predictive features.

## Contains

### Price Features

- Log(price)
- Price bins
- Normalized prices

### User Features

- Ads per user
- Average user price

### Text Features

- Title length
- Description length
- Punctuation counts
- Keyword counts

### Time Features

- Posting weekday
- Weekend indicators

### Statistical Features

- Group aggregations
- Category averages

## Important

Reusable feature logic should be moved into:

```python
src/feature_engineering.py
```

## Owners

Person 1 + Person 2

---

# 05_baseline_models.ipynb

## Purpose

Train baseline machine learning models.

## Contains

### Models

- Logistic Regression
- Decision Tree
- Random Forest

### Evaluation

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

### Cross Validation

## Important

Training logic should be moved into:

```python
src/train.py
```

## Owner

Person 2

---

# 06_advanced_models.ipynb

## Purpose

Train advanced boosting models.

## Contains

### Models

- XGBoost
- LightGBM
- CatBoost

### Hyperparameter Tuning

- GridSearchCV
- RandomizedSearchCV
- Optuna

### Additional Tasks

- Feature selection
- Ensemble experiments
- Model comparison

## Owner

Person 2

---

# 07_model_evaluation.ipynb

## Purpose

Evaluate machine learning and business performance.

## Contains

### Evaluation Metrics

- Confusion Matrix
- ROC Curves
- Precision-Recall Curves
- Threshold optimization

### Error Analysis

- False positives
- False negatives

### Business Interpretation

- Operational implications
- Conversion tradeoffs

## Owner

Person 3

---

# 08_explainability.ipynb

## Purpose

Interpret model behavior and feature importance.

## Contains

- SHAP Analysis
- Feature Importance
- Partial Dependence Plots
- Local explanations

### Business Recommendations

- What improves ad success
- Key conversion drivers

## Owner

Person 3

---

# 09_business_insights.ipynb

## Purpose

Convert technical findings into business recommendations.

## Contains

### Seller Insights

- Optimal pricing ranges
- Successful posting behavior

### Category Insights

- Best-performing categories
- Weak-performing segments

### Regional Analysis

### Marketplace Recommendations

- Ranking suggestions
- Seller optimization ideas

### KPI Recommendations

## Owner

Person 3

---

# 10_final_pipeline_demo.ipynb

## Purpose

Final end-to-end project demonstration.

## Contains

- Load raw data
- Apply preprocessing
- Apply feature engineering
- Train final model
- Generate predictions
- Display metrics
- Visualize insights
- Demo example predictions

## Owners

Entire team

---

# Python Module Responsibilities

## src/preprocessing.py

Contains:

- Text cleaning
- Missing value handling
- Categorical encoding
- Preprocessing pipelines

---

## src/feature_engineering.py

Contains:

- Engineered feature functions
- Aggregation features
- Derived metrics

---

## src/train.py

Contains:

- Model training functions
- Hyperparameter tuning functions

---

## src/predict.py

Contains:

- Prediction functions
- Inference pipeline

---

## src/evaluate.py

Contains:

- Evaluation metrics
- Confusion matrix functions
- ROC plotting

---

## src/visualization.py

Contains:

- Reusable charts
- Plotting utilities

---

# Collaboration Workflow

---

# Branching Strategy

Never work directly on `main`.

Each team member creates feature branches:

```bash
git checkout -b feature/preprocessing
git checkout -b feature/modeling
git checkout -b feature/evaluation
```

---

# Pull Request Workflow

1. Create branch
2. Make changes
3. Commit changes
4. Push branch
5. Open Pull Request
6. Review changes
7. Merge into main

---

# Notebook Collaboration Rules

## Rules

### Keep notebooks short

Notebooks should:

- Visualize
- Experiment
- Explain

Not contain:

- Huge reusable code blocks

---

### Reusable logic belongs in `/src`

Example:

```python
from src.preprocessing import preprocess_data
from src.train import train_xgboost
```

---

### Clear notebook outputs before commit

Install:

```bash
pip install nbstripout
```

Then:

```bash
nbstripout --install
```

This reduces notebook merge conflicts.

---

# Recommended Kanban Board

## BACKLOG

- Understand dataset
- Define KPIs
- Research Avito business model

---

## TODO

### Data Tasks

- Handle missing values
- TF-IDF preprocessing
- Feature engineering

### Modeling Tasks

- Logistic regression baseline
- Random forest benchmark
- XGBoost model
- Hyperparameter tuning

### Evaluation Tasks

- ROC analysis
- SHAP explainability
- Threshold optimization

### Product Tasks

- Streamlit dashboard
- README documentation
- Final presentation

---

## IN PROGRESS

Currently assigned active work.

---

## REVIEW

Code review and pull request review.

---

## DONE

Completed and merged tasks.

---

# Smart Task Splitting Strategy

---

# Person 1 — Data Engineering

## Primary Focus

Create clean and reusable datasets.

## Tasks

- EDA
- Preprocessing
- TF-IDF
- Feature engineering
- Processed dataset exports

## Deliverables

- preprocessing.py
- feature_engineering.py
- processed datasets

---

# Person 2 — Machine Learning

## Primary Focus

Build and optimize models.

## Tasks

- Logistic regression
- Random forest
- XGBoost
- LightGBM
- Hyperparameter tuning
- Model comparison

## Deliverables

- train.py
- trained models
- evaluation benchmarks

---

# Person 3 — Analytics / Product

## Primary Focus

Business interpretation and deployment.

## Tasks

- Evaluation notebooks
- Explainability
- Business recommendations
- Streamlit dashboard
- GitHub organization
- README
- Final presentation

## Deliverables

- Evaluation reports
- SHAP insights
- Streamlit app
- Final documentation

---

# Final Project Goal

The final deliverable should demonstrate:

- End-to-end ML workflow
- Collaborative software engineering
- Business analytics
- Explainable AI
- Deployment-ready structure
- Professional GitHub practices

The objective is not only model accuracy, but building a realistic machine learning analytics system.