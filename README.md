# 📈 Stock Alert Automation using UiPath

This project uses Robotic Process Automation (RPA) built with UiPath to monitor stock prices from Yahoo Finance and send email alerts when prices cross user-defined thresholds.

## 🚀 Features
- Reads stock list from Excel
- Scrapes current stock prices from Yahoo Finance
- Compares with user-defined thresholds
- Sends email alert if stock price is above/below limits

## 📂 Files Included
- `Main.xaml` – Main UiPath workflow
- `StockList.xlsx` – Excel sheet with stock names, URLs, and thresholds
- `project.json` – UiPath project config

## 🛠️ Tools Used
- UiPath Studio
- Excel Activities
- Web Scraping (Browser Automation)
- SMTP Mail

## 📬 Sample Alert
Hello,
The stock ICICIBANK has crossed your alert threshold.
Current Price: ₹1447.7
Status: Above Threshold
Regards,
Stock Monitor Bot
