# 📈 NIFTY 50 Forecasting & Trading Strategy using ML + Prophet

This project builds a **multi-factor predictive trading system** for the Indian stock index **NIFTY 50**, combining:

- 🔮 **Time Series Forecasting** (Prophet)
- 🤖 **Machine Learning Models** (Logistic Regression, Random Forest, LSTM)
- 📊 **Technical Indicators** (RSI, MACD, Bollinger Bands, SMA)
- 🧠 **Sentiment Analysis** (Economic Times RSS + VADER)
- ⚖️ **Risk-Controlled Strategy Simulation** (TP/SL logic + cost + spacing)

---

## 🧠 About the Project

This repo showcases an end-to-end intelligent market prediction pipeline. It forecasts market direction and simulates realistic trading performance with risk-adjusted thresholds and ensemble logic.

> **Objective:** Beat the market by predicting 3-day price movement and filtering entries through ensemble modeling + Prophet confirmation.

---

## 🔧 Setup Instructions

pip install yfinance prophet scikit-learn ta vaderSentiment feedparser matplotlib pandas numpy


🧪 How It Works

🛠 Feature Engineering
	•	RSI, MACD, MACD Signal
	•	Bollinger Bands, SMA
	•	India VIX from Yahoo Finance
	•	Daily sentiment scores from Economic Times headlines (via RSS + VADER)
	•	Lagged returns for context
	•	yhat forecast from Prophet

📈 Forecasting
	•	Facebook Prophet used with technical + sentiment regressors
	•	yhat acts as a filter: only trade if model and Prophet both agree

⚙️ ML Modeling
	•	Classification target: Will return > TP threshold in next 3 days?
	•	Models tested:
	•	Logistic Regression
	•	Random Forest
	•	LSTM (optional extension)
