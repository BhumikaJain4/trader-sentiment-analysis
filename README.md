# Trader Performance vs Market Sentiment — Primetrade.ai Round-0 Assignment

## What is this?
This is my submission for the Primetrade.ai Data Science Intern assignment. The goal was to 
figure out whether Bitcoin market sentiment (Fear/Greed) actually affects how traders behave 
and perform on Hyperliquid.

## Datasets used
- `fear_greed.csv` — 2,644 days of daily Bitcoin Fear/Greed classifications (Feb 2018 - May 2025)
- `hyperliquid_trades.csv` — 211,224 trades from 32 unique traders on Hyperliquid (May 2023 - May 2025)
- After merging on date, we had 211,218 matched records across 547 overlapping days

## How to run
1. Put both CSV files in the same folder as the notebook
2. Install dependencies: pip install pandas numpy matplotlib seaborn scikit-learn
3. Open `trader_sentiment_analysis.ipynb` and run all cells top to bottom

## What's inside
- **Part A** — loading the data, cleaning it up, aligning dates and building the key metrics
- **Part B** — answering the 4 analysis questions with charts and written findings
- **Part C** — 2 strategy recommendations based on what the data showed
- **Bonus** — K-Means clustering (4 clusters) to group traders into archetypes and a Random 
Forest model predicting next day profitability at 65% accuracy

## Quick findings
- Extreme Fear days average ~53k daily PnL but drawdowns hit -38k — high risk, high reward
- Extreme Greed has the highest win rate (0.47) and lowest drawdown (-2.7k) — most stable period
- Frequent traders (>6,800 trades) generate 3x more PnL than infrequent ones (496k vs 144k)
- Consistent winners trade with avg position size of just $2,333 and hit a 0.69 win rate
- Sentiment is the weakest predictor of next day profitability (feature importance 0.09)

