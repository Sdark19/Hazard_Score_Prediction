# Hazard Score Prediction

## Table of Contents
- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Dataset](#dataset)
  - [Features](#features)
  - [Target Variable](#target-variable)
- [Installation](#installation)
- [Usage](#usage)
- [Model Details](#model-details)
- [Results](#results)

## Overview
This project focuses on predicting the hazard score for maintenance tasks in heavy equipment operations. The goal is to assess the potential danger associated with these tasks before they are executed, enabling organizations to implement appropriate safety measures proactively. The dataset provided contains masked features related to maintenance tasks, and the target variable is the hazard score. The project involves building a predictive model using the training dataset and generating predictions for the test dataset.

## Problem Statement
All the money in the world cannot make up for a loss of life. "Better safe than sorry" is the motto of all engineering and construction practices that routinely deal with dangerous situations. However, many times, the extent of caution is just not enough and leads to very hard-learned lessons in employee safety.

Instead of relying on something going wrong and then taking preventive measures, organizations are coming up with ways of assessing the extent of danger to life for a new project before even the first hammer strikes.

Given to you is a masked dataset that contains various properties of tasks taken up in heavy equipment maintenance by a manual crew. Each of these tasks has been given a hazard score, which is eventually used in deciding levels of safety checks and caution while planning for the maintenance process.

## Dataset
The dataset consists of two files:
- **Train Dataset**: `Hazard_train.csv`
  - Contains the features and the target variable (`Hazard`).
- **Test Dataset**: `Hazard_test_share.csv`
  - Contains only the features. The target variable (`Hazard`) needs to be predicted.

  ### Features
  - The features are masked, and no formal data dictionary is provided.
  - The dataset includes various properties related to maintenance tasks.

  ### Target Variable
  - **Target Column**: `Hazard`
  - This is the hazard score that needs to be predicted for the test dataset.

## Installation
To set up the project, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/Hazard-Score-Prediction.git
   ```
   
2. Install Dependencies:
Install the required Python packages using:
```bash
pip install -r requirements.txt
```
- The requirements.txt file includes the following dependencies:
  - pandas
  - numpy
  - scikit-learn
  - lightgbm
  - catboost
  - optuna

## Usage
-  Open the Pharma.ipynb notebook in Jupyter or vs code.

-  Run each cell sequentially to load the data, preprocess it, train the model, and generate predictions.

-  The final predictions are saved in a CSV file named output.csv.

## Model Details
The predictive model is built using the following steps:

1.  Data Preprocessing:

- Handle missing values using imputation.

- Encode categorical variables using label encoding.

- Scale numerical features using standardization.

2. Model Selection:

- The model is built using LightGBM and CatBoost, which are gradient boosting frameworks known for their efficiency and accuracy.

3.  Hyperparameter Tuning:

- Hyperparameters are optimized using Optuna, a hyperparameter optimization framework.

4.  Evaluation:

-  The model is evaluated using Mean Absolute Error (MAE) on the validation set.

## Results
- The final predictions are saved in output.csv.

-  The model achieves a Mean Absolute Error (MAE) of 2.5852540755461844 on the validation set, indicating its performance in predicting hazard scores.
