# Trader Performance vs Market Sentiment
**Primetrade.ai — Round 0 Assignment**

## Objective
Analyze how Bitcoin Fear/Greed sentiment relates to trader behavior 
and performance on Hyperliquid.

## Setup
Install required libraries:
pip install pandas numpy matplotlib seaborn scikit-learn

## How to Run
1. Place both CSV files in the same folder as the notebook
2. Open data_science.ipynb in Jupyter or VS Code
3. Run All Cells top to bottom

> Note: historical_data.csv is 45MB — download from:
> [Download](https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing)

## Methodology
- Loaded and cleaned both datasets, aligned by date
- Computed daily PnL, win rate, drawdown proxy, long/short ratio
- Segmented traders by leverage, frequency, and consistency
- Applied KMeans clustering to identify 3 trader archetypes
- Trained Random Forest model to predict next-day profitability

## Key Insights
1. Greed days show higher win rates and larger average trade sizes
2. Long/Short ratio exceeds 1 during Greed — traders prefer long positions
3. Deepest drawdowns occur on Greed days — position discipline is critical
4. Today's PnL is the strongest predictor of next-day profitability (~52% accuracy)

## Strategy Recommendations
1. Reduce position size 30-40% during Extreme Fear days
2. Favor long setups during Greed, stay flat during Fear
