# Module 05 — Data Preprocessing

Data preprocessing is one of the most important steps in any Machine Learning workflow.  
Real-world datasets are rarely clean. They often contain missing values, categorical data, inconsistent formats, and features with very different scales.

Before training a machine learning model, the dataset must be cleaned and transformed so that algorithms can learn meaningful patterns.

This module covers the most essential preprocessing techniques used in machine learning pipelines.

---

# Topics Covered

## 1. Handling Missing Values

Datasets frequently contain missing or incomplete data.  
Machine learning models cannot directly handle missing values, so they must be processed before training.

Common techniques include:

- Dropping rows or columns with missing values
- Filling missing values using:
  - Mean
  - Median
  - Mode
- Forward fill and backward fill

Notebook:

01_handling_missing_values.ipynb

---

## 2. Encoding Categorical Data

Many datasets contain categorical variables such as:

- Gender
- City
- Payment Type
- Product Category

Machine learning algorithms require numerical input, so categorical data must be converted into numerical form.

Common encoding techniques:

### Label Encoding

Assigns a unique number to each category.

Example:

| City | Encoded |
|-----|------|
| Delhi | 0 |
| Mumbai | 1 |
| Chennai | 2 |

### One-Hot Encoding

Creates a binary column for each category.

Example:

| City_Delhi | City_Mumbai | City_Chennai |
|------------|------------|-------------|
| 1 | 0 | 0 |

Notebook:

02_encoding_categorical_data.ipynb

---

## 3. Feature Scaling

Features in a dataset may have different numerical ranges.

Example:

| Feature | Range |
|-------|-------|
| Age | 18–60 |
| Salary | 20,000–100,000 |

Large-scale features can dominate machine learning models.  
Feature scaling ensures that all features contribute equally.

Two common methods:

### Normalization (Min-Max Scaling)

Formula:

(X - Xmin) / (Xmax - Xmin)

Transforms values to the range **0–1**.

### Standardization (Z-Score Scaling)

Formula:

(X - Mean) / Standard Deviation

Transforms data so that:

- Mean = 0
- Standard deviation = 1

Notebook:

03_feature_scaling.ipynb

---

## 4. Train-Test Split

Before training a machine learning model, the dataset must be divided into two parts:

### Training Data
Used to train the machine learning model.

### Testing Data
Used to evaluate the model's performance on unseen data.

A common split ratio:

- 80% Training
- 20% Testing

This helps prevent **overfitting**, where a model memorizes the training data but fails to generalize to new data.

Notebook:

04_train_test_split.ipynb

---

## 5. Feature Engineering

Feature engineering is the process of creating new features or transforming existing ones to improve model performance.

Techniques include:

### Feature Creation

Creating new variables from existing ones.

Example:

Productivity_Index = Study_Hours × Attendance

### Feature Transformation

Changing the distribution of data.

Example:

Log Transformation

### Feature Selection

Selecting only important features for the model.

Notebook:

05_feature_engineering_basics.ipynb

---

# Why Data Preprocessing is Important

Proper preprocessing can significantly improve machine learning model performance.

Benefits include:

- Cleaner datasets
- Better model accuracy
- Faster model convergence
- Reduced overfitting
- Improved interpretability

In many real-world projects, **data preprocessing and feature engineering consume the majority of the project time**.

---

# Folder Structure

05_data_preprocessing/

├── 01_handling_missing_values.ipynb  
├── 02_encoding_categorical_data.ipynb  
├── 03_feature_scaling.ipynb  
├── 04_train_test_split.ipynb  
├── 05_feature_engineering_basics.ipynb  
└── README.md  

---

# Next Module

The next module introduces **Machine Learning algorithms**, starting with:

06_machine_learning/

First notebook:

01_linear_regression.ipynb

In that module we will learn how to:

- Train machine learning models
- Make predictions
- Evaluate model performance
- Build complete ML pipelines.
