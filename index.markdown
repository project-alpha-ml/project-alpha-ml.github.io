---
layout: default
---
## About

Project Alpha explores active investing in the US stock market using advanced machine learning and rules-based strategies. The project aims to devise profitable strategies by extracting patterns from an extensive dataset, comprising price data, news sentiment, fundamental data, corporate actions, and macroeconomic data. All data are sourced from publicly available, free APIs.

## Approach

### Strategies

- **Machine Learning Strategies**: The portfolios, PAE and PAE.CORE, use predictions generated daily to make trades. The models are retrained daily and hyperparameters are retuned at least monthly or in response to significant corporate actions. While both strategies use the same predictions, PAE.CORE is more risk-averse, aiming for reduced volatility compared to PAE.
- **Rules-Based Strategy**: The PAE.ROTA portfolio follows predefined rules and thresholds, offering a contrast to ML-driven strategies.

### Execution

- Trades are made only on the 150-200 highest market cap stocks from the S&P 500, selected for their significant market influence and stability.
- All portfolios operate without leverage, using exclusively long positions.

## Explore the Work

- **[Predictions](/predictions)**: Find predictions for stocks expected to make significant moves in the next 10 trading days, updated daily before the US market opens.
- **[Portfolios](/portfolios)**: Discover the composition of each portfolio, updated daily at close of US market.
- **[Performance](/performance)**: View the cumulative performance of the portfolios against the S&P 500 TR, updated daily at close of US market.
- **[Sign Up](/signup)**: Subscribe to the mailing list for future updates.

## A Note to Visitors

All trades are conducted in a simulated environment allowing for realistic trade execution and portfolio management without financial risk.

Project Alpha's viability will be reevaluated annually. Your feedback is always appreciated.

**Thank you for visiting!**