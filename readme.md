

---

# Binance Automation Tool (Selenium)

A Python-based automation toolkit built with Selenium, designed for interacting with the Binance exchange.
This project provides tools for **market data scraping**, **automated trading interactions**, and **debug visualization**.

---

## 🚀 Features

### 📊 Multi-Symbol Market Query

* Supports querying multiple trading pairs at once (e.g. `BTC BNB ETH`)
* Automatically appends default quote asset (`USDT`)
* Accepts custom pairs (e.g. `ETH/BTC`)

### 📈 Advanced Market Data Extraction

* Real-time price
* 24h price change (%)
* Market cap ranking (Rank)
* Dominance Index

### 🤖 Automated Trading Actions

* Simulates continuous buy/sell actions
* Supports market orders via UI interaction
* User-controlled parameters:

  * Trading pair
  * Order type (Buy/Sell)
  * Number of executions
  * Total amount per trade

### 🔍 Debug Mode (Developer-Friendly)

* Step-by-step data extraction logs
* Displays intermediate dictionaries and processing flow
* Useful for debugging selectors and data parsing logic

### 📑 Smart Result Sorting

* Automatically sorts queried results by **market cap rank**

---

## 🛠️ Requirements

* Python 3.x
* Google Chrome
* ChromeDriver (must match your Chrome version)

### Install dependencies:

```bash
pip install selenium
```

---

## 📖 Usage Guide

### 1. Market Data Query

Run the script and input symbols:

```
BTC
ETH/BTC
BNB SOL DOGE
```

#### Notes:

* Default quote asset: `USDT`
* Browser will **maximize automatically** for accurate element detection
* Do NOT resize or minimize during execution

---

### 2. Automated Trading

⚠️ Requires manual login

#### Steps:

1. Run the script → opens Binance trading page
2. Manually complete:

   * Login
   * 2FA / security verification
3. Enter parameters in terminal:

   * Trading pair (e.g. `BNB/USDT`)
   * Buy or Sell
   * Number of repetitions
   * Total amount per trade

The bot will:

* Locate input fields
* Simulate clicks
* Execute trades continuously

---

### 3. Debug Mode

Use the debug version to:

* Print each step’s data
* Inspect parsed results
* Trace logic issues

Ideal for:

* Developers modifying selectors
* Handling UI changes

---

## ⚠️ Disclaimer

### Legal & Risk Notice

This project is for **educational and research purposes only**.
It does **NOT** constitute financial or investment advice.

Automated trading involves **significant financial risk**.
Always test in:

* Small amounts
* Demo environments

---

## ⚠️ Important Notes

### 1. UI Dependency

Selenium relies on:

* `CLASS_NAME`
* `CSS_SELECTOR`

If Binance updates its UI, selectors may break.
You must manually update them.

---

### 2. Timing Issues

The script uses:

```python
time.sleep(0.15)
```

If you experience instability:

* Increase delay based on network speed

---

## 💡 Suggested Improvements (Optional)

* Replace `time.sleep()` with `WebDriverWait` (more stable)
* Add exception handling for failed element lookup
* Support headless mode
* Integrate Binance API for hybrid approach (faster + safer)

---


