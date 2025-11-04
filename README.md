# Global Temperature Forecasting with Random Forest
 Predicting Land and Ocean Temperature Averages using Machine Learning


##  Overview
This project explores a historical global temperature dataset dating back to **1750** and applies **Random Forest Regression** to predict the **Land and Ocean Average Temperature** based on land temperature features.

The goal was to build an end-to-end pipeline using Python and scikit-learn that demonstrates real-world data preprocessing, model building, and evaluation — showcasing the application of machine learning for climate forecasting.


## What I learned 
- Cleaning and transforming time-series data using `pandas`
- Understanding and applying feature selection and scaling
- Building machine learning pipelines with `scikit-learn`
- Training and evaluating ensemble models (Random Forest)
- Using MAE as a baseline and model performance metric
- Detecting and interpreting overfitting
- Visualizing feature correlation and model insights


## Dataset
- Source: Global Land and Ocean Temperature Dataset (CSV)
- Contains monthly temperature data from **1750 to present**
- Key features:
  - `LandAverageTemperature`
  - `LandMaxTemperature`
  - `LandMinTemperature`
  - `LandAndOceanAverageTemperature` *(Target)*
 

## Data Cleaning Steps
- Dropped uncertainty columns to reduce noise
- Parsed and extracted `year` from the datetime column
- Removed rows with missing values
- Dropped seasonal bias by removing `month`
- Final cleaned dataset: **1,992 rows**

## Exploratory Data Analysis (EDA)

- Correlation heatmap shows strong correlation between land temperatures and the target
- Visual checks ensured feature relevance and data sanity


## Model Pipeline 

  | Step               | Tool                      |
  |--------------------|---------------------------|
  | Feature Selection  | `SelectKBest`             |
  | Feature Scaling    | `StandardScaler`          |
  | Model              | `RandomForestRegressor`   |
  | Evaluation Metric  | Mean Absolute Error (MAE) |

- Training-test split: 75/25
- Baseline MAE (mean-only predictor): **1.63**
- Random Forest MAE (Test): **0.031**
- Random Forest MAE (Train): **0.004**


##  Results

✅ Model outperforms baseline significantly  
✅ Demonstrates strong predictive power  
⚠️ Minor overfitting observed (train MAE vs test MAE)  

##  Tech Stack

- Python 3.x
- pandas, numpy
- matplotlib, seaborn
- scikit-learn (pipeline, modeling, evaluation)

