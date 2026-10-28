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

However, this project does not take the superiority of equal weighting as given.

Instead, the goal is to test the original hypothesis more carefully and ask:

> **What exactly is inefficient about market-cap weighting, under which definition of efficiency, and does equal weighting actually solve these problems?**

This distinction is important because several different concepts are often mixed together:

- return performance;
- risk-adjusted performance;
- capital diversification;
- risk diversification;
- factor exposure;
- portfolio concentration.

Even if equal weighting historically outperforms cap weighting, this does not necessarily imply that cap weighting is structurally inferior. The difference may instead come from factor exposures, systematic rebalancing, differences in concentration, or other sources of risk.

The project therefore develops naturally from:

**Cap Weighting → Equal Weighting → Equal Risk Contribution → Global Minimum Variance**

The broader objective is not simply to identify the portfolio with the highest return, but to understand how different weighting rules distribute capital and risk, and what trade-offs they create in terms of diversification, stability, estimation error, turnover, and out-of-sample performance.

## Project Pipeline

1. **EW vs CW within industries**  
   Exploratory comparison of equal- and cap-weighted industry portfolios.

2. **EW vs CW aggregate portfolios**  
   Construct proper aggregate indices and compare return, volatility, Sharpe, drawdown, and tracking error.

3. **Capital diversification**  
   Compare HHI, effective number of industries, weight dispersion, and concentration over time.

4. **Risk diversification**  
   Compare risk contributions and the effective number of risk contributors.

5. **Add ERC / Risk Parity**  
   Move from equal capital allocation to equal risk allocation.

6. **Add GMV**  
   Test whether minimizing estimated variance reduces realized out-of-sample risk.

7. **Common walk-forward backtest**  
   Compare CW, EW, ERC, and GMV under a consistent out-of-sample framework.

8. **Interpretation**  
   Explain differences through concentration, covariance structure, rebalancing, turnover, and estimation error.

### Core progression

**CW → EW → Capital Diversification → Risk Diversification → ERC → GMV → Out-of-Sample Comparison → Interpretation & Robustness**