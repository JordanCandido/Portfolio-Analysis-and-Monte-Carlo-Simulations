# Project 1: Portfolio Analysis, Simulations and Benchmark Comparison
## Motivation and Summary
### Spreadsheets are getting outdated and overrated with the addition of more efficient methods of analyzing data. Updating a spreadsheet with data even prior to performing analysis can take hours. However, in this bootcamp we have learned methods to more efficiently retrieve and analyze data using Python and Jupyter Lab. The purpose of this project is to develop a notebook that uses the power of portfolio and risk analysis spreadsheets into one servable dashboard that can be viewed by the user/client. 
### Question: 
#### 1. How do I create a dashboard for my stock and crypto portfolio? We asked this question because we learned in our bootcamp classes how to build a dashboard for real estate analysis and mapping data. In this assignment we saw the power of creating a dashboard and providing deliverable and servable information to clients and users.
#### 2. How does the inputted portfolio compare to a traditional 60/40 Stocks and Bonds Strategy and other benchmark indexes? We asked this question to provide information to the client/user on the most important aspect of portfolio management being risk analysis. We wanted the use of simulations and forecasted returns to show the risk structure of the portfolio compared to the market benchmarks. 
#### 3. What is the forecasted return? We asked this question to provide the actual numeric forecasted returns in dollar amount based on 1-year and 5-year projections. We wanted to provide the exact value of the expected return for the inputted portfolio. 
### In summary, we were successful in meeting our goals for the requirements of the project and included possible further work in the Postmortem below. We found that our selection of stocks being more growth oriented had shown a high-risk structure with a high beta compared to the benchmark indexes. As we suspected and as a result of the recent strength of growth stocks and assets, the portfolio has a much higher expected return compared to benchmarks. The volatility and growth potential of having a small percentage of the portfolio in crypto assets can also return larger than expected returns even when using low probability simulations. 
## Questions & Data
### Answer: 
#### 1. We used the Panel library to create a dashboard for our investment portfolio with tabs showing the deliverable and servable information for the client/user. The tabs include a Welcome description including this read.me file, the inputted portfolio, percentage allocations, expected returns and benchmark simulations and expected returns. The information is presented in the form of graphical plots and calculation statements based on data calculated in the simulations. 
#### 2. We used Monte Carlo Simulations to forecast potential expected returns. The benchmark indexes include the S&P 500 and the Nasdaq. Simulations were conducted for the stock portfolio, crypto portfolio, a 60/40 Stocks and Bonds portfolio and the benchmark indexes for a 1-year and 5-year timeframe. The forecasted returns shown in each simulation plot provide data on the average expected returns within 95% confidenc eof simulated outcomes. The calculations for average returns, minimums and maximums paint a picture that shows the difference in the risk structure of the portfolio compared to the benchmarks. 
#### 3. The Yahoo Finance API provides a constant connection of market data to the notebook. Using the data from the API in CSV format we were able to create our own dataframes that construct the inputted portfolio for the client/user. This means that the notebook can be run on a constant frequency to provide data and forecasts over any desired timeframe. The recommended timeframe is either monthly, quarterly or bi-yearly for adjustments of position sizes and portfolio management. 

## Data Cleanup & Exploration
### Data collection was completed with the use of The Yahoo Finance API or more specifically the y.finance library. Stock market information as collected using this library for each asset of stocks and cryptos into CSV format and readable in the notebook as a dataframe. The dataframe for stock market information was indexed for each ticker and spanned as far as the information is available or to a maximum of 10 years.
### Stocks: (10)
#### 1. QQQ (NASDAQ)
#### 2. CIBC
#### 3. MSFT
#### 4. ASUS
#### 5. TSLA
#### 6. PFE
#### 7. NVDA
#### 8. F
#### 9. CCL
#### 10. AC
### Crypto: (5)
#### 1. Bitcoin
#### 2. Ethereum
#### 3. Cardano
#### 4. Chainlink
#### 5. Litecoin
### We found that running a simulation for the complete portfolio of stocks and crypto was a little bit misleading and did not provide the full information of the risk structure. We then chose to make more sense of the data in the simulations by running separate simulations for each of the stocks and the cryptos. After doing this we were able to see the true effect of having a small allocation to cryptos in the portfolio to increase expected returns. Another issue we focused on was the limited amount of market data for cryptos which resulted in less accurate simulations compared to the stock simulations. We worked around this by using the crypto tickers in USD currency as there was more time data for these tickers and gave more historical data to work with. 

## Data Analysis
### The simulated average return for the stock portfolio over a 5-year period was 5x the original investment. The simulated average return for the crypto portfolio over a 5-year period was 89x the original investment. The simulated average return for the 60/40 Stocks and Bonds portfolio over a 5-year period was 1.5x the original investment or a 50% increase. The simulated average return for the Nasdaq index over a 5-year period was 2.7x the original investment. The results compiled here show that simply investing money into the benchmark indexes yields a much larger expected return over a 5-year period compared to the traditional 60/40 Stock and Bonds portfolio. Furthermore, for the investors that are willing to put in more work into picking individual stocks and look to outperform the market indexes returns by using growth stocks similar to the ones chosen in this project. The simulation do not factor in dividends and dividend growth and a separate calculations for expected returns would need to be done to consider the full expected return. For the simulations done on the shorter 1-year timeframe, the short-term risk that is shown by the simulations with negative returns or using the minimum value. These simulations show that the choice of growth stock in the inputted portfolio can offer larger than expected returns in both the long-term and the short term. Furthermore, with more volatile stocks and cryptos also come with the risk of lower than expected or negative returns in the short-term depending on market conditions. 

## Discussion
## The resulting analysis proves that the 60/40 Stocks and Bonds strategy is the most conservative form of investing. For people with a larger investment window of greater than 5-years, investing in market indexes seems to be the more common strategy in modern days and yields a much larger expected return with minimal increase in risk. For the people who are willing to do more than plow their money into one or two market indexes or ETF's, building a diversified investment portfolio of stocks spread across the various market sectors and with a small allocation of <10% can yield larger than expected returns. The creation of your own portfolio is at the very least the acceptance of the challenge of beating and out-performing the stock market and other hedge funds.

## Postmortem 
### - Selector for user interaction to modify analysis information.
### - Include columns in the portfolio table for current market value and a portfolio position weighting using the ATR of each asset. 
### - Input function for tickers, share amount and share price. 
### - Add an additional column for sector and provide a pie chart for sector allocation which shows the diversification of assets. 