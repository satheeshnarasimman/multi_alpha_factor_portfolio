# multi_alpha_factor_portfolio
In this project, a portfolio of 3 stocks are compared using alpha factors like momentum, growth and value. The tickers of interest here are Apple (AAPL), Microsoft(MSFT) and Amazon (AMZN).

## Libraries used
- numpy
- pandas
- pathlib
- datetime
- requests
- json
- dotenv
- technical analysis (ta)
- hvplot
- matplotlib

## Tools used
- Alphavantage API
- Windows 10 64-bit
- Google Sheets
- Github
- Gitbash
- Slack

## Data retrieval
- The stock price dating back to 2008 was downloaded from Google Sheets using the Google Finance function.
- The earnings data was pulled from Alphavantage using an API key. From the earnings data, the quarterly earnings is accessed.
- The balance sheets was also retrieved from Alphavantage. The metrics of interest here are Total Assets, Total Liabilities, Common Stock Shares Outstanding.

## Metrics calculated
### Momentum
- 20 day difference
- 20 day shift
- Momentum
- Z score

### Growth
- Percentage change of Earnings Per Share

### Value
- Book value= (Total Assets- Total Liabilities)/ Common Stock Shares Outstanding
- Average closing price in a quarter
- Price to Book ratio= Price/ Book Value

## Graphs plotted
- The momentum graphs of all 3 tickers 'AAPL', 'MSFT', 'AMZN'
- The percentage change of Earnings Per Share of all 3 tickers
- Price to Book (P/B) ratio of the 3 tickers.

## Interpretation
- From the momentum plot, the momentum of 'AAPL', 'MSFT' and 'AMZN' respectively has experienced a considerable swing from 2008- 2020, indicating that the tech stocks are very volatile.
- From the growth plot, 'AAPL' had a massive rise in 2003 before dropping and has stayed relatively flat since Q1 2004.
- 'MSFT' saw a big uptrend in 2007 and 2009, whereas 'AMZN' hit a 500 percent growth in 2002 and 2005. 
- In Q4 2013, 'AMZN' dipped to -500 percent growth.

## Conclusion
- From the factors calculated, it is not sufficient to reach a conclusive decision on whether the above stocks are a good investment. There are other parameters that need to be measured in order to reach an objective decision.

## Challenges
- The Book Value data is only available quarterly, while the closing price is available daily. 
- To calcualte the Price/Book value, the business days between a given range of dates had to be generated. The book value at the end of a particular quarter had to be forward filled for the next quarter.
- After forward filling the book value, it is concatenated with the closing price

## If there was more time
- Based on the 3 alpha factors built, Standardization and Winsorization wouled have been calculated.
- In addition, factor weighing, how much each ticker would contribute to the overall portfolio would have been performed.

## Contributors
- Satheesh Narasimman, helped along by my mentor, Fatemeh Arbab.

## References
- https://www.alphavantage.co/documentation/

- https://www.investopedia.com/terms/p/price-to-bookratio.asp

- https://www.statisticshowto.com/probability-and-statistics/z-score/

- https://www.investopedia.com/ask/answers/010915/what-considered-good-price-book-ratio.asp
