# BCU_FYP
Final Project: A Comparative Evaluation of GBM, LSTM, and GDELT-Based Sentiment Models for Stock Price Forecasting 
# A Comparative Evaluation of GBM, LSTM, and GDELT-Based Sentiment Models for Stock Price Forecasting

## Project Overview

This project is a Python-based forecasting and model comparison framework developed for a final year project. It evaluates whether advanced forecasting models and GDELT-based sentiment features improve short-term stock price prediction compared with simple baseline models.

The artefact compares baseline, machine learning, deep learning, stochastic simulation and sentiment-enhanced models across nine selected stocks.

## Models Compared

The project compares the following models:

- Random Walk
- Linear Regression
- LSTM
- LSTM + Sentiment
- Basic Monthly GBM
- Periodic GBM
- GBM + Sentiment
- Periodic GBM + Sentiment

## Data Used

The project uses:

- Daily OHLCV stock data for WMT, NVDA, AMD, KO, JNJ, MSFT, AAPL, AMZN and NFLX
- Aggregated daily GDELT sentiment data
- Technical indicators such as returns, moving averages, volatility, momentum and volume-based features

## Methodology

The forecasting pipeline follows these stages:

1. Stock data collection
2. GDELT sentiment data collection
3. Data cleaning and preprocessing
4. Technical feature engineering
5. Sentiment feature engineering
6. Chronological train-validation-test splitting
7. Model implementation and training
8. Model evaluation
9. Statistical and directional testing
10. Result export and visualisation

## Evaluation Metrics

The models were evaluated using:

- MAE
- RMSE
- MAPE
- sMAPE
- MASE
- Mean Error
- Directional Accuracy

The one-step-ahead models and GBM path-based models were evaluated separately because they produce different forecast structures.

## Key Findings

- Random Walk achieved the strongest one-step-ahead forecasting performance overall.
- LSTM performed best for selected stocks such as WMT and JNJ, but did not outperform Random Walk overall.
- LSTM + Sentiment did not improve average next-day forecasting performance.
- Basic Monthly GBM achieved the lowest average GBM path-based error.
- GBM + Sentiment improved performance for selected stocks but did not improve overall average performance.

## Main Conclusion

The project shows that more complex models and sentiment features do not automatically improve short-term stock forecasting. The main contribution is a controlled comparison framework rather than a claim that stock prices can be reliably predicted.

PNG result figures               MAE, RMSE, GBM path error and pipeline visuals

## Repository Contents

```text
StockMarketPrediction_FYP.ipynb   Main Google Colab notebook
README.md                        Project overview and documentation
requirements.txt                 Python libraries required to run the project
.gitignore                       Files excluded from the repository

How to Run
Open StockMarketPrediction_FYP.ipynb.
Run the notebook in Google Colab.
Install the required packages listed in requirements.txt.
Run the cells in order.
Review the generated model results, charts and exported outputs.
Reproducibility Notes

The project uses chronological train-validation-test splitting to reduce data leakage. This ensures that models are trained on past data and tested on future data.

Some GDELT/BigQuery cells may require Google Cloud authentication. Private credentials are not included in this repository.

Disclaimer

This project is for academic research only. It is not financial advice and should not be used as a trading system.

```text
