✈️ Flight Deal Tracker
An automated flight price tracker that finds the cheapest flights from a specified origin to multiple international destinations and notifies users via email and WhatsApp when prices drop below a defined threshold.

📌 Features
Automatically fetches IATA codes for cities

Searches for both direct and indirect flights

Compares flight prices with the lowest threshold

Sends notifications via:

📧 Email

💬 WhatsApp (via Twilio)

Google Sheets integration for destination data and user email management

🧠 Tech Stack
Python

Google Sheets API – for managing destination and customer data

Flight Search API (e.g., Tequila/Kiwi) – to search for flight prices

Twilio API – for sending WhatsApp and SMS alerts

SMTP – for sending notification emails

🛠️ Project Structure
bash
Copy code
flight-deal-tracker/
├── data_manager.py         # Handles reading/writing data to Google Sheets
├── flight_search.py        # Manages flight search API queries
├── flight_data.py          # Utility to extract and find the cheapest flight
├── notification_manager.py # Sends email and WhatsApp messages
└── main.py                 # Main script that ties everything together
🔧 How It Works
Fetches city data and updates IATA codes in Google Sheet if missing.

Searches for flights from a fixed origin city (e.g., London) to listed destinations.

Identifies the cheapest direct or indirect flight.

Sends notifications to customers if prices are lower than a specified threshold.

🚀 Getting Started
1. Clone the repository
bash
Copy code
git clone https://github.com/your-username/flight-deal-tracker.git
cd flight-deal-tracker
2. Install dependencies
bash
Copy code
pip install -r requirements.txt
3. Set up environment variables
Create a .env file with the following credentials:

env
Copy code
TEQUILA_API_KEY=your_kiwi_tequila_api_key
SHEET_ENDPOINT=https://api.sheety.co/your_endpoint
SHEET_TOKEN=your_sheety_token
TWILIO_SID=your_twilio_sid
TWILIO_AUTH_TOKEN=your_twilio_auth_token
TWILIO_WHATSAPP_NUMBER=whatsapp:+14155238886
SENDER_EMAIL=your_email@example.com
EMAIL_PASSWORD=your_email_password
4. Run the project
bash
Copy code
python main.py
✅ Prerequisites
Google Sheet with:

Destination city names

Price threshold

(Optional) Email list of users

Tequila (Kiwi) API key

Twilio account for WhatsApp messaging

SMTP credentials for email

📧 Notifications
WhatsApp messages are sent using Twilio's WhatsApp sandbox.

Email notifications are sent via SMTP.

📈 Learning Outcomes
Hands-on experience with RESTful APIs

Automating workflows using Python

Working with structured data in Google Sheets

Real-time customer notifications
