Financial Statement Data Preparation – TCS
📊 Project Overview

This project focuses on cleaning, analyzing, and visualizing the financial performance of Tata Consultancy Services (TCS) over a 10-year period (FY2016–FY2025).
The goal is to evaluate company financial health using key metrics such as Revenue Growth, Profit Trends, Debt-to-Equity Ratio, and Asset–Liability structure.

🎯 Objectives

Prepare and clean financial statement data from raw CSV inputs.

Compute essential financial ratios and KPIs.

Analyze trends in revenue, profitability, and leverage.

Visualize insights through charts and dashboards for investor decision-making.

🧾 Dataset Description

File Name: TCS_Financial_Data_2016_2025.csv

Column Name	Description
Year	Financial Year (ending March)
Revenue	Total Revenue (₹ crore)
ProfitAfterTax	Net Profit After Tax (₹ crore)
TotalAssets	Total Assets (₹ crore)
TotalLiabilities	Total Liabilities (₹ crore)
DebtToEquityRatio	Ratio of Liabilities to Shareholders’ Equity
RevenueGrowthPercent	Year-on-year growth in Revenue (%)
⚙️ Tools & Technologies

Python (pandas, numpy, matplotlib)

Excel / Google Sheets

Power BI / Tableau (optional for dashboard visualization)

🧮 Sample Python Workflow
import pandas as pd
import matplotlib.pyplot as plt

# Load CSV
df = pd.read_csv("TCS_Financial_Data_2016_2025.csv")

# Basic Cleaning
df.dropna(inplace=True)
df['RevenueGrowthPercent'] = df['Revenue'].pct_change() * 100

# Visualization
plt.figure(figsize=(10,5))
plt.plot(df['Year'], df['Revenue'], marker='o', label='Revenue')
plt.plot(df['Year'], df['ProfitAfterTax'], marker='s', label='Profit After Tax')
plt.title('TCS Financial Growth (2016–2025)')
plt.xlabel('Year')
plt.ylabel('₹ Crore')
plt.legend()
plt.grid(True)
plt.show()

📈 KPIs to Analyze

Revenue Growth (%) = (Current Year Revenue – Previous Year Revenue) / Previous Year × 100

Debt-to-Equity Ratio = Total Liabilities / (Total Assets – Total Liabilities)

Profit Margin (%) = Profit After Tax / Revenue × 100

Return on Assets (ROA) = Profit After Tax / Total Assets × 100

📅 Future Enhancements

Automate data fetching from company reports (web scraping).

Build a Power BI dashboard for investor insights.

Compare TCS with peers like Infosys, Wipro, and HCL Tech.

👩‍💻 Author

Divya Drishti
Student Project – Financial Statement Data Preparation using Python & CSV
Theme: Corporate Finance / Fundamental Analysis