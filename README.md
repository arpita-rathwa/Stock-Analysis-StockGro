# 📈 Stock Analysis — StockGro
### TSA Capstone 2026 · Time Series Analysis

> A full end-to-end stock forecasting and portfolio construction project using ARIMA, Prophet, LSTM, XGBoost, GARCH, HMM, and Markowitz optimization — applied to 5 NSE-listed Indian stocks over a live 2-day trading window on StockGro.

---

## 🔴 Live Dashboard

**[→ View Interactive Dashboard](https://stock-analysis-stock-gro.vercel.app/Task0_Bonus_Dashboard.html)**

---

## 📂 Project Structure

| File | Description |
|------|-------------|
| `Task1_Stock_Universe_Selection.ipynb` | Stock selection with ADF test, rolling volatility, sector momentum |
| `Task2_Data_Preprocessing.ipynb` | Missing value handling, stationarity, MinMax scaling, train/test split |
| `Task3_Time_Series_Forecasting.zip` | ARIMA · Prophet · LSTM forecasting notebooks |
| `Task4_Volatility_Trend_Analysis.ipynb` | GARCH(1,1), rolling volatility, STL decomposition |
| `Task5_Portfolio_Construction.ipynb` | Forecast-guided + volatility-aware capital allocation |
| `Task6_Model_Comparison.ipynb` | MAPE, RMSE, directional accuracy across all models |
| `Task7_Stockgro_Execution.ipynb` | Live trade execution on StockGro platform |
| `Task8_Performance_Tracking.ipynb` | Predicted vs actual prices, live P&L, reflection |
| `Task0_Bonus_Dashboard.html` | Interactive fintech-style dashboard (all tasks visualized) |
| `Critical_fixes.ipynb` | Post-review improvements: convergence fixes, benchmark comparison |

---

## 🏦 Stock Universe

| Ticker | Sector | Allocation |
|--------|--------|-----------|
| HDFCBANK.NS | Banking | 27.3% |
| SUNPHARMA.NS | Pharmaceuticals | 22.0% |
| INFY.NS | Information Technology | 20.8% |
| HINDUNILVR.NS | FMCG | 19.7% |
| M&M.NS | Automobile | 10.3% |

**Total virtual capital:** ₹10,00,000 · **Period:** Jan 2021 – Dec 2025 · **Live window:** May 12–13, 2026

---

## 🤖 Models Used

| Model | Type | Best Metric |
|-------|------|-------------|
| **ARIMA** | Statistical | Avg MAPE: **0.97%** (best price accuracy) |
| **Prophet** | Additive | Avg Dir. Acc: **55.2%** (best direction signals) |
| **LSTM** | Deep Learning | Avg MAPE: 1.88% |
| **XGBoost** | Gradient Boosting | Avg Dir. Acc: ~52.6% |
| **GARCH(1,1)** | Volatility | Risk estimation for portfolio sizing |
| **HMM** | Probabilistic | Bull / Bear / Sideways regime detection |
| **Markowitz** | Optimization | Efficient frontier & max Sharpe portfolio |

---

## 📊 Key Results

| Metric | Value |
|--------|-------|
| Portfolio return (2-day live) | **−1.17%** (₹−11,653) |
| Best performing stock | **HDFCBANK** (+0.26%) |
| Worst performing stock | **M&M** (−3.09%) |
| ARIMA backtest MAPE | **0.97%** |
| ARIMA live MAPE | 3.67% (distribution shift on May 13) |
| Prophet live directional accuracy | **60%** |

---

## 🛠 Tech Stack

```
Python 3.12 · yfinance · pandas · numpy · statsmodels
TensorFlow / Keras · scikit-learn · XGBoost · Prophet
arch (GARCH) · hmmlearn · matplotlib · Chart.js
```

---

## 📝 Train / Test Split

| Split | Period | Days |
|-------|--------|------|
| Training | Jan 2021 – Jun 2025 | ~1,110 |
| Testing | Jul 2025 – Dec 2025 | 125 |
| Live | May 12–13, 2026 | 2 |

---

## 💡 Key Findings

- **ARIMA** was most accurate on price level (0.97% MAPE) but all models over-predicted on May 13 due to a broad NSE market decline — a known limitation of univariate models.
- **Prophet** was the best directional model (55.2% backtest, 60% live).
- **GARCH risk weighting** correctly reduced M&M allocation — M&M was the worst performer (−3.09%) while HDFCBANK, the lowest-risk stock, was the only green position (+0.26%).
- **SUNPHARMA** showed near-integrated GARCH persistence (α+β = 0.9951), indicating extremely persistent volatility — consistent with FDA/regulatory event risk.

---

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/arpita-rathwa/Stock-Analysis-StockGro.git
cd Stock-Analysis-StockGro

# Install dependencies
pip install yfinance pandas numpy statsmodels tensorflow prophet arch xgboost hmmlearn matplotlib scikit-learn

# Run notebooks in order
# Task1 → Task2 → Task3 (a/b/c/d/e) → Task4 → Task5 → Task6 → Task7 → Task8
```

> **Note:** Run Task 2 first and save the CSV outputs before running Tasks 3–8, to ensure all notebooks use the same canonical dataset.

---

*TSA Capstone 2026 · Consulting & Analytics Club*
