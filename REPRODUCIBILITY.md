# Reproducibility Guide

This project was implemented in Google Colab using Python.

## Steps to Reproduce

1. Open `StockMarketPrediction_FYP.ipynb`.
2. Install the libraries listed in `requirements.txt`.
3. Run the stock data collection cells.
4. Run the GDELT sentiment collection cells.
5. Run the preprocessing and feature engineering cells.
6. Run the chronological train-validation-test split cells.
7. Run the model implementation cells.
8. Run the evaluation cells.
9. Review the generated charts and exported CSV outputs.

## Data Leakage Control

The project uses chronological train-validation-test splitting instead of random splitting. This ensures that models are trained on past data and evaluated on future unseen data.

## Important Note

Some GDELT and BigQuery steps may require Google Cloud authentication. Private credentials are not included in this repository.
