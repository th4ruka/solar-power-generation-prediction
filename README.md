<img src="https://github.com/th4ruka/solar-power-generation-prediction/assets/78165134/6c506dd8-0344-4046-9afe-80827c4ce232" width="1000" height="300">

[![Language-Python-blue.svg](https://img.shields.io/badge/language-python-blue.svg)]([https://img.shields.io/badge/language-python-blue.svg]) [![License-MIT-yellow.svg](https://img.shields.io/badge/License-MIT-yellow.svg)]([https://img.shields.io/badge/License-MIT-yellow.svg])


## Solar Power Generation Prediction for a Power Plant

This project focuses on predicting the AC power generation of a solar power plant using machine learning models. The primary goal is to forecast power generation for the upcoming days, assisting plant operators in efficient resource planning and management. This project was conducted under the **EE7209: Machine Learning** module in the [Department of Electrical and Information Engineering, University of Ruhuna](https://www.eng.ruh.ac.lk/deie/).

### Group Members

* [Tharuka Pavith](https://github.com/th4ruka) 
* [Sachini Ranaweera](https://github.com/ranaweerasc65)

### Project Structure

* **Plant_2_Generation_Data.csv:** Contains power generation data for different inverters over time.
* **Plant_2_Weather_Sensor_Data.csv:** Holds weather information relevant to power generation (temperature, irradiation, etc.).
* **SolarPowerGenerationPrediction.ipynb:**  The Jupyter Notebook containing the data analysis, preprocessing, model building, and evaluation steps.

### Project Overview

1. **Data Loading and Cleaning:** The dataset is loaded from CSV files and initial cleaning is performed (dropping irrelevant columns).
2. **Feature Engineering:**
    * A new feature `TOTAL_MINUTES_PASS` is created to capture time within a day in a format suitable for machine learning models.
    * The `SOURCE_KEY` (inverter ID) is one-hot encoded to handle its categorical nature.
3. **Exploratory Data Analysis (EDA):**  The data is thoroughly explored using visualizations and summary statistics to understand patterns and relationships.
4. **Feature Scaling:** Numerical features are standardized for better model performance.
5. **Model Building:** Two regression models are implemented and compared:
    * **Linear Regression:**  A simple baseline model.
    * **Random Forest Regression:** A more flexible, non-linear model.
6. **Hyperparameter Tuning:** Grid Search is used to find optimal hyperparameters for the Random Forest model.
7. **Model Evaluation:** Models are evaluated on both training and testing sets using metrics like R-squared, Mean Absolute Error (MAE), Median Absolute Error (MedAE), and Root Mean Squared Error (RMSE).

### Key Findings

* **Random Forest outperforms Linear Regression:** The Random Forest model, especially after hyperparameter tuning, significantly outperforms Linear Regression in predicting AC power generation.
* **Overfitting Mitigation:** Techniques to reduce overfitting in the Random Forest model (limiting tree depth, adjusting minimum samples per split/leaf) were explored.
* **Data Insights:** EDA reveals important relationships between weather conditions, time, and power generation.
