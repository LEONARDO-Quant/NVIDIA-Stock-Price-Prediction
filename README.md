# 📈 NVIDIA Stock Return Prediction: A Multi-Model ML Approach
> **Advanced Machine Learning capstone project developed for the "Sorbonne Data Analytics" Professional Graduate Degree at Université Paris 1 Panthéon-Sorbonne.**

![NVIDIA](https://img.shields.io/badge/Focus-NVIDIA_Returns-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![ML](https://img.shields.io/badge/Machine_Learning-XGBoost_%7C_LSTM_%7C_ARIMAX-blueviolet?style=for-the-badge)

## 🎯 Project Overview

Can we predict the daily returns of the world's AI infrastructure leader? This project analyzes **NVIDIA (NVDA)** stock dynamics from 2018 to 2026, leveraging a hybrid dataset of financial technicals, competitor data, and macroeconomic indicators.

We move beyond simple price prediction to focus on **Daily Returns**, addressing the non-linear complexity and high volatility of the modern semiconductor market.

-----

## 🏗️ The Pipeline

The project follows a rigorous data science workflow to ensure statistical validity:

1.  **Data Collection:** Sourcing from Yahoo Finance and Federal Reserve (FRED).
2.  **Feature Engineering:** Implementation of lagged variables (1-10 days), rolling volatility windows (10/21 days), and cyclic calendar features.
3.  **Data Cleaning:** Log-return transformations to ensure **stationarity** (confirmed via ADF test, p=0.000).
4.  **Modeling:** Benchmarking traditional econometrics against Deep Learning and Gradient Boosting.

-----

## 📊 Features & Dataset

We integrated diverse data streams to capture the "NVIDIA Ecosystem":

  * **Competitors:** AMD, TSMC, Intel.
  * **Market Indices:** S\&P500, NASDAQ, SOXX (Semiconductor Index).
  * **Macro Indicators:** US10Y (Treasury yields), DXY (Dollar Index), CPI, FED Rates, and a COVID-19 dummy variable.
  * **Volatility:** VXN (Nasdaq 100 Volatility).

-----

## 🤖 Models & Performance

We compared three distinct architectures to find the optimal predictive balance:

| Model | Typology | Key Performance | Conclusion |
| :--- | :--- | :--- | :--- |
| **🏆 XGBoost** | **Boosted Trees** | **MAE: 0.013 | R²: 0.65** | **Winner:** Best at capturing non-linear market relations. |
| **ARIMAX** | **Econometrics** | MAE: 0.014 | R²: 0.62 | Solid baseline, but struggles with volatility peaks. |
| **LSTM** | **Deep Learning** | MAE: 0.015 | R²: 0.58 | Sub-optimal; requires larger data volume for convergence. |

-----

## 💡 Key Insights

  * **Sector Dominance:** NVIDIA’s returns are most heavily influenced by the **SOXX** (Semiconductor index) and **AMD**'s performance (lagged).
  * **Volatility Matters:** Inclusion of the VXN index and rolling volatility significantly improved model convergence (LSTM RMSE dropped by 24%).
  * **The "AI Explosion":** The data clearly marks three phases: pre-2020 growth, post-COVID acceleration, and the current AI-driven "explosion".

-----

## 🚀 Future Perspectives

To further enhance the accuracy ($R^2$), future iterations will include:

  * **Sentiment Analysis:** Scraping news and financial reports.
  * **Options Data:** Incorporating put/call ratios for better volatility forecasting.
  * **Advanced Architectures:** Testing Transformer-based models for time-series.
