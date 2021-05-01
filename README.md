# Overview
Analyze whether the daily bar and the first minute bar of the day match.

# Description
* Targeting stocks listed on the Tokyo Stock Exchange (more than 4,000 companies)
  * Download the stock list from https://www.jpx.co.jp/markets/statistics-equities/misc/01.html and save it as tickers.csv. At this time, the column name of the brand code is ticker.
* Obtains the daily and minute (5 minute by default) stock prices for the specified number of days from Yahoo and analyzes whether the daily and the first minute of the day match. The result is output to result.csv. Each column of result.csv is as follows
  * match_rate: Percentage of matching directions
  * match_count: Number of matches in the same direction
  * whole_count: number of daily bars
  * average_volume: Average volume (daily basis)
  * average_price: Average stock price (based on daily closing price)
* When acquiring stock prices from Yahoo, wait a certain number of seconds (5 seconds by default) before downloading the data of the next stock price so as not to overload the server. Therefore, it takes more than 6 hours to download all stocks.
* Output the acquired JSON to a file to reduce the chance of re-downloading (under the json_data directory)

# What is not done
* Analysis using local files (stored CSV files)

# How to open it on Google Colaboratory
Please take a look at [How-to-open-ipynb-on-Google-Colaboratory](https://github.com/shoji9x9/How-to-open-ipynb-on-Google-Colaboratory).

# Reference
* https://note.com/aiduudia/n/na9ea4f90e255
