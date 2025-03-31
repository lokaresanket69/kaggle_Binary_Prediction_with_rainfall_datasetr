# kaggle_Binary_Prediction_with_rainfall_dataset
# Kaggle Rainfall Prediction Hackathon

This repository contains my solution for the 2025 Kaggle Playground Series hackathon, where the goal is to predict daily rainfall. The competition focuses on binary classification using synthetically generated tabular data derived from a real-world rainfall prediction dataset.

## Overview

- **Competition Goal:** Predict the probability of rainfall for each day based on weather and climate features.
- **Evaluation Metric:** ROC AUC score.
- **Dataset Files:**
  - `train.csv`: Contains training data with features and a binary target (`rainfall`).
  - `test.csv`: Contains test data for which predictions are required.
  - `sample_submission.csv`: A sample file showing the required submission format.

The challenge is designed as a lightweight introduction to time series and tabular data analysis, allowing experimentation with different feature engineering and model tuning strategies.

## Project Structure

- **Data Exploration & Preprocessing:**  
  - Load datasets and inspect shapes, data types, and missing values.
  - Visualize the distribution of features and the target variable.
  
- **Baseline Modeling:**  
  - A baseline Logistic Regression model is built to set an initial benchmark.
  
- **Advanced Modeling with LightGBM:**  
  - A tree-based model using LightGBM is implemented.
  - Feature importance is analyzed to understand influential variables.
  
- **Feature Engineering:**  
  - New features such as temperature range, average temperature, and humidity delta are engineered.
  
- **Hyperparameter Tuning:**  
  - Hyperparameter tuning using LightGBM's cross-validation (`lgb.cv`) and early stopping is performed.
  
- **Final Model & Submission:**  
  - The final model is trained on the full dataset using the best hyperparameters.
  - Predictions are generated for the test set, and a submission file (`submission.csv`) is created in the required format.

## How to Run

This notebook was implemented in Google Colab. To reproduce the results:
1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/kaggle-rainfall-prediction.git
   cd kaggle-rainfall-prediction
