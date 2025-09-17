---

# Portfolio Analysis and Sharpe Ratio Optimization

This project applies quantitative finance and data science techniques to analyze the performance of several technology stocks (AAPL, MSFT, GOOGL, AMZN, TSLA) and optimize a portfolio based on the Sharpe ratio.

---

## Features

* Automatic stock data download using `yfinance`
* Data cleaning and transformation (Close, Open, Volume)
* Integration of U.S. holidays to filter market data
* Financial calculations:

  * Simple and logarithmic returns
  * Cumulative returns
  * Annualized volatility (30-day rolling window)
  * Sharpe ratio per stock
* Portfolio optimization with `scipy.optimize`:

  * Sharpe ratio maximization
  * Weight constraints (sum = 1, no short selling)
* Visualizations with `matplotlib`:

  * Normalized stock performance (base 100)
  * Cumulative returns
  * Annualized volatility
  * Sharpe ratio bar chart

---

## Technologies Used

* Python 3.x
* yfinance
* pandas
* numpy
* matplotlib
* scipy
* holidays

---

## Possible Improvements

* Add more stocks or sectors to diversify the analysis
* Test different frequencies (weekly, monthly)
* Compare optimization methods (e.g., classical Markowitz)
* Build an interactive interface (Dash, Streamlit)

---

## Disclaimer

This project is for educational purposes only.
It does **not** constitute investment advice.
