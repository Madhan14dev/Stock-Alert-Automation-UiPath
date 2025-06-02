# 📘 README: Automated Stock Price Monitor Bot (UiPath)

## 📌 Project Overview

This project is a **UiPath automation bot** that reads a list of stock symbols and their threshold prices from an Excel file, fetches their current prices from Yahoo Finance using browser automation, compares the prices to thresholds, updates the Excel file, and sends alert emails when thresholds are crossed.

---

## 🛠️ Technologies Used

* **UiPath Studio**
* **UiPath.Excel.Activities**
* **UiPath.Mail.Activities**
* **UiPath.UIAutomation.Activities**
* **Yahoo Finance (for stock price data)**

---

## 📂 Project Structure

```
StockMonitorBot/
│
├── Main.xaml                  # Main workflow
├── StockList.xlsx             # Input stock list with thresholds
├── project.json               # UiPath project config
└── README.md                  # Project instructions
```

---

## 🔧 Instructions Note

### 📅 Step 1: Open Project in UiPath Studio

1. Open **UiPath Studio**.
2. Click **Open Project** → Locate and open `project.json`.

### 📦 Step 2: Install Missing Dependencies

> Required Packages:

* UiPath.Excel.Activities
* UiPath.Mail.Activities
* UiPath.System.Activities
* UiPath.UIAutomation.Activities

✅ Go to **Manage Packages** → Install from **Official Feed** → Save.

### 📧 Step 3: Configure Email Credentials

* Navigate to `Send SMTP Mail Message` activity in **Main.xaml**.
* Enter your email, password, SMTP server, and port.

For Gmail:

* Generate an App Password via [https://myaccount.google.com/apppasswords](https://myaccount.google.com/apppasswords)
* Use `smtp.gmail.com` and port `587`, with `StartTls` enabled.

### 📊 Step 4: Edit Excel File `StockList.xlsx`

| Stock Name | URL                                                                                | Upper Threshold | Lower Threshold |
| ---------- | ---------------------------------------------------------------------------------- | --------------- | --------------- |
| INFY       | [https://finance.yahoo.com/quote/INFY.NS](https://finance.yahoo.com/quote/INFY.NS) | 1600            | 1400            |
| ...        | ...                                                                                | ...             | ...             |

* ✅ Do not change column headers.
* ✅ Add or remove rows as required.

### ▶️ Step 5: Run the Bot

1. Close Excel before running.
2. Hit **Run** in UiPath Studio.
3. Bot will:

   * Read stock list
   * Open browser to fetch prices
   * Compare values
   * Update Excel with status
   * Send email alerts if above or below threshold

---

## 📤 Sample Email Alert

```
Subject: Stock Price Alert

Alert for INFY:
Current Price: ₹1650
Status: ABOVE threshold (1600)
```

---

## ✅ Output

**Excel file updated with current stock prices and status**

| Stock Name | URL | Upper Threshold | Lower Threshold | Current Price | Status          |
| ---------- | --- | --------------- | --------------- | ------------- | --------------- |
| INFY       | ... | 1600            | 1400            | 1650          | Above Threshold |

---

Happy Automating! 🤖
