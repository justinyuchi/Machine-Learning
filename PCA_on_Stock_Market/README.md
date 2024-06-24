
# Principal Component Analysis (PCA) on Stock Market

## Executive Summary

This project demonstrates the application of Principal Component Analysis (PCA) to stock market data. The analysis showcases how to leverage PCA to identify major risks and factors influencing asset returns, reconstruct component portfolios, and backtest the suggested portfolios. This study focuses on the first principal component, with similar procedures applicable to the second and third components.

![PCA](images/pca_overview.png)

## Outline

1. **Introduction to PCA on Asset Returns**
2. **Exploratory Data Analysis (EDA)**
3. **Applying PCA to Stock Returns**
4. **Reconstructing Component Portfolios**
5. **Constructing Portfolios through PCA Filtering**
6. **Backtesting PCA-Suggested Portfolios**
7. **Discussion and Limitations**

## Introduction

In this study, Principal Component Analysis (PCA) is directly applied to stock return series without first calculating the covariance matrix. Although this approach may introduce some noise, it allows PCA to capture the temporal information inherent in the data, unlike the traditional method that relies on the covariance matrix and only provides static information. Further improvements and variations of PCA are discussed in the "Discussion and Limitations" section.

## Exploratory Data Analysis (EDA)

Initial data analysis is conducted to understand the structure and characteristics of the stock market data.

![Daily Returns of Stocks](images/stocks_returns.png)
![Correlation Heatmap](images/correlation_heatmap.png)

## Applying PCA to Stock Returns

PCA is applied to the stock returns data to extract the principal components and analyze how much variance each component explains.

![PCA Components](images/pca_components.png)

## Reconstructing Component Portfolios

Based on the PCA loadings, portfolios aligned with the extracted components are reconstructed. This step involves understanding the economic significance of the PCA weights.

![Component Portfolio](images/component_portfolio.png)

## Constructing Portfolios through PCA Filtering

Using PCA weights, portfolios that are least sensitive or even negatively correlated to the primary principal component are constructed.

![PCA Filtering](images/pca_filtering.png)

## Backtesting PCA-Suggested Portfolios

To avoid look-ahead bias, information from the previous period is used to construct the portfolio. In this study, data prior to 2022-01-01 is used to construct the PCA-suggested portfolios, and data post-2022-01-01 is used to backtest the strategy.

### Backtesting: Portfolio with 10 Highest First Component Factor Loadings

![Backtesting: Equally Weighted Portfolio with Stocks with 10 Highest First Component Factor Loadings](images/backtesting_highest_10_factor_loading.png)

### Backtesting: Portfolio with 10 Lowest First Component Factor Loadings

![Backtesting: Equally Weighted Portfolio with Stocks with 10 Lowest First Component Factor Loadings](images/backtesting_lowest_10_factor_loading.png)

## Discussion and Limitations

A detailed discussion on the findings, potential limitations, and areas for future research is provided. Different PCA methods suitable for financial data analysis are also explored.

## Conclusion

This project showcases the application of PCA in financial markets, providing valuable insights into risk management and portfolio construction.

## Contact

For any queries or further discussions, feel free to reach out to me at [juhsu@ucsd.edu](mailto:juhsu@ucsd.edu).
