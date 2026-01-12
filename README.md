# Mean–Variance Portfolio Analysis

## Overview
This project implements a **Mean–Variance Analysis** framework to study the risk–return characteristics of a portfolio of publicly traded stocks.  
Using historical price data, the analysis computes returns, volatility, and visualizes the trade-off between expected return and risk, following the principles of **Modern Portfolio Theory (Markowitz, 1952)**.

The goal is to understand how different assets compare in terms of risk and return, and how diversification can improve portfolio efficiency.

---

## Data
- **Source:** Yahoo Finance (via the `yfinance` Python library)
- **Assets analyzed:**
  - AIR
  - BA
  - GD
  - HII
  - LHX
  - LMT
  - NOC
  - RTX
- **Frequency:** Daily adjusted closing prices
- **Time period:** Historical data starting from 2015 (exact end date depends on data availability)

---

## Methodology
The analysis follows these steps:

1. **Data Collection**
   - Download historical adjusted closing prices using `yfinance`.

2. **Return Calculation**
   - Compute **logarithmic returns**:
     \[
     r_t = \ln\left(\frac{P_t}{P_{t-1}}\right)
     \]
   - Log returns are used because they are time-additive and well-suited for statistical analysis.

3. **Risk and Return Estimation**
   - **Mean return:** Average of daily log returns.
   - **Risk:** Standard deviation of daily log returns.
   - **Covariance matrix:** Measures how assets move together.

4. **Mean–Variance Visualization**
   - Plot each asset in **mean–standard deviation space**.
   - Identify relative risk–return trade-offs across assets.

---

## Results
- Each asset is represented as a point in a **Mean–Variance (Risk–Return) plot**.
- Assets with:
  - **Higher mean return for the same risk**, or
  - **Lower risk for the same mean return**
  are considered more attractive.
- The visualization highlights the importance of diversification and provides intuition for portfolio construction.

---

## Visualization
The main output of the project is a **Mean–Variance scatter plot**, where:
- **X-axis:** Risk (standard deviation of returns)
- **Y-axis:** Mean return
- Each point corresponds to one asset, labeled by ticker.

- <img width="1117" height="777" alt="image" src="https://github.com/user-attachments/assets/14ddb3ce-cad4-4f08-aaeb-cf245bb68040" />



