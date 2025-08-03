# 📈 Algo Trading System (RSI + Moving Average Strategy with ML Validation)

This project implements a basic **algorithmic trading strategy** using technical indicators and evaluates its effectiveness using **machine learning**. It also features **automated logging to Google Sheets** for real-time tracking of trades and strategy performance.

---

## 🔍 Strategy Overview

- **Buy Signal Criteria:**
  - RSI (Relative Strength Index) < 30 _(oversold)_
  - 20-Day SMA > 50-Day SMA _(short-term uptrend)_

- **Trade Execution:**
  - Buy on signal day
  - Sell after 5 trading days
  - Log return and whether the trade was a win/loss

- **ML Integration:**
  - Features like RSI, SMA, volatility, and momentum are used
  - Model: XGBoost Classifier (used due to higher accuracy vs Logistic/Decision Tree)
  - Accuracy is logged per stock for performance validation

---


## 🧪 Sample Output

**Example Result from Strategy Run:**

| Metric         | Value   |
|----------------|---------|
| Total Trades   | 16      |
| Win Ratio      | 0.56    |
| Avg Return (%) | 0.44%   |
| Avg ML Accuracy | ~84%   |

> Note: The above results are from a sample run and will vary depending on market conditions.

---

## 🔗 Google Sheets Logging

Trades and summary results are automatically logged to a connected Google Sheet:

- **Sheet 1:** Trade Log (Buy/Sell records, returns)
- **Sheet 2:** Summary (Total trades, Win Ratio, Avg Return %)

✅ Sheets are **overwritten each time the function runs**, ensuring fresh logs.

---

## ⚙️ Setup Instructions

### 1. Clone Repository

```bash
git clone https://github.com/DivyanshiRw/Algo-Trading-System.git
cd Algo-Trading-System
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Setup Google Sheets Logging (Optional)

- Create a Google Cloud project and enable Google Sheets API
- Download gcreds.json and place it in the root folder (already .gitignored)

---

🤖 Tech Stack
Python (Pandas, NumPy, scikit-learn)

XGBoost (ML Model)

Google Colab (for development)

gspread (for Google Sheets)

yfinance (fetch stock data)

---
✅ Strategy implementation with logic

✅ ML component with accuracy report

✅ Backtesting logic with trade summary

✅ Google Sheets integration

✅ Clean documentation and modular functions

✅ README + Sample Output + .gitignore for secure handling
