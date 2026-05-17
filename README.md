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
## Repository Contents

This repository contains the main implementation notebook, project poster, result figures and exported model output files.

| File | Description |
|---|---|
| `StockMarketPrediction_FYP.ipynb` | Main Google Colab notebook containing the full forecasting pipeline, feature engineering, model implementation and evaluation. |
| `FYP_Poster.pptx` | Editable PowerPoint version of the final project poster. |
| `requirements.txt` | List of Python libraries required to run the notebook. |
| `.gitignore` | Excludes unnecessary or private files from the repository. |

## Key Result Figures

| File | Description |
|---|---|
| `one_step_mae_comparison.png` | Compares one-step-ahead models using MAE across the selected stocks. |
| `one_step_rmse_comparison.png` | Compares one-step-ahead models using RMSE across the selected stocks. |
| `gbm_path_mae_comparison.png` | Compares GBM path-based models using MAE. |
| `gbm_path_rmse_comparison.png` | Compares GBM path-based models using RMSE. |
| `gbm_sentiment_uncertainty_band.png` | Shows GBM + Sentiment forecast paths, actual prices and uncertainty bands. |
| `model_pipeline.png` | Shows the overall workflow from data collection to feature engineering, modelling and evaluation. |

## Exported Result Files

The repository includes CSV output files generated from the notebook. These files provide the numerical results behind the evaluation charts.

| File | Description |
|---|---|
| `final_grouped_model_comparison.csv` | Overall grouped model comparison results. |
| `final_grouped_average_comparison.csv` | Average comparison of model performance. |
| `one_step_model_comparison.csv` | One-step-ahead model comparison results. |
| `one_step_average_comparison.csv` | Average one-step-ahead model performance summary. |
| `directional_accuracy_significance_results.csv` | Directional accuracy and statistical significance results. |
| `best_model_by_ticker_and_type.csv` | Best-performing model by ticker and model category. |
| `gbm_sentiment_monthly_results.csv` | Monthly GBM + Sentiment results. |
| `gbm_sentiment_yearly_results.csv` | Yearly GBM + Sentiment results. |
| `gbm_periodic_sentiment_results.csv` | Periodic GBM + Sentiment result outputs. |
| `lstm_sentiment_results.csv` | LSTM + Sentiment model result outputs. |
| `lstm_results_no_sentiment.csv` | LSTM model results without sentiment features. |

## How to Run the Project

1. Open `StockMarketPrediction_FYP.ipynb`.
2. Run the notebook in Google Colab.
3. Install the required libraries using `requirements.txt`.
4. Run the notebook cells in order.
5. Review the exported CSV result files and PNG figures.

## Reproducibility Notes

The project uses chronological train, validation and test splitting instead of random splitting. This helps reduce data leakage by ensuring that models are trained on past data and evaluated on future unseen data.

Some GDELT and BigQuery cells may require Google Cloud authentication. Private credentials are not included in this repository.

## Academic Disclaimer

This project is for academic research only. It is not financial advice and should not be used as a live trading system..

```text
