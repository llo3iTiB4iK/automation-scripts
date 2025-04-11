# ✈️ Flight Deals Alert

A Python project that tracks cheap flight deals from a specific city to popular destinations. If a lower-than-usual price is found, the system notifies all subscribed users via SMS and email.

---

## 📁 Project Structure

### `flight-deals/`

Main flight alert logic:

- `main.py` — for each destination in the spreadsheet:
  - ensures the IATA code is filled (via Tequila API),
  - searches for the cheapest flight in the next 6 months,
  - sends an alert if a deal is found below the set price.

- `data_manager.py` — reads and updates the Google Sheet data using Sheety API.

- `flight_search.py` — performs flight searches via the Kiwi Tequila API.

- `notification_manager.py` — handles notifications:
  - sends SMS using Twilio,
  - sends emails using SMTP.

### `customer_acquisition/`

Handles user registration:

- `main.py` — prompts new users for their name and email and validates their input.
- `sheety.py` — connects to the Sheety API to store user information in the `users` sheet.

---

## 🔐 Environment Variables

The following variables should be set in a `.env` file or your system environment:

```
SHEETY_PRICES_ENDPOINT=
SHEETY_USERS_ENDPOINT=
SHEETY_AUTHORIZATION=
TEQUILA_API_KEY=
TEQUILA_ENDPOINT=https://api.tequila.kiwi.com
TWILIO_SID=
TWILIO_AUTH_TOKEN=
TWILIO_PHONE_NUMBER=
YOUR_EMAIL=
YOUR_EMAIL_PASSWORD=
```

---

## 📊 Google Sheet Format

Two sheets are used:

1. `prices` — contains destination cities and desired minimum prices:
   ```
   city | iataCode | lowestPrice
   ```

2. `users` — stores registered users:
   ```
   firstName | lastName | email
   ```

---

## 🚀 How to Run

Register a new user:

```bash
cd customer_acquisition
python main.py
```

Search for deals and notify users:

```bash
cd ../flight-deals
python main.py
```

---

## 📦 Dependencies

Install required libraries:

```bash
pip install requests twilio python-dotenv
```

Also uses:

- `smtplib` (built-in)
- `datetime` (built-in)

---

## 🧠 Notes

- Flight search uses the Tequila API (https://tequila.kiwi.com/).
- User data and destinations are stored in Google Sheets.
- Notifications are sent only if a flight deal is below the predefined threshold.

---

## 🛠️ Ideas for Improvement

- Support multiple departure cities.
- Add a Telegram bot for instant alerts.
- Track historical price trends and show charts.

---

## 📚 Based On

Inspired by Day 39 of the course  
[100 Days of Code: The Complete Python Pro Bootcamp](https://www.udemy.com/course/100-days-of-code/)