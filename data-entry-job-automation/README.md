# 🏠 Zillow Clone Scraper & Google Form Automation

This mini project scrapes real estate listings from a Zillow clone site and automatically submits them into a Google Form using Selenium. It's a hands-on example of web scraping + automation.

---

## 🧩 Features

- 🌐 Scrapes:
  - Property **addresses**
  - **Prices**
  - Listing **URLs**
- 📝 Automatically fills out a Google Form with the scraped data
- ⚙️ Uses both `requests + BeautifulSoup` for scraping and `selenium` for automation

---

## 🔧 Technologies

- `requests` — for fetching HTML pages
- `BeautifulSoup` — for parsing HTML and extracting data
- `selenium` — for interacting with the Google Form
- `ChromeDriver` — to control the Chrome browser

---

## ⚙️ Setup

1. Install required Python packages:

```bash
pip install requests beautifulsoup4 selenium
```

2. Download [ChromeDriver](https://sites.google.com/chromium.org/driver/) and ensure it matches your installed version of Chrome.
   - Place the executable in your project folder or add it to system PATH.

3. Update the target Google Form link in the script if needed:
```python
driver.get("https://YOUR-GOOGLE-FORM")
```

---

## ▶️ Usage

Run the script with:

```bash
python main.py
```

The script will:
1. Scrape addresses, prices, and links from [Zillow Clone](https://appbrewery.github.io/Zillow-Clone/)
2. Open a Chrome window
3. For each listing, fill out and submit the form
4. Close the browser after finishing

> ⚠️ Chrome window remains open after the script finishes (due to `detach=True`) so you can review the process.