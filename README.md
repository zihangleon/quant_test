
# Single SMA Backtesting Strategy

This project implements a **single SMA trading strategy** for cryptocurrencies in a Jupyter Notebook. Buy/sell signals are generated when the price crosses above/below the SMA. The backtest simulates full-position long/short trades with optional transaction fees.

**Requirements:**  
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
‘’‘
Features:

Test multiple SMA periods and compare performance.

Track total return, number of trades, max drawdown, and Sharpe ratio.

Output equity curves, trade logs, and a performance summary CSV.

Insights:

SMA(20) performed best in this dataset (lowest loss, moderate drawdown).

Short-period SMAs are sensitive to noise and lead to frequent losing trades.

Improvements:

Add signal filtering, stop-loss/take-profit rules, or dual SMA crossover.

Test across different market conditions to optimize SMA selection.

Usage Example:

python
Copy code
df_bt, trades, perf = backtest_single_sma(df, sma_period=10, initial_capital=100000, fee=0.0002)
