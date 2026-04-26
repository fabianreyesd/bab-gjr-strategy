# BAB-GJR: Betting Against Beta with Conditional Volatility

MSc Finance project — Católica Lisbon School of Business & Economics  
**Authors:** André Lopez · Alice Dubuis · Fabián Reyes Díaz

---

## What this is

Implementation and comparison of two systematic long/short equity strategies based on Frazzini & Pedersen (2014)'s Betting Against Beta factor.

- **BAB-OLS** — rolling beta estimation using a standard 5-year OLS window (the FP benchmark)
- **BAB-GJR** — conditional betas from GJR-GARCH(1,1) market variance + EWMA covariance (our extension)

Data: CRSP daily returns via WRDS · Universe: ~2,500 US stocks/month · Period: 2000–2022

---

## Results (Out-of-Sample, 2016–2022)

| | BAB-OLS | BAB-GJR |
|---|---|---|
| Sharpe ratio | 0.19 | **0.64** |
| Ann. return | 1.68% | **6.44%** |
| Max drawdown | −25.66% | **−13.44%** |
| CAPM α/month | 16 bp | **51 bp** |

---

## Files

| File | Description |
|---|---|
| `BAB-GJR.ipynb` | Full pipeline from raw CRSP data to final performance tables |
| `BAB_GJR_Report.pdf` | Written report (13 pages) |

---

## Stack

Python · pandas · numpy · statsmodels · arch · matplotlib · WRDS
