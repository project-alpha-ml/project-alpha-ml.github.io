---
layout: default
---
## About

Project Alpha explores active investing in the U.S. stock market using machine learning and rule-based strategies. The project aims to devise profitable strategies by extracting patterns from an extensive dataset, comprising price data, news data, fundamental data, corporate actions, and macroeconomic data. All data are sourced from publicly available, free APIs.

## Approach

### Strategies

- **Machine Learning Strategies**: The portfolios, PAE and PAE.CORE, use predictions generated daily to make trades. The models are retrained daily and hyperparameters are retuned at least monthly or in response to significant corporate actions. While both strategies use the same predictions, PAE.CORE is more risk-averse, aiming for reduced volatility compared to PAE.
- **Rule-Based Strategy**: The PAE.ROTA portfolio follows predefined rules and thresholds based on a subset of engineered features, serving as an alternative to the machine learning strategies.

### Execution

- Orders are submitted daily during regular U.S. market trading hours.
- The universe of stocks to choose from contains only the 150-200 highest market cap stocks from the S&P 500, selected for their significant market influence and stability.
- All portfolios trade without leverage, using exclusively long positions.
- All portfolios begin with $100,000. No additional funds will be added beyond the initial investment.

## Explore the Site

- **[Predictions](/predictions)**: Find predictions for stocks expected to make significant moves in the next 10 trading days, updated daily before the start of regular U.S. market trading hours.
- **[Portfolios](/portfolios)**: View the composition and transaction history of each portfolio, updated hourly during regular U.S. market trading hours.
- **[Performance](/performance)**: View the cumulative performance of each portfolio against the [S&P 500 TR](https://www.google.com/finance/quote/SP500TR:INDEXSP), updated hourly during regular U.S. market trading hours.
- **[Feedback](/feedback)**: Please share your thoughts here. Your suggestions for improvements are welcome.

## A Note to Visitors

- The [strategies](#strategies) are not expected to be [market neutral](https://www.investopedia.com/terms/m/marketneutral.asp). Consequently, due to the [execution](#execution) of these strategies, daily portfolio returns are expected to exhibit a moderate degree of correlation with each other and with the S&P 500 index.
- All trades are conducted in a simulated environment allowing for realistic trade executions and portfolio management without financial risk.

Project Alpha's viability will be reevaluated annually. Your [feedback](/feedback) is appreciated.

**Thank you for visiting!**