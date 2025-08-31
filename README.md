# Pairs-Trading
Project Overview
This project explores a pairs trading strategy using Python and yfinance data. The aim was to gain hands-on experience with quantitative trading research: collecting data, identifying relationships between stocks, implementing trading rules, and evaluating profit & loss.

Methodology
Data: Daily adjusted close prices for NASDAQ-100 technology stocks (via yfinance).
Analysis:
Built correlation matrices to identify candidate pairs (e.g., AMAT & KLAC, AMAT & LRCX).
Constructed spreads and applied ±2 standard deviation bands for entry/exit signals.

Strategy:
Enter long/short positions when spread crosses thresholds.
Exit when spread reverts to the mean.
Dollar-neutral allocation on each leg.
Backtest: Simulated trades, calculated per-trade P&L, and reviewed holding periods.

Results
Demonstrated how small spread deviations can create relative value trade opportunities.
Some trades were profitable, while others showed that spreads can drift for months.
Highlighted practical challenges: transaction costs, long holding periods, and need for hedge ratios.

Limitations
Used raw correlation instead of cointegration to identify pairs.
Ignored transaction costs and slippage.
Some trades had long holding times (months), which is less realistic for pairs strategies.

Next Steps
Incorporate hedge ratios (via regression) for more balanced spreads.
Test cointegration and stationarity to validate mean reversion.
Add transaction costs and evaluate impact on profitability.
Explore rolling windows to adapt to changing correlations.

Tech Stack
Python (pandas, numpy, matplotlib, seaborn)
yfinance for data collection
Jupyter Notebook for analysis & write-up
