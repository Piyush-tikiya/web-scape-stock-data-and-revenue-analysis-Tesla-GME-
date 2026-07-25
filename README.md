# 📈 ***Stock Data Web Scraping and Analysis (Tesla | GME)***

## 📌 Project Overview

As a **Data Scientist** working for a startup investment firm, my objective was to help investors make informed investment decisions by collecting financial information from multiple data sources.

This project extracts:

- 📊 Historical Stock Prices using **Yahoo Finance API (yfinance)**
- 🌐 Quarterly Revenue using **Web Scraping (BeautifulSoup)**
- 🧹 Cleans and prepares the data for analysis
- 📈 Visualizes stock price and revenue trends to identify business growth patterns

The project demonstrates real-world data collection, web scraping, data cleaning, and visualization skills frequently used by Data Analysts and Data Scientists.

---

# 🎯 Business Problem

Investment firms rely on multiple data sources to evaluate a company's financial performance.

The goal of this project is to:

- Extract historical stock price data
- Extract quarterly revenue data
- Compare revenue growth with stock price movements
- Visualize both datasets together
- Help identify trends that may influence investment decisions

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Requests
- BeautifulSoup (bs4)
- yFinance
- Matplotlib
- Jupyter Notebook

---

# 📂 Project Workflow

## Step 1 — Extract Tesla Stock Data

Historical Tesla stock prices are extracted using the **yfinance** library.

```python
Tesla = yf.Ticker("TSLA")
tesla_data = Tesla.history(period="max")
```

### Output

<img width="1780" height="701" alt="image" src="https://github.com/user-attachments/assets/4ecc5ba8-e73e-4320-994e-2ded1d10ea3a" />


---

## Step 2 — Extract Tesla Quarterly Revenue

Quarterly revenue is extracted from an HTML webpage using:

- Requests
- BeautifulSoup
- Pandas

```python
response = requests.get(url)
soup = BeautifulSoup(response.text, "lxml")
```

Revenue tables are then converted into a Pandas DataFrame.

### Output

<img width="1672" height="747" alt="image" src="https://github.com/user-attachments/assets/a6513c91-a0ec-4961-bfa4-c4d7ed7b75ea" />


---

## Step 3 — Extract GameStop (GME) Stock Data

Historical stock data is collected using Yahoo Finance.

```python
gme = yf.Ticker("GME")
gme_data = gme.history(period="max")
```

### Output

<img width="1811" height="381" alt="image" src="https://github.com/user-attachments/assets/b66a7a17-0bda-4138-b9ca-f40a7e82e5a7" />


---

## Step 4 — Web Scrape GameStop Revenue

The quarterly revenue table is extracted from HTML using BeautifulSoup.

```python
table_rows = soup.select("tbody tr")
```

The extracted values are stored in a DataFrame.

### Output
<img width="1521" height="667" alt="image" src="https://github.com/user-attachments/assets/747a0226-468c-4cc0-823e-fee70d9cadf6" />


---

## Step 5 — Tesla Dashboard

Both datasets are visualized together.

The dashboard compares:

- Historical Share Price
- Quarterly Revenue

This helps identify whether revenue growth aligns with stock price performance.

### Dashboard

<img width="1105" height="702" alt="image" src="https://github.com/user-attachments/assets/56ce38bc-e2b5-497e-8531-7f6a8946bb48" />

---

## Step 6 — GameStop Dashboard

A similar dashboard is created for GameStop.

### Dashboard

<img width="1052" height="732" alt="image" src="https://github.com/user-attachments/assets/9693408a-58f2-43aa-9065-f73c4abe159a" />


---

# 📊 Key Insights

### Tesla

- Consistent revenue growth over the years.
- Significant increase in stock price beginning around 2020.
- Revenue growth generally aligns with long-term market valuation.

### GameStop

- Revenue remained relatively stable before declining in later years.
- Stock price experienced extreme volatility during the 2021 meme stock event.
- Demonstrates that stock prices may not always reflect company fundamentals.

---

# 📁 Project Structure

```
Stock-Data-Web-Scraping-and-Analysis/
│
├── images/
│   ├── Q1.png
│   ├── Q2.png
│   ├── Q3.png
│   ├── Q4.png
│   ├── Q5.png
│   └── Q6.png
│
├── Stock_Data_Web_Scraping_and_Analysis.ipynb
├── README.md
└── requirements.txt
```

---

# 🚀 Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Stock-Data-Web-Scraping-and-Analysis.git
```

Move into the project directory

```bash
cd Stock-Data-Web-Scraping-and-Analysis
```

Install dependencies

```bash
pip install pandas
pip install requests
pip install beautifulsoup4
pip install matplotlib
pip install yfinance
pip install lxml
```

or

```bash
pip install -r requirements.txt
```

---

# ▶️ Run the Project

Launch Jupyter Notebook

```bash
jupyter notebook
```

Open

```
Stock_Data_Web_Scraping_and_Analysis.ipynb
```

Run all cells.

---

# 📚 Skills Demonstrated

- Financial Data Analysis
- Web Scraping
- API Data Extraction
- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Visualization
- Python Programming
- Business Intelligence

---

# 📈 Libraries Used

| Library | Purpose |
|----------|---------|
| yfinance | Download stock price data |
| Requests | HTTP requests |
| BeautifulSoup | HTML parsing |
| Pandas | Data manipulation |
| Matplotlib | Visualization |
| lxml | HTML parser |

---

# 📖 Learning Outcomes

Through this project, I learned how to:

- Extract live financial data using APIs.
- Scrape structured financial information from websites.
- Clean and transform raw datasets.
- Merge information from multiple sources.
- Build analytical dashboards.
- Interpret financial trends using data visualization.

---

# 👨‍💻 Author

## **Piyush Tikiya**

**Business Analyst**

---
⭐ **If you found this project helpful, consider giving it a Star!**
