# Calories Burnt Prediction Using XGBoost

## Project Overview

This project uses machine learning to predict the number of calories burned during physical exercise based on personal characteristics and exercise-related measurements.

The project follows a complete machine learning workflow, including data inspection, exploratory data analysis (EDA), preprocessing, model training, and performance evaluation.

## Objectives

- Explore and understand the exercise and calories datasets.
- Perform exploratory data analysis and visualize feature distributions.
- Prepare features for machine learning.
- Train an XGBoost regression model.
- Evaluate model performance using regression metrics.
- Examine feature importance and prediction residuals.

## Dataset

The project uses two CSV files downloaded from Kaggle: https://www.kaggle.com/datasets/fmendes/fmendesdat263xdemos?select=exercise.csv

- `exercise.csv` — contains user information and exercise-related measurements.
- `calories.csv` — contains the corresponding calorie expenditure values.

The datasets are combined using `User_ID`.

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Google Colab

## Machine Learning Workflow

1. Import libraries and load the datasets.
2. Inspect data structure and quality.
3. Merge datasets using `User_ID`.
4. Perform exploratory data analysis.
5. Encode the categorical `Gender` feature.
6. Separate features and target.
7. Split data into training and testing sets.
8. Train a Dummy Regressor baseline and an XGBoost Regressor.
9. Evaluate performance and analyze predictions.
10. Examine feature importance and residuals.

## Model Performance

The XGBoost Regressor achieved the following results on the held-out test set:

| Metric | Dummy Regressor | XGBoost Regressor |
|---|---:|---:|
| MAE | 53.9279 | 1.1964 |
| RMSE | 63.5667 | 1.6341 |
| R² Score | -0.0012 | 0.9993 |

The XGBoost model substantially outperformed the mean-prediction baseline on this dataset split. However, the exceptionally high R² score should be validated on independent data before making claims about real-world performance.

## Feature Importance

The model assigned its highest feature-importance score to `Duration`, followed by `Heart_Rate` and `Body_Temp`.

Feature importance describes how the model uses its input features; it does not establish causal relationships.

## Repository Contents

- `Calories_Burnt_Prediction.ipynb` — notebook containing data analysis, model training, evaluation, and visualizations.
- `calories.csv` — calorie expenditure dataset.
- `exercise.csv` — exercise-related dataset.
- `README.md` — project documentation.

## Limitations and Future Improvements

- Validate the model using independent data.
- Apply cross-validation.
- Compare additional regression algorithms.
- Perform systematic hyperparameter tuning.
- Investigate the unusually high predictive performance.

## Learning and Acknowledgment

This project was developed as part of my ongoing learning in machine learning, with reference to tutorial-based learning materials and assistance from AI tools.
