# Week 2 — Supervised Machine Learning Models

## Project Overview

This project demonstrates the fundamental concepts of **supervised machine learning** using Scikit-learn. The workflow covers model training, prediction, evaluation, and comparison of multiple regression and classification algorithms.

## Concept Demonstrated

The main concept demonstrated is:

> **Prepared Data → Model Training → Prediction → Evaluation → Model Comparison**

In supervised learning, a model learns a relationship between input features and a known target variable using labelled training data. After training, the model can make predictions on previously unseen test data.

## Key Concepts Covered

### 1. Supervised Learning

Supervised machine learning uses labelled data where the desired output is known during training.

Two major problem types are demonstrated:

- **Regression** — predicts a continuous numerical value.
- **Classification** — predicts a class/category.

### 2. Train-Test Split

The dataset is divided into training and testing portions.

The training set is used to learn model parameters, while the test set is kept separate for evaluating performance on unseen observations.

The project uses an **80/20 train-test split**.

```text
Dataset
   ↓
Train/Test Split
   ├── 80% Training Data → Model Learning
   └── 20% Test Data → Final Evaluation
```

### 3. Linear Regression

Linear Regression is used for regression problems. It models the relationship between input features and a continuous target.

The project evaluates the regression prediction using:
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

### 4. Logistic Regression

Logistic Regression is used for binary classification. Instead of directly predicting a continuous value, it estimates the probability of a class and converts that probability into a class prediction.

It is a fundamental classification algorithm and provides an important baseline for comparison.

### 5. Decision Tree

A Decision Tree makes predictions through a sequence of feature-based decision rules.

Conceptually:

```text
Feature Condition
       ↓
   Decision Rule
    ↙        ↘
Branch       Branch
  ↓            ↓
Further       Further
Decision      Decision
       ↓
   Prediction
```

Decision Trees can model nonlinear relationships and are easy to interpret.

### 6. Random Forest

Random Forest combines multiple decision trees into an ensemble model.

Instead of relying on a single tree, multiple trees contribute to the final prediction. This demonstrates the concept of **ensemble learning**.

### 7. K-Nearest Neighbors (KNN)

KNN predicts the class of an observation based on the classes of nearby training observations.

The basic idea is:

```text
New Observation
       ↓
Find K Nearest Training Samples
       ↓
Compare Their Classes
       ↓
Majority Vote
       ↓
Predicted Class
```

### 8. Classification Evaluation

Classification models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

These metrics provide different views of classification performance rather than relying on accuracy alone.

### 9. Regression Evaluation

Regression models are evaluated using:

**MAE**

Measures the average absolute difference between predicted and actual values.

**RMSE**

Measures prediction error while giving greater weight to larger errors.

**R²**

Measures how much of the variation in the target is explained by the regression model.

### 10. Model Comparison

The project compares multiple algorithms using common evaluation metrics.

This demonstrates an important machine-learning practice:

> A model should be evaluated using appropriate metrics and compared objectively rather than selected only because it is a familiar algorithm.

## Models Implemented

### Regression Models

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- KNN Regressor

### Classification Models

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- KNN Classifier

## Dataset

The project uses the **STAR98 Educational Dataset** used in the earlier internship workflow.

The dataset is transformed into supervised-learning targets so that both regression and binary classification experiments can be performed.

## Machine-Learning Workflow

```text
Prepared Dataset
       ↓
Define Features & Target
       ↓
Train/Test Split
       ↓
Feature Preprocessing
       ↓
Train Multiple Models
       ↓
Generate Predictions
       ↓
Calculate Evaluation Metrics
       ↓
Compare Models
       ↓
Visualize Performance
       ↓
Analyze Errors and Limitations
```

## Actual Model Comparison

### Regression

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 0.0578 | 0.0695 | 0.8764 |
| Random Forest | 0.0719 | 0.0885 | 0.7997 |
| KNN | 0.0854 | 0.1072 | 0.7063 |
| Decision Tree | 0.0867 | 0.1084 | 0.6994 |

### Classification

| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| KNN | 0.8361 | 0.7838 | 0.9355 | 0.8529 | 0.9280 |
| Logistic Regression | 0.8033 | 0.7879 | 0.8387 | 0.8125 | 0.9194 |
| Random Forest | 0.8033 | 0.7879 | 0.8387 | 0.8125 | 0.9333 |
| Decision Tree | 0.7869 | 0.7813 | 0.8065 | 0.7937 | 0.8016 |

These results are the outputs generated for this project configuration and dataset split.

## Technologies Used

- Python
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- pytest

## Validation

The project includes automated validation tests to check important pipeline behavior.

Run:

```bash
python -m pytest -q
```

## Learning Outcome

After completing this project, the learner understands the basic supervised-learning lifecycle:

1. Prepare labelled data.
2. Separate features and targets.
3. Split data into training and testing sets.
4. Train multiple algorithms.
5. Generate predictions.
6. Evaluate predictions using suitable metrics.
7. Compare model performance.
8. Examine errors and limitations.

## Relationship to Week 1

Week 1 established the **data preprocessing foundation**.

Week 2 builds on that foundation by applying the prepared data to **supervised machine-learning models**.

```text
WEEK 1
Data Preparation
      ↓
Clean & Transform Data
      ↓
WEEK 2
Train Supervised Models
      ↓
Predict & Evaluate
      ↓
Compare Models
```

## Project Purpose

This repository is part of the **Virtual Data Science with Python Apprentice Internship — Week 2** work and focuses on supervised machine-learning model development, evaluation, and comparison.
