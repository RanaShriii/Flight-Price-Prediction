#  Flight Price Prediction using Machine Learning

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?logo=scikitlearn)
![XGBoost](https://img.shields.io/badge/XGBoost-Regressor-green)
![CatBoost](https://img.shields.io/badge/CatBoost-Regressor-yellow)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

An end-to-end Machine Learning project that predicts airline ticket prices using multiple regression algorithms. The project covers exploratory data analysis, data preprocessing, model comparison, hyperparameter tuning, feature importance analysis, and final prediction generation.

## Project Overview

Airfare prediction is a regression problem where the objective is to estimate the price of a flight based on various travel-related attributes such as airline, source, destination, duration, number of stops, travel class, and booking timing.

In this project, multiple machine learning regression models were trained and compared to identify the best-performing model. After evaluating several algorithms, a tuned Random Forest Regressor achieved the strongest overall performance and was used to generate predictions for unseen test data.

The project follows a complete machine learning workflow including:

- Data Exploration
- Data Cleaning
- Missing Value Handling
- Feature Encoding
- Model Training
- Model Evaluation
- Hyperparameter Tuning
- Feature Importance Analysis
- Final Prediction Generation

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- XGBoost
- CatBoost
- Jupyter Notebook
- Git & GitHub

## Dataset

The dataset contains historical flight booking information used to predict airline ticket prices.

### Features

| Feature | Description |
|----------|-------------|
| Airline | Airline operating the flight |
| Flight | Flight code |
| Source | Departure city |
| Departure | Time of departure |
| Stops | Number of stops |
| Arrival | Arrival time |
| Destination | Destination city |
| Class | Travel class (Economy/Business) |
| Duration | Flight duration |
| Days Left | Days remaining before departure |
| Price | Target variable (Flight Ticket Price) |

> **Note:** The dataset is available publicly on my Kaggle profile.
> **Dataset:** [Flight Price Prediction Dataset](https://www.kaggle.com/datasets/shrimantrana/flight-dataset)

## Project Workflow

```text
Dataset
   │
   ▼
Data Cleaning
   │
   ▼
Missing Value Handling
   │
   ▼
Feature Encoding
   │
   ▼
Exploratory Data Analysis
   │
   ▼
Train / Validation Split
   │
   ▼
Model Training
   │
   ▼
Model Comparison
   │
   ▼
Hyperparameter Tuning
   │
   ▼
Feature Importance
   │
   ▼
Prediction on Test Dataset
   │
   ▼
Submission File
```

## Machine Learning Models

The following regression algorithms were implemented and evaluated:

- Dummy Regressor (Baseline)
- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Extra Trees Regressor
- Gradient Boosting Regressor
- XGBoost Regressor
- CatBoost Regressor

Hyperparameter tuning was performed on the Random Forest model using **RandomizedSearchCV** to improve predictive performance.

## Model Performance

The models were evaluated using **Mean Absolute Error (MAE)**, **Root Mean Squared Error (RMSE)**, and **R² Score** on the validation dataset.

| Model | MAE | RMSE | R² Score |
|------|------:|------:|------:|
| Dummy Regressor | 19766.42 | 22714.82 | 0.0000 |
| Linear Regression | 4685.93 | 7082.07 | 0.9028 |
| Decision Tree Regressor | 1825.92 | 4264.85 | 0.9647 |
| Random Forest Regressor | 1631.29 | 3241.74 | 0.9796 |
| Extra Trees Regressor | 1689.08 | 3466.36 | 0.9767 |
| Gradient Boosting Regressor | 2907.95 | 4830.26 | 0.9548 |
| XGBoost Regressor | 2107.39 | 3673.69 | 0.9738 |
| CatBoost Regressor | 2353.77 | 3965.45 | 0.9695 |
| **Tuned Random Forest** | **1633.56** | **3216.55** | **0.9799** |

## Best Performing Model

After comparing multiple regression algorithms, the **Random Forest Regressor** achieved the strongest overall performance.

Hyperparameter tuning using **RandomizedSearchCV** further improved the model, resulting in:

- **RMSE:** 3216.55
- **R² Score:** 0.9799

The tuned Random Forest model was selected as the final model for generating predictions on the unseen test dataset.

## Feature Importance

The Random Forest model provides feature importance scores that indicate how much each feature contributes to the prediction.

| Feature | Importance |
|---------|-----------:|
| Class | 0.8839 |
| Duration | 0.0340 |
| Flight | 0.0306 |
| Stops | 0.0158 |
| Days Left | 0.0143 |
| Destination | 0.0101 |
| Source | 0.0058 |
| Arrival | 0.0030 |
| Departure | 0.0022 |
| Airline | 0.0004 |

The travel **class** was by far the most influential feature, followed by **flight duration** and **flight identifier**, indicating that these variables had the greatest impact on ticket price prediction.

## Key Insights

- Random Forest outperformed all other evaluated models.
- Hyperparameter tuning improved the model's RMSE and R² score.
- Travel class was the most significant predictor of ticket price.
- Ensemble learning methods consistently performed better than Linear Regression.
- The final model generalized well on the validation dataset, achieving an R² score close to 0.98.

## Project Structure

```
Flight-Price-Prediction/
│
├── notebook/
│   └── Flight_Price_Prediction.ipynb
│
├── submission/
│   └── submission.csv
│
├── images/
│
├── docs/
│
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
```

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/RanaShriii/Flight-Price-Prediction.git
```

Navigate to the project directory:

```bash
cd Flight-Price-Prediction
```

Install the required packages:

```bash
pip install -r requirements.txt
```

## How to Run

1. Clone the repository.
2. Install the required dependencies.
3. Open the notebook located in the `notebook/` folder.
4. Run all cells sequentially.
5. The final predictions will be generated as `submission.csv`.

## Future Improvements

- Deploy the trained model as a web application using Flask or Streamlit.
- Experiment with deep learning models for price prediction.
- Perform advanced feature engineering.
- Automate hyperparameter tuning using Optuna.
- Build an interactive dashboard for ticket price analysis.

## 👨‍💻 Author

**Shrimant Rana**

- GitHub: (https://github.com/RanaShriii) 
- Kaggle: (https://www.kaggle.com/shrimantrana)
- LinkedIn: (https://www.linkedin.com/in/ranashrimant)