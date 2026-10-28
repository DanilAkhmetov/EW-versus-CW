## Short Description

Here you will find my notebooks in which I examined how cap-weighted portfolio construction method differs from some other alternatives.

I first compare capitalization-weighted and equal-weighted portfolios using long-run **Kenneth French** and **CRSP data**. I then move to a stock-level universe and compare CW, EW, ERC, and GMV portfolios.

## Motivation

This project began with a simple but provocative idea: **market-cap weighting may be a natural way to construct a portfolio, but not necessarily an efficient one.**

The initial motivation came from the claim that even a very simple allocation rule such as **equal weighting** can outperform a cap-weighted portfolio, including on a risk-adjusted basis.

Early evidence from Kenneth French industry portfolios appeared to support this view. Equal-weighted portfolios often showed stronger historical performance than their value-weighted counterparts, which initially led to a strong hypothesis:

> If a naive equal-weighted portfolio can outperform a cap-weighted portfolio, perhaps market-cap weighting is a fundamentally inefficient way to allocate capital.

Several intuitions support this argument.

Under cap weighting, more capital is allocated to the largest companies. As a result, the portfolio may:

- become concentrated in large-cap stocks;
- underweight small- and medium-sized companies;
- have lower exposure to the size premium;
- potentially have lower exposure to value characteristics;
- concentrate portfolio risk in a relatively small part of the investment universe;
- have a much lower effective number of constituents than the nominal number of holdings suggests.


The project therefore develops naturally from:

**Cap Weighting → Equal Weighting → Equal Risk Contribution → Global Minimum Variance**

The broader objective is not simply to identify the portfolio with the highest return, but to understand how different weighting rules distribute capital and risk, and what trade-offs they create in terms of diversification, stability, estimation error, turnover, and out-of-sample performance.

## Project Structure

The empirical analysis is organized into three notebooks:

### `01_KF_inds_CRSP.ipynb`

This notebook compares equal-weighted and value-weighted portfolios using:

- Kenneth French industry portfolios across several industry classifications;
- different historical starting periods, including samples extending back to 1926;
- CRSP equal-weighted and value-weighted market indices.

The purpose is to examine whether the apparent advantage of equal weighting is persistent across datasets and time periods.

---

### `02_100stock.ipynb`

Contains the analysis on a fixed set of 81 stocks over the sample period.

The notebook compares:

- Capitalization Weighting (CW)
- Equal Weighting (EW)
- Equal Risk Contribution (ERC)
- Global Minimum Variance (GMV)

The analysis focuses not only on returns and volatility, but also on:

- effective number of constituents;
- risk contributions;
- effective number of risk contributors;
- portfolio concentration;

---

### `03_expost.ipynb`

Examines the role of covariance estimation error.

The main analysis constructs ERC and GMV portfolios using covariance matrices estimated from past returns. This notebook instead considers an oracle setting in which the covariance structure of the next 36 months is treated as if it were known in advance.

Future expected returns are **not** assumed to be known.

The comparison therefore asks:

> How would covariance-based portfolio construction behave if future risk could be estimated perfectly?