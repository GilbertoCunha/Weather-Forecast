<h1 align="center"> Weather Forecasting </h1>

This repository encompasses a weather forecasing task using the Kaggle dataset present in "https://www.kaggle.com/datasets/balabaskar/historical-weather-data-of-all-country-capitals".

<h1 align="center"> Tools used </h1>
<p align="center"> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://numpy.org/" target="_blank" rel="noreferrer"> <img src="https://numpy.org/doc/stable/_static/numpylogo.svg" alt="numpy" width="100" height="40"/> </a> <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/> </a> <a href="https://scipy.org/" target="_blank" rel="noreferrer"> <img src="https://scipy.org/images/logo.svg" alt="scipy" width="40" height="40"/> </a> <a href="https://seaborn.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="seaborn" width="40" height="40"/> </a> <a href="https://www.sktime.org/en/stable/" target="_blank" rel="noreferrer"> <img src="https://www.sktime.org/en/stable/_static/sktime-logo-text-horizontal.png" alt="sktime" height="35"/> </a> </p>
<p align="center"> <a href="https://www.statsmodels.org/stable/" target="_blank" rel="noreferrer"> <img src="https://www.statsmodels.org/stable/_images/statsmodels-logo-v2-horizontal.svg" alt="statsmodels"  height="35"/> </a> </p>

The main code is scattered across three notebooks:

<h1 align="center"> 1 - Exploratory data analysis </h1>

In the notebook `1-eda.ipynb`, I perform exploratory data analysis on the data:
- Check for missing values and data types
- Filter the weather data to focus on a particular city
- Time-plots, seasonal and ACF-plots
- Power spectral decomposition
- Trend-cycle and seasonal decomposition using `statsmodels`
- Measure signal forecastability using trend and seasonal strength and Shannon spectral entropy

<h1 align="center"> 2 - Model selection and tuning </h1>

This notebook, `2-models.ipynb`, create a simple Naive seasonal model for making weather forecasts using the `sktime` package.

The following approach is used:
- Creating a data pipeline
- Training and performing time-series cross-validation on the Naive seasonal model
- Saving the pipeline for later evaluation

<h1 align="center"> 3 - Model evaluation </h1>

Notebook `3-eval.ipynb` evaluates the model from the previous notebook and benchmarks it across various different metrics on the test set.

The evaluation consists of the following steps:
- Forecast vs true time-plot with prediction interval
- Point forecast evaluation using the MASE (Mean absolute scaled error) metric
- Quantile evaluation using the pinball loss metric
- Prediction interval evaluation using the Wrinkler score
- Forecast distribution evaluation using the CRPS (Continuous Ranked Probability Score) metric
