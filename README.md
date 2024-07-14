# Gas Price Automated Scraper
A simple automated web scraper using BeautifulSoup to find gas prices near a given postal code.

---

## Project Overview
This project is just a simple automated scraper that takes a postal code (US or Canada) and a fuel type (Regular, Midgrade, Premium, Diesel) and returns the most recent gas prices in the area. Data is scraped from [GasBuddy](https://www.gasbuddy.com/). This tool can be used to compare gas prices in a certain area and monitor trends in gas prices over time.

The tool extracts the following data for up to 20 gas stations near to the given postal code in a .csv file:
- Brand of gas station
- Price
- Address of gas station
- Date
- Country (US or Canada)

## Usage
To use, first download the Jupyter notebook [here](https://github.com/jamesinjune/Gas_Price_Automated_Scraper/blob/main/Automated_Scraper_Gasbuddy.ipynb).
There are four fields that need to be manually entered:
- `postal`: Postal code in any standard US or CA postal code format
- `fuel`: Strings of digits 1-4, corresponding to: 1) Regular, 2) Midgrade, 3) Premium, 4) Diesel
- `headers`: A unique User-Agent Header that can be retrieved at https://httpbin.org/get. Copy the line that starts with <"User-Agent": ...>
- `path`: File directory for where to store scraped data
Then, run the cell with the user-variables and functions. The data will be scraped every 24 hours, or after any other specified time length if changed.

## Example Data
Below is three months of data for gas stations near the University of British Columbia in Vancouver for regular fuel:

![Gas prices and average for V6T 1Z4, regular fuel](https://github.com/jamesinjune/Gas_Price_Automated_Scraper/blob/main/gas_prices_sample_lineplot.png)
