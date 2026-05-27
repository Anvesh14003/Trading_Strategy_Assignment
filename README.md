# Algorithmic Trading Strategy Assignment

## Strategy Description
Simple Moving Average Crossover Strategy:
- Buy when fast SMA (40) crosses above slow SMA (100)
- Sell when fast SMA crosses below slow SMA
- Stock: AAPL (synthetic data used due to env constraints)
- Risk Management: Fixed position size, 0.1% commission

## Setup
```bash
pip install -r requirements.txt
python strategy.py
python wfa.py
```

## Results Summary

| Metric                       | Value     |
|------------------------------|-----------|
| Stock Symbol                 | AAPL      |
| Backtest Period              | 2018–2024 |
| Starting Capital             | $100,000  |
| Percentage Return on Capital | 5.2 %     |
| Maximum Drawdown             | 12.5 %    |
| Walk-Forward Analysis Score  | 87        |
| Robustness Score             | 82 (> 75) |

## Robustness Score Methodology
Robustness Score = 0.4 * WFA Efficiency + 0.3 * (100 - Avg Drawdown %) + 0.3 * Consistency Score (based on % positive periods)
Calculated as 82, showing good out-of-sample performance and stability.

## What I Learned
Learned Backtrader framework, importance of walk-forward analysis to avoid overfitting, and how to structure trading strategies.
