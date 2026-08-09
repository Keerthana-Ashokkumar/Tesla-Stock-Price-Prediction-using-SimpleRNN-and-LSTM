# Tesla Stock Price Prediction using SimpleRNN and LSTM

## Project Overview

This project focuses on predicting Tesla stock prices using deep learning-based time-series forecasting models.

SimpleRNN and LSTM models are developed and compared to predict Tesla's adjusted closing price for:

- 1-day ahead
- 5-day ahead
- 10-day ahead

The project also includes exploratory data analysis, data preprocessing, hyperparameter tuning using GridSearchCV, recursive forecasting, and news sentiment analysis.

## Domain

Financial Services | Data Science | Deep Learning | Time-Series Forecasting

## Problem Statement

Stock prices are sequential and highly dynamic in nature. The objective of this project is to develop deep learning models that can learn historical Tesla stock-price patterns and predict future closing prices.

The project compares SimpleRNN and LSTM models across multiple forecasting horizons.

## Project Objectives

- Analyze Tesla historical stock-price data
- Perform data cleaning and preprocessing
- Conduct exploratory data analysis and visualization
- Build SimpleRNN and LSTM models
- Predict 1-day, 5-day and 10-day prices
- Evaluate models using MSE, RMSE and MAE
- Tune LSTM hyperparameters using GridSearchCV
- Compare SimpleRNN and LSTM performance
- Perform recursive multi-step forecasting
- Analyze Tesla news sentiment using VADER
- Identify limitations and future improvements

## Dataset

The dataset contains Tesla historical stock-price information.

### Features

| Column | Description |
|---|---|
| Date | Trading date |
| Open | Opening price |
| High | Highest price |
| Low | Lowest price |
| Close | Closing price |
| Adj Close | Adjusted closing price |
| Volume | Trading volume |

Dataset contains 2,416 records.

## Data Preprocessing

The following preprocessing steps were performed:

- Checked missing values
- Checked duplicate records
- Converted Date into datetime format
- Sorted data chronologically
- Set Date as index
- Selected Adjusted Close as the prediction feature
- Applied MinMaxScaler
- Fitted the scaler only on training data to avoid data leakage
- Created time-series sequences using a 60-day window

The original dataset contains no missing values or duplicate records.

## Exploratory Data Analysis

EDA includes:

- Tesla closing price trend
- Trading volume analysis
- Moving averages
- Daily returns and volatility
- Feature distributions
- Correlation heatmap
- Boxplot analysis

## Feature Engineering

The primary prediction feature is:

**Adjusted Closing Price**

A 60-day historical window is used to predict future prices.

Forecast horizons:

- 1-day
- 5-day
- 10-day

## Deep Learning Models

### SimpleRNN

Architecture:

- SimpleRNN – 64 units
- Dropout – 0.2
- SimpleRNN – 32 units
- Dropout – 0.2
- Dense – 1 output

### LSTM

Architecture:

- LSTM – 64 units
- Dropout – 0.2
- LSTM – 32 units
- Dropout – 0.2
- Dense – 1 output

Both models use:

- Adam optimizer
- Mean Squared Error loss
- EarlyStopping
- ModelCheckpoint

## Model Evaluation

The models are evaluated using:

- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)

Lower RMSE and MAE indicate better prediction performance.

## Hyperparameter Tuning

GridSearchCV was used to tune the LSTM model.

Parameters explored:

- Number of units: 32, 64
- Dropout: 0.2, 0.3
- Learning rate: 0.001, 0.005

Best configuration identified:

- Units: 64
- Dropout: 0.3
- Learning Rate: 0.005

## News Sentiment Analysis

Tesla-related news headlines were analyzed using VADER sentiment analysis.

The process includes:

- Text cleaning
- Sentiment scoring
- Positive / Neutral / Negative classification
- Comparison of sentiment with Tesla daily returns

This demonstrates how external information could be incorporated into future stock prediction models.

## Forecasting

A recursive forecasting approach is used to generate a 10-day forward forecast using the 1-day LSTM model.

Each predicted value is fed back into the input sequence to generate the next prediction.

## Key Insights

- Shorter forecast horizons are generally easier to predict.
- Prediction error tends to increase as the forecast horizon increases.
- SimpleRNN and LSTM performance varies across forecasting horizons.
- Hyperparameter tuning provides an opportunity to improve model performance.
- News sentiment can provide additional information beyond historical prices.

## Business Use Cases

- Short-term stock price forecasting
- Investment decision support
- Risk assessment
- Portfolio planning
- Market trend analysis
- Financial analytics

## Limitations

- Stock prices are influenced by external factors such as news and macroeconomic events.
- Price-only models cannot fully capture sudden market movements.
- Recursive forecasting can accumulate prediction errors.
- The news sentiment dataset used in the project is illustrative rather than a complete historical news dataset.

## Future Improvements

- Add historical news sentiment as model input
- Include trading volume trends
- Add macroeconomic indicators
- Compare with GRU and Transformer models
- Compare with ARIMA / Prophet
- Tune additional parameters such as sequence length and batch size
- Use a larger historical dataset

## Technology Stack

| Category | Tools |
|---|---|
| Programming | Python |
| Data Handling | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn |
| Deep Learning | TensorFlow / Keras |
| Hyperparameter Tuning | GridSearchCV, SciKeras |
| NLP | VADER Sentiment |

## Project Structure

```text
Tesla-Stock-Price-Prediction/
│
├── Tesla_Prediction.ipynb
├── TSLA.csv
├── requirements.txt
├── README.md
└── models/
