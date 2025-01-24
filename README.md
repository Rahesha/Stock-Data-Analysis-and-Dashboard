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
Follow these simple steps to use this project:
* Clone the Repository

 Download or clone the repository to your local machine.
```git
git clone https://github.com/Rahesha/Stock-Data-Analysis-and-Dashboard
```
* Install the Required libraries
For this project,use the command pip install provided above to install the needed python libraries.
* Run the Notebook:
Open the python script or Jupyter notebook in your preferred environment and execute the code step by step.
* View the Visualizations:
Explore the graphs for Tesla and GameStop, displaying trends in stock prices and revenue over time.

### Functionality
 #### Graphing Function
A core feature of this project is the reusable make_graph function, which creates visualizations for stock price and revenue data.
Functions Inputs:
* Stock DataFrame ( Date, Close)
* Revenue DataFrame (Date, Revenue)
* Stock Name
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
stock_data = yf.Ticker("TSLA")
tesla_data = stock_data.history(period="max").reset_index()
```
#### Step 2: Scrape Revenue Data
Use web scraping to collect Tesla's revenue information with BeautifulSoup:
```python
from bs4 import BeautifulSoup
import requests

url = "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/revenue.htm"
html_data = request.get(url).text
```
Parse the html data using beautifulSoup using parser- 'html.parser':
```python
soup = BeautifulSoup(html_data, "html_parser")
```
#### Step 3: Visualize Data
Plot Tesla's stock price and revenue trends using make_graph.
 ### GameStop Data Analysis
 #### Step 1: Extract Stock Data
 Retrieve GameStop's historical stock data:
 ```python
game_stock = yf.Ticker("GME")
gme_data = game_stock.history(period="max").reset_index()
```
#### Step 2: Scrape Revenue data
Use web scraping to gather GameStop's revenue details:
```python
url = "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/stock.html"
html_data2 = requests.get(url).text
```
Parse the html data using BeautifulSoup using parser 'html.parser':
```python
soup = BeautifulSoup(html_data2,"html.parser")
```
#### Step 3: Visualize Data
Plot GameStop's stock price and revenue trends using make_graphs.

### Author
Joseph Santarcangelo, PhD in Electrical Engineering, specializes in machine learning, signal processing, and computer vision. Dr. Santarcangelo is currently affiliated with IBM.

### License
This project is © IBM Corporation 2020. All rights reserved.
