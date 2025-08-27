# Mean Reversion Trading Strategy on US ETFs

This project explores a mean reversion trading strategy applied to major US ETFs (SPY, QQQ, IWM). 
The strategy is implemented in Python and validated using **walk-forward analysis** to minimize overfitting risk.  

---

## 📌 Project Overview

- **Goal:** Explore mean reversion strategies using Z-scores of rolling returns as a hands-on exercise in quantitative trading, focusing on understanding signal generation, backtesting, and performance evaluation.   
- **Assets:** SPY (S&P 500), QQQ (Nasdaq 100), IWM (Russell 2000).  
- **Methodology:**
  - Calculate rolling mean & standard deviation of returns
  - Generate signals when Z-score exceeds thresholds
  - Apply filters using trend indicators (EMA)
  - Backtest with slippage and transaction costs
  - Optimize parameters (lookback window, Z-threshold)
  - Validate robustness using **walk-forward validation**

---

## ⚙️ Key Features

- **Backtesting Framework** with realistic assumptions (slippage & commissions).  
- **Performance Metrics:** Annualized Return, Volatility, Sharpe, Sortino, CAGR, Max Drawdown, Win Rate.  
- **Rolling Sharpe Ratio Analysis** to capture stability over time.  
- **Parameter Optimization** (grid search on lookback & z-threshold).  
- **Walk-Forward Validation**:
  - Trains on rolling windows (~1 year)
  - Tests on next window (~3 months)
  - Avoids overfitting by continuously re-optimizing parameters

---

## 📊 Results & Insights

- Walk-forward analysis shows **mixed performance** across windows:  
  - Some periods with positive Sharpe ratio  
  - Others with negative returns and drawdowns  
- Comprehensive analysis shows limited robustness and unfavorable risk-adjusted returns, indicating the strategy is not suitable for deployment.  
- Demonstrates importance of **robust validation and risk management**  

### Example Outputs:
- **Cumulative Returns (Strategy vs Buy&Hold)**  
- **Drawdown analysis with stress periods**  
- **Heatmaps of Sharpe ratio across parameter space**  
- **Rolling Sharpe ratio distribution**  

---

## 🛠️ Tech Stack

- **Python** (pandas, numpy, matplotlib, seaborn)  
- **Yahoo Finance API (yfinance)** for data  
- **SciPy** for statistical analysis  

---

## 📈 Potential Extensions

- Test with intraday data (5m / 15m intervals)  
- Add advanced execution logic (dynamic position sizing)  
- Explore other mean-reversion indicators (Bollinger Bands, Ornstein-Uhlenbeck models)  
- Portfolio construction across multiple ETFs  
