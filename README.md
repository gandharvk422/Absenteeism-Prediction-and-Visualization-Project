# Absenteeism Prediction and Visualization Project

## Project Overview
This project aims to predict employee absenteeism using machine learning and visualize the results with Tableau. The workflow covers data cleaning, feature engineering, model building, prediction on new data, database integration, and interactive dashboarding.

## Folder Structure
- `Part1.ipynb` — Data exploration and cleaning (Part 1)
- `Part2.ipynb` — Machine learning model development (Part 2)
- `Part3.ipynb` — Module creation for prediction (Part 3)
- `Part4.ipynb` — SQL integration and automation (Part 4)
- `Part5.twb` — Tableau dashboard (Part 5)
- `Part6.pbix` — PowerBI dashboard (Part 6)
- `absenteeism_module.py` — Custom Python module for prediction
- `Absenteeism-data.csv` — Raw data
- `Absenteeism_preprocessed.csv` — Preprocessed data
- `Absenteeism_new_data.csv` — New data for prediction
- `Absenteeism_predictions.csv` — Model predictions on new data
- `model` — Pickled logistic regression model
- `scaler` — Pickled scaler object
- `Creating Database.sql` — SQL script for MySQL table

## Data Description
- **Absenteeism-data.csv**: Raw dataset with features such as ID, Reason for Absence, Date, Transportation Expense, Distance to Work, Age, Daily Work Load Average, Body Mass Index, Education, Children, Pets, and Absenteeism Time in Hours.
- **Absenteeism_preprocessed.csv**: Cleaned and feature-engineered data, including dummy variables for reasons, month, and other processed features.
- **Absenteeism_new_data.csv**: New, unseen data for prediction, with the same structure as the raw data but without the target variable.
- **Absenteeism_predictions.csv**: Model output on new data, including predicted probabilities and binary predictions for absenteeism.

## Workflow
### 1. Data Cleaning and Exploration (Part1)
- Loads and explores the raw absenteeism data.
- Handles missing values, outliers, and prepares the data for modeling.

### 2. Machine Learning Model (Part2)
- Loads preprocessed data.
- Creates a binary target for excessive absenteeism.
- Standardizes features and trains a logistic regression model.
- Saves the trained model and scaler for reuse.

### 3. Module Creation and Prediction (Part3)
- Implements `absenteeism_module.py` with a custom scaler and model class.
- Demonstrates how to load new data, preprocess it, and generate predictions using the saved model and scaler.

### 4. SQL Integration (Part4 & Creating Database.sql)
- Uses the module to predict absenteeism on new data.
- Connects to a MySQL database and creates a table for predictions.
- Inserts prediction results into the database for further analysis.

### 5. Visualization (Part5.twb and Part6.pbix)
- Tableau and PowerBI dashboards connects to `Absenteeism_predictions.csv`.
- Provides interactive visualizations such as:
  - Age vs Probability of Absenteeism
  - Reasons vs Probability
  - Transportation Expense and Children

## How to Run
### Requirements
- Python 3.x
- pandas, numpy, scikit-learn, pymysql
- MySQL server (for database integration)
- Tableau and Power BI Desktops (for dashboard)

### Steps
1. **Data Preparation**: Run `Part1` to clean and preprocess the raw data.
2. **Model Training**: Run `Part2` to train and save the model and scaler.
3. **Module and Prediction**: Run `Part3` to use the module for predictions on new data.
4. **Database Integration**: Run `Part4` to insert predictions into MySQL using the provided SQL script.
5. **Visualization**: Open `Part5` in Tableau Desktop and `Part6` in PowerBI Desktop and connect to `Absenteeism_predictions.csv` for interactive analysis.

## Tableau Dashboard
- Open `Part5.twb` in Tableau Desktop.
- Ensure `Absenteeism_predictions.csv` is in the expected directory.
- Explore the provided worksheets for insights into absenteeism patterns.

## PowerBI Dashboard
- Open `Part6.pbix` in PowerBI Desktop.
- Ensure `Absenteeism_predictions.csv` is located in the same directory or correctly linked in the data source settings.
- Review the visuals and filters to analyze patterns and trends in employee absenteeism.

## Credits
Developed as a comprehensive workflow for absenteeism prediction and visualization, integrating Python, SQL, Tableau, and PowerBI.
