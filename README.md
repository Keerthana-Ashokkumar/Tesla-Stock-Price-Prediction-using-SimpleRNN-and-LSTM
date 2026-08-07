# Tesla Stock Price Prediction

## 📌 Overview
This project predicts Tesla stock closing prices using two deep learning models: **SimpleRNN** and **LSTM**. The models forecast stock prices for **1-day, 5-day, and 10-day** horizons and compare their performance using standard regression metrics.

---

## 🎯 Objectives
- Analyze Tesla historical stock price data.
- Build and train SimpleRNN and LSTM models.
- Predict future closing prices.
- Compare model performance across multiple forecasting horizons.
- Improve LSTM performance using GridSearchCV hyperparameter tuning.

---

## 🛠️ Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- TensorFlow / Keras
- SciKeras

---

## 📂 Dataset
- Tesla Historical Stock Price Dataset
- Features used:
  - Open
  - High
  - Low
  - Close
  - Volume

---

## 🤖 Models
- SimpleRNN
- LSTM
- Tuned LSTM (GridSearchCV)

---

## 📊 Evaluation Metrics
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)

---

## 📈 Results

| Horizon | Better Model |
|----------|--------------|
| 1-Day | SimpleRNN |
| 5-Day | LSTM |
| 10-Day | LSTM |

---

## 💡 Key Findings
- SimpleRNN performs better for short-term (1-day) prediction.
- LSTM achieves better accuracy for medium and long-term forecasting.
- Hyperparameter tuning improved LSTM performance.

---

## 🚀 Future Improvements
- Add technical indicators (RSI, MACD, Bollinger Bands).
- Include news sentiment analysis.
- Compare with GRU and Transformer models.
- Deploy using Streamlit or Flask.

---
