# **Stock fundamental analysis**
Per fundamental analysis model, in order to calculate intrinsic value of a stock, we need to bring in all necessary financial data.  
The program gets price from yfinance package, other financial data from [FundamentalAnalysis package](https://pypi.org/project/fundamentalanalysis).  
Charts by plotly (graph_objects) show data in visual form.

<img src="./images/AAPL%20price%20chart.png" width="700" />

Then stock's fundamental financial data is collected through fundamentalanalysis package.
<img src="./images/AAPL%20fundamental%20growth%20chart.png" width="700" />

Finally CAGR (Compound Annual Growth Rate) of Price/Revenue/EPS/freeCashFlow are calculated and shown in chart.
<img src="./images/AAPL%20Compound%20Annual%20Growth%20Rate.png" width="700" />

Then results are exported to excel spreadsheet with proper format.

## Improvement on second commit:  update_per_growth()
FundamentalAnalysis package is using Financial Modeling Prep API, which only provide 5 years data of Revenue/EPS/freeCashFlow. Monthly subscription is needed for all years data.  
I noticed that free subscription also provides all years data for growth of Revenue/EPS/freeCashFlow, so all years data of Revenue/EPS/freeCashFlow can be calculated based on growth data, and CAGR can be calculated accordingly.  
New function update_per_growth() is added to fulfill above requirement.

2023-06-16 Latest update on Financial Modeling Prep API: Free subscription no longer proivde growth data beyond 5 years. update_per_growth() is obselete now.

## How to start with the project
Just download .ipynb file, run over jupyter notebook or other python IDE, enter stock ticker and start/end date, results will be generated as excel file.
Intrinsic value calculation locates on lower portion of excel page, need to be adjusted manually. Key inputs will be future 10 years growth rate and fair year 1 free cash flow. Financial data only provides background information, finally inputs are solely depends on user's investment experiences.  
Example: "Stock fundamental analysis - BRK-B 2023-05.xlsx"
