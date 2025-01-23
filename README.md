## Stock Data Analysis and Dashboard
### Description
This project demonstrates extracting stock data and visualizing it using Python. It enables users to analyze historical trends 
in data for companies like Tesla and GameStop. The project uses yfinance for extracting stock data and webscraping using beautifulsoup and pandas.
### Features
Extract historical stock data using yfinance
Webscrape revenue data for Tesla and Gamestop
Visualize stock price and revenue trends with plotly
### Installation
Before running the project , ensure the following llibraried are installed.
``` python
!pip install yfinance
!pip install bs4
!pip install pandas plotly
```
In Python, we can ignore warnings using the warnings module.

```python
import warnings
warnings.filterwarnings("ignore", category=FutureWarning)
```
### Usage

### Functionality
 #### Graphing Function
A core feature of this project is the reusable make_graph function, which creates visualizations for stock price and revenue data.
Functions Inputs:
Stock DataFrame ( Date, Close)
Revenue DataFrame (Date, Revenue)
Stock Name
```python
make_graph(tesla_data, tesla_revenue, "Tesla")
make_graph(gme_data, gme_revenue, "GameStop")
```
### Workflow
 ### Tesla Data Analysis
#### Step 1: Extract Stock Data
Retrieve Tesla's historical stock data using yfinance:
```python
      import yfinance as yf
      tesla_data = yf.Ticker("TSLA").history(period="max").reset_index()
```
#### Step 2: Scrape Revenue Data
Use web scraping to collect Tesla's revenue information with BeautifulSoup:
```python
from bs4 import BeautifulSoup
import requests

url = "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/revenue.htm"
html_data = request.get(url).text
```
#### Step 3: Visualize Data
Plot Tesla's stock price and revenue trends using make_graph.



 
