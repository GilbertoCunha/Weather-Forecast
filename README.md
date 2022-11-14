## Weather Forecasting

This repository encompasses a weather forecasing task using the Kaggle dataset present in "https://www.kaggle.com/datasets/balabaskar/historical-weather-data-of-all-country-capitals".

This repository showcases many skills necessary to tackle this kind of problem:
- `1-eda.ipynb`: exploratory data analysis to understand the data, its features and their relationship. Showcases scatter plots, seasonal plots, power spectral density analysis and ACF plots.

- `2-model.ipynb`: creating a data pipeline and performing model validation using time-series cross validation.

- `3-eval.ipynb`: evaluating the model trained in the previous notebook under a wide range of different metrics.
    - Point forecasts: evaluated using MASE
    - Quantile forecasts: evaluated using pinball loss function
    - Prediction interval: evaluated using Wrinkler score 
    - Forecast distribution: evaluated using CRPS