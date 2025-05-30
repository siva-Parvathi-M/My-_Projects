 * # Project - 1 *

Here’s a professional `README.md` file tailored for your **Sales Forecasting Dashboard (Power BI + Excel)** project — perfect for showcasing on GitHub:

---

````markdown
#  Sales Forecasting Dashboard (Power BI + Excel)

This project demonstrates the analysis and visualization of 3 years of historical sales data (2015–2018) using **Power BI Desktop**. It includes trend analysis, interactive reporting, and sales forecasting using DAX expressions.

---

##  Project Objectives

- Analyze 3 years of historical sales data to identify trends and seasonality
- Forecast future sales using DAX (3-month moving average)
- Build an interactive dashboard with slicers for year, category, and region
- Enable monthly report refresh using Excel as a data source

---

##  Tools Used

- **Power BI Desktop (Free Version)**
- **Microsoft Excel (as data source)**
- **DAX (Data Analysis Expressions)** for calculated columns and forecasting
- **Power Query** for basic transformations

---

##  Data Overview

The dataset contains the following fields:

- `OrderDate` — Sales transaction date
- `Sales` — Sales revenue amount
- `Product` — Product name
- `Category` — Product category
- `Region` — Sales region
- *(No Profit or Quantity fields used)*

---

## Steps Performed

### 1. **Data Preparation**
- Created a sales dataset covering the period **2015–2018** using Excel
- Cleaned the dataset and ensured correct data types (e.g., date format)

### 2. **Data Import in Power BI**
- Loaded Excel data into Power BI using **Get Data → Excel**
- Applied basic transformations using **Power Query**

### 3. **Created a Date Table**
- Generated a `DateTable` using DAX:
  ```DAX
  DateTable = CALENDAR(MIN(Sales_Data[OrderDate]), MAX(Sales_Data[OrderDate]))
````

* Added columns: Year, Month, Quarter

### 4. **Data Modeling**

* Created relationships between `DateTable` and `Sales_Data[OrderDate]`
* Verified correct data model with star schema

### 5. **Forecasting Using DAX**

* Created a DAX measure for 3-month moving average forecast:

  ```DAX
  Sales Forecast = 
  AVERAGEX(
      DATESINPERIOD('DateTable'[Date], MAX('DateTable'[Date]), -3, MONTH),
      CALCULATE(SUM('Sales_Data'[Sales]))
  )
  ```

### 6. **Built the Dashboard**

* Key visuals included:

  * Line chart for actual vs forecasted sales
  * Sales by Category (Clustered Column Chart)
  * Sales by Region (TreeMap)
  * Monthly Sales Trend (Line Chart)
  * KPI Cards (Total Sales, Average Sale, Max Sale, Order Count)
* Added **slicers** for:

  * Date Range
  * Year
  * Category
  * Region

### 7. **Refresh & Export**

* Simulated monthly report automation:

  * Excel file updated with new data
  * Refresh button in Power BI updates all visuals and calculations
  * Exported reports as **PDF** for distribution

---

## Dashboard Snapshot

> *(Insert a screenshot of your dashboard here)*
> Save a screenshot as `dashboard.png` and link it:
> `![Dashboard Preview](dashboard.png)`

---

##  Folder Structure

```
Sales-Forecasting-Dashboard/
├── sales_data.xlsx               # Source dataset (2015–2018)
├── SalesForecast.pbix            # Power BI dashboard file
├── dashboard.png                 # Screenshot of dashboard
└── README.md                     # Project documentation




# Project - 2

# Machine Uptime & Fault Trend Analysis in Tableau

## Project Overview

This project focuses on analyzing manufacturing machine performance using Tableau. By visualizing **machine uptime, downtime**, and **hourly fault trends**, we aim to uncover patterns that impact operational efficiency on the factory floor.

Using a dataset containing timestamped logs for multiple machines, the dashboard highlights when and how frequently machines are experiencing faults and how it affects their overall performance.

---

## Dataset Features

The dataset contains the following columns:

| Column Name     | Description                               |
|------------------|-------------------------------------------|
| `MachineID`      | Unique identifier for each machine         |
| `CycleTime`      | Time taken to complete one production cycle |
| `Temperature`    | Recorded machine temperature               |
| `Pressure`       | Pressure reading at a given time           |
| `Fault`          | 1 = Fault occurred, 0 = No fault           |
| `Timestamp`      | Date and time of the event recorded        |

---

## Key Visualizations

1. **Uptime vs Downtime per Machine per Day**  
   - Shows how long each machine was running vs. down on a daily basis.

2. **Hourly Fault Trend**  
   - Highlights the number of faults that occur during each hour of the day.

3. *(Optional additional insights can be added based on dataset)*

---

## Insights Derived

- Identification of machines with the highest fault rates.
- Pinpoint hours in the day with increased fault frequency.
- Overall machine efficiency trends across days and shifts.

---

## Tools Used

- **Tableau Public** – for interactive dashboard creation.
- **Microsoft Excel / CSV** – for source data formatting and preparation.

-------------------------------------------------------------------------------------------

# project - 4

# Data Workflow Automation using Python & GenAI

This project automates repetitive data cleaning tasks using Python and generates insightful business reports using Generative AI via Together.ai API. The dataset used is the Online Retail (2009-2010) Excel file.

# Project Overview

Goal: Automate the end-to-end data cleaning, transformation, and report generation process.

Key Components:

Automated data cleaning using pandas

Insight generation using Together.ai GenAI API

Exporting AI-generated insights to a well-formatted PDF report

# Project Structure

# data-workflow-python-genai
├── data/
│   └── Online Retail.xlsx
├── genai_report.pdf           # Final output report
├── requirements.txt           # Required Python libraries
├── DejaVuSans.ttf             # Unicode-compatible font for PDF
├── main.ipynb                 # Colab-compatible notebook
└── README.md

# Dataset

File: Online Retail.xlsx

Sheet used: 2009-2010

Sample columns:

InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country

# How It Works

Data Cleaning

Remove null values

Drop duplicates

Filter rows with invalid quantities or prices

Insight Generation using GenAI

Group data (e.g., top-selling products, monthly revenue)

Send summaries to Together.ai’s chat completion endpoint

Receive narrative insights back from the GenAI model

PDF Report Creation

Uses fpdf2 and DejaVuSans.ttf for full UTF-8 support

Structure:

Title

Section-wise narrative insights (from GenAI)

# API Key Setup

This project uses Together.ai API.

Set your API key inside the notebook like this:

api_key = "your_together_ai_api_key_here"

# Requirements

Install all required packages:

pip install pandas fpdf2 requests openpyxl

# Output

genai_report.pdf: Final report with cleaned data insights generated by GenAI

# Future Improvements

Schedule the notebook using Colab + Google Drive

Integrate with email to send PDF reports

Add real-time alert generation for anomalies

