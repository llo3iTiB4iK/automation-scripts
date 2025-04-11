# 🤖 Python Automation Projects

A collection of small Python automation tools and scripts, built to practice web automation, API usage, and task automation using popular Python libraries like `Selenium`, `requests`, and `BeautifulSoup`.

---

## 📂 Projects

### 1. 🦖 Chrome Dinosaur Automation

**Goal**: Automate playing the Chrome offline dinosaur game.

- Uses `Selenium` to detect obstacles and simulate keyboard jumps.
- Ideal for understanding basic image detection and reaction time loops.
- Requires Google Chrome and the `chromedriver`.

➡️ [View project](chrome-dinosaur-automation)

---

### 2. 🧾 Data Entry Job Automation

**Goal**: Automate transferring data from a CSV file to a Google Form.

- Reads housing data from a file (e.g., price, address, link).
- Fills out a Google Form for each entry using `Selenium`.
- Useful for practicing web scraping, automation, and form submission.

➡️ [View project](data-entry-job-automation)

---

### 3. ✈️ Flight Deals Alert

**Goal**: Notify subscribed users when flight prices drop below a set threshold.

- Checks prices from a fixed city using the Tequila Kiwi API.
- Sends SMS and email alerts to users using `Twilio` and `SMTP`.
- Stores user and destination data in Google Sheets via the Sheety API.

➡️ [View project](flight-deals)

---

## ⚙️ Technologies Used

- `Selenium` — browser automation
- `BeautifulSoup` — web scraping (optional for some projects)
- `requests` — API communication
- `twilio`, `smtplib` — sending notifications
- `dotenv` — environment variable handling

---

## 🚀 Getting Started

Each project is standalone. To run any of them:

1. Clone the repository
2. Enter the folder for the desired project
3. Set up any required environment variables (`.env`)
4. Install libraries required for this project
5. Run the script.

---

## 📚 Learning Source

All projects are based on exercises and lessons from the  
[100 Days of Code: The Complete Python Pro Bootcamp](https://www.udemy.com/course/100-days-of-code/)