# PCA-Based Eigen Portfolio Optimization

##  Overview

This project implements a **quantitative portfolio optimization strategy** using eigenvalue decomposition via Principal Component Analysis (PCA).

The goal is to construct **eigen-portfolios** from stock return data and evaluate their performance using risk-adjusted metrics.

---

##  Objectives

* Analyze stock return correlations and extract latent risk factors
* Construct portfolios using principal components
* Optimize portfolios based on Sharpe Ratio
* Compare performance with an equal-weight benchmark
* Perform out-of-sample backtesting

---

##  Methodology

### 1. Data Preprocessing

* Used historical adjusted closing prices of Dow Jones stocks
* Computed daily returns (log & percentage)
* Removed outliers beyond 3 standard deviations
* Standardized data for PCA

---

### 2. PCA & Eigen Portfolio Construction

* Applied PCA on standardized returns
* Extracted principal components (eigenvectors)
* Converted components into portfolio weights

---

### 3. Portfolio Evaluation

* Calculated:

  * Annualized Return
  * Volatility
  * Sharpe Ratio
* Selected:

  * Best Sharpe portfolio
  * Maximum return portfolio

---

### 4. Backtesting

* Split data into train (80%) and test (20%)
* Evaluated performance on unseen data
* Compared against equal-weight portfolio

---

##  Results

| Portfolio Type               | Return | Volatility | Sharpe Ratio |
| ---------------------------- | ------ | ---------- | ------------ |
| Equal Weight Portfolio       | 16.24% | 9.97%      | 1.63         |
| Eigen Portfolio (Max Sharpe) | 15.86% | 10.12%     | 1.57         |
| Eigen Portfolio (Max Return) | 51.81% | 128.11%    | 0.40         |

###  Key Insights

* Equal-weight portfolio achieved the highest Sharpe ratio due to diversification
* Eigen portfolios captured latent market factors but introduced higher volatility
* Maximizing returns alone leads to excessive risk
* Risk-adjusted optimization is crucial for portfolio selection

---

##  Tech Stack

* Python
* NumPy
* Pandas
* Scikit-learn
* Matplotlib

---

##  How to Run

1. Clone the repository

```bash
git clone https://github.com/your-username/eigen-portfolio.git
cd eigen-portfolio
```

2. Install dependencies

```bash
pip install -r requirements.txt
```

3. Run the notebook

```bash
jupyter notebook
```

---

##  Future Improvements

* Add portfolio constraints (long-only, weight normalization)
* Include transaction costs
* Implement rolling window backtesting
* Extend to multi-factor models

---

##  Learnings

* Practical application of PCA in finance
* Importance of risk-return tradeoff
* Portfolio evaluation using Sharpe ratio
* Backtesting strategies on time-series data

---

##  Contact

If you have any questions or suggestions, feel free to connect!

---

