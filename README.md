# Macroeconomic Investor Dashboard

## Overview
This notebook will generate 20 years of data for 20 different classical recession indicators using FRED and Yahoo Finance data/APIs. These could be used to hedge upcoming downturns in a long portfolio, but should not be used for financial advice. Use this information at your own risk.

## Goals of this Project
1. Provide the common investor with insights to market internals
2. Make it easy and convinient to access and understand
3. Use public data that will always be avaliable
4. Allow for adjustments to be made to the time frame viewed

## Function Explanations

#### ``def plot_figure(ax, data, label, title, start_date, end_date, fred, ylabel="", plotRecessions=1, legend_loc='upper left')``
- Helps the main function plot multiple figures on a plot
- Cleans up the main for higher readability

#### ``def create_investor_dashboard(start_date, end_date=datetime.today())``
- Downloads all of the stock and financial data from yfinance and FRED APIs at the specified start date to the specified end date
- Calculates the ratios, inversions and YoY percentages for all 20 indicators
- Plots the figures and prints a copy to a PNG for easy sharing in your Google Drive

## How to use this project in Google Colab
1. Connect to a Runtime
2. Press ``Ctrl + F9``

## Example Quick Start Main
``` Python
# Call the function with a start date
today = datetime.today()
start_date = today - timedelta(days=365 * 20)
start_date = start_date.strftime("%Y-%m-%d")
create_investor_dashboard(start_date)
```

## Example Output - PNG
![image](https://user-images.githubusercontent.com/84938803/222829358-45d4cfca-ffc1-4909-9c79-3666d767237d.png)

## Libraries Used
- [YFinance](https://github.com/ranaroussi/yfinance)
- [Pandas](https://github.com/pandas-dev/pandas)
- [MatPlotLib](https://github.com/matplotlib/matplotlib)
- [FredAPI](https://github.com/mortada/fredapi)
