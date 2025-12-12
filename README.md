# ds_sunidhi

Web3 Trading Team — Data Science Assignment

This repository contains a complete analysis of how trader behavior correlates with market sentiment (Fear vs. Greed), using Hyperliquid trading data and the Bitcoin Fear–Greed Index.
The project includes dataset preprocessing, merged analysis, visualization, and lightweight predictive modeling.
```
📂 Repository Structure
ds_<yourname>/
│
├── notebook_1.ipynb               # Data cleaning, merging, and EDA
├── notebook_2.ipynb               # Simple ML models (classification & regression)
│
├── csv_files/
│   ├── fear_greed_index.csv
│   ├── historical_data.csv
│   └── hist_with_sentiment.csv    # processed + merged final dataset
│
├── outputs/
│   ├── pnl_vs_sentiment.png
│   ├── volume_reaction.png
│   ├── risk_analysis.png
│   ├── confusion_matrix.png
│   ├── actual_vs_predicted_pnl.png
│   ├── reg_feature_importance.png
│   └── test_set_with_predictions.csv
│
├── ds_report.pdf                  # Final detailed written report


🎯 Objective
To analyze how trading decisions (risk exposure, trade size, profitability) change during different market sentiment regimes and to evaluate whether simple machine learning models can identify loss-prone trades or estimate expected PnL.


📊 Datasets Used
1. Bitcoin Fear & Greed Index
Contains:
timestamp
value (0–100 sentiment score)
classification (Fear / Greed)
date

2. Hyperliquid Trader Data
Contains:
Account, Coin, Execution Price
Size Tokens, Size USD
Side, Start Position, Direction
Closed PnL, Fee
Timestamp IST, Timestamp

Both datasets were merged on date after proper timestamp normalization.


🔍 Notebook 1 — Data Preparation & EDA
This notebook covers:
Parsing and cleaning timestamps
Date extraction from Timestamp IST

Feature engineering:
trade_volume
risk_exposure
Merging sentiment data with trader data

Visual analysis including:
PnL comparison (Fear vs Greed)
Risk exposure distribution
Trade volume behavior
Sentiment score trends

All visual outputs are saved in /outputs.


🤖 Notebook 2 — Lightweight Machine Learning
Since complex models were too heavy for Colab, Notebook 2 uses simple and efficient models:

1. Binary Classification
Predict whether a trade will result in a loss.

Model:
✔ Logistic Regression

Features used:
trade_volume
risk_exposure
value (sentiment score)

Outputs:
Classification report
Confusion matrix

2. Regression
Predict the Closed PnL of a trade.
Model:
✔ Random Forest Regressor (20 trees)

Outputs:
RMSE score
Actual vs predicted PnL plot
Simple feature importance chart

All model outputs are stored in /outputs.

🧠 Key Findings
Traders take larger and riskier positions during Greed conditions.
Loss-making trades are strongly linked to high risk exposure.
Sentiment score influences volatility, not direct profitability.
Even simple models detect consistent behavioral patterns in trader activity.

▶️ How to Run This Project
Open notebooks in Google Colab
Upload:
fear_greed_index.csv
historical_data.csv
Run notebook_1.ipynb
Generates merged dataset + visualizations
Run notebook_2.ipynb
Trains lightweight models
Saves predictions and charts in /outputs


📄 Final Report
The file ds_report.pdf includes:
Project introduction
Methodology
Dataset explanation
EDA insights
Model results
Conclusions & recommendations

```
