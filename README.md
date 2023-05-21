# stock-analysis
There're two python program created in jupyter notebook: Stock fundamental analysis and S&P 500 investment pattern.

# First program - Stock fundamental analysis.ipynb
Per fundamental analysis model, in order to calculate intrinsic value of a stock, we need to bring in all necessary financial data. 
The program gets price from yfinance package, the rest of financial data from FundamentalAnalysis package (https://pypi.org/project/fundamentalanalysis). 
Finally most recent freeCashFlow and CAGR (Compound Annual Growth Rate) of Price/Revenue/EPS/freeCashFlow are collected and calculated. Then results are exported to excel spreadsheet with proper format.

## Improvement of second commit Stock fundamental analysis
FundamentalAnalysis package is using Financial Modeling Prep API, which only provide 5 years data of Revenue/EPS/freeCashFlow. Monthly subscription is needed for all years data.
I noticed that free subscription also provides all years data for growth of Revenue/EPS/freeCashFlow, so all years data of Revenue/EPS/freeCashFlow can be calculated based on growth data, and CAGR can be calculated accordingly.
New function update_per_growth is added to fulfill above requirement.

# How to start with the project
Just download .ipynb file, run over jupyter notebook or other python IDE, enter stock ticker and start/end date, results will be generated as excel file.
Intrinsic value calculation locates on lower portion of excel page, need to be adjusted manually. Key inputs will be future 10 years growth rate and fair year 1 free cash flow. Financial data only provides background information, finally inputs are solely depends on user's investment experiences.
