# 📊 Portfolio Analysis and Sharpe Ratio Optimization

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

> Portfolio analysis and Sharpe Ratio optimization for major tech stocks (AAPL, GOOGL, TSLA, MSFT)

## 📋 Description

This project applies **quantitative finance** and **data science** techniques to analyze the historical performance of 4 major tech stocks and build an optimal portfolio that maximizes the Sharpe Ratio.

### 🎯 Objectives

1. **Analyze** historical stock performance over 3 years (2022-2025)
2. **Calculate** key financial metrics (returns, volatility, Sharpe Ratio)
3. **Optimize** portfolio allocation to maximize risk-adjusted returns
4. **Visualize** results through professional charts

## 🚀 Features

| Feature | Description |
|---------|-------------|
| 📥 Data | Automatic download via Yahoo Finance |
| 🧹 Cleaning | US holidays filtering |
| 📈 Metrics | Simple, log, cumulative returns + volatility |
| ⚡ Optimization | Sharpe Ratio maximization (scipy) |
| 📊 Visualization | 5 interactive charts with matplotlib |

## 📁 Project Structure

```
Sharpe-Ratio-optimization/
├── Sharpe_ratio_optimization.ipynb   # Main notebook
├── README.md                          # Documentation
├── requirements.txt                   # Python dependencies
├── .gitignore                         # Git ignored files
├── LICENSE                            # MIT License
└── docs/
    └── Projet_1_de_python.pdf         # Detailed report
```

## 🛠️ Installation

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Install Dependencies

```bash
# Clone the repository
git clone https://github.com/yanis75fr/Sharpe-Ratio-optimization.git
cd Sharpe-Ratio-optimization

# Create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # Linux/Mac
# or
venv\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements.txt
```

## 💻 Usage

### Run the Notebook

```bash
jupyter notebook Sharpe_ratio_optimization.ipynb
```

### Quick Start

Run all cells in order to:
1. Download stock data
2. Calculate financial metrics
3. Visualize performance
4. Get optimal portfolio allocation

## 📐 Methodology

### 1. Data Acquisition

Historical data is retrieved via the **yfinance** API for the following stocks:
- **AAPL** (Apple)
- **GOOGL** (Alphabet/Google)
- **TSLA** (Tesla)
- **MSFT** (Microsoft)

### 2. Financial Metrics

| Metric | Formula | Description |
|--------|---------|-------------|
| Simple Return | $R_t = \frac{P_t - P_{t-1}}{P_{t-1}}$ | Percentage change between two days |
| Log Return | $R_{log} = \ln(\frac{P_t}{P_{t-1}})$ | Logarithmic return (additive) |
| Cumulative Return | $R_{cum} = \prod(1 + R_i)$ | Total performance since start |
| Annualized Volatility | $\sigma_{ann} = \sigma_{daily} \times \sqrt{252}$ | Risk measure |
| **Sharpe Ratio** | $\frac{R_a - R_f}{\sigma_a}$ | Excess return per unit of risk |

### 3. Portfolio Optimization

The optimization problem solved:

$$\max_{w} \frac{E[R_p] - R_f}{\sigma_p}$$

Subject to:
- $\sum_i w_i = 1$ (budget constraint)
- $w_i \geq 0$ (no short selling)

**Method:** Sequential Least Squares Programming (SLSQP) via `scipy.optimize`

## 📊 Results (Example)

### Individual Sharpe Ratios

| Stock | Sharpe Ratio |
|-------|--------------|
| AAPL  | 0.52         |
| GOOGL | 0.41         |
| MSFT  | 0.41         |
| TSLA  | 0.31         |

### Optimal Allocation

| Stock | Weight |
|-------|--------|
| AAPL  | ~72%   |
| GOOGL | ~19%   |
| MSFT  | ~6%    |
| TSLA  | ~3%    |

### Optimized Portfolio Performance

- **Expected Annual Return:** ~15%
- **Annualized Volatility:** ~26%
- **Sharpe Ratio:** ~0.49

## 📈 Visualizations

The notebook generates 5 charts:

1. **Normalized Performance (Base 100)** - Visual comparison of stocks
2. **Cumulative Returns** - Investment evolution over time
3. **Annualized Volatility** - Risk on 30-day rolling window
4. **Sharpe Ratio by Stock** - Risk-adjusted performance ranking
5. **Optimal Allocation** - Pie chart + comparison with individual stocks

## 🔧 Technologies Used

| Library | Version | Purpose |
|---------|---------|---------|
| `yfinance` | ≥0.2.0 | Stock data download |
| `pandas` | ≥1.5.0 | Data manipulation |
| `numpy` | ≥1.23.0 | Numerical computations |
| `matplotlib` | ≥3.6.0 | Visualization |
| `scipy` | ≥1.9.0 | Mathematical optimization |
| `holidays` | ≥0.25 | US holidays management |

## 📝 Possible Improvements

- [ ] Add more stocks/sectors for diversified analysis
- [ ] Implement Markowitz efficient frontier
- [ ] Test different frequencies (weekly, monthly)
- [ ] Compare with Black-Litterman model
- [ ] Create interactive interface with Streamlit or Dash
- [ ] Add out-of-sample backtesting
- [ ] Integrate tail risk management (CVaR, Expected Shortfall)

## 📄 Documentation

The detailed project report is available in [`docs/Projet_1_de_python.pdf`](docs/Projet_1_de_python.pdf).

## 👤 Author

**Yanis Calvo**

- GitHub: [@yanis75fr](https://github.com/yanis75fr)

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

⭐ If you found this project useful, please consider giving it a star!
