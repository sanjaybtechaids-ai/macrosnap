MacroSnap 🥗📊

MacroSnap is an AI-powered nutrition assistant that helps users understand and track their daily macronutrient intake. It analyzes meal information, estimates calories, protein, carbohydrates, and fats, and generates a simple personalized nutrition summary.

✨ Features
🤖 AI-powered meal analysis
🥩 Protein, carbohydrate, and fat estimation
🔥 Daily calorie estimation
📊 Personalized macro summary
💬 Messaging integration using Twilio
🔐 Secure API-key management with Streamlit Secrets
🖥️ Simple Streamlit web interface
🛠️ Tech Stack
Python
Streamlit
AI API
Twilio
Git & GitHub
📁 Project Structure
macrosnap/
│
├── app.py
├── prompts.py
├── requirements.txt
├── .gitignore
│
└── .streamlit/
    ├── secrets.toml
    └── secrets.toml.example
File Description
File	Purpose
app.py	Main Streamlit application
prompts.py	AI system prompts and personality
requirements.txt	Python dependencies
.gitignore	Prevents secrets and unnecessary files from Git
secrets.toml	Stores API credentials locally
secrets.toml.example	Example configuration without real credentials
🚀 Installation
1. Clone the repository
git clone https://github.com/YOUR_USERNAME/macrosnap.git
cd macrosnap
2. Create a virtual environment

Windows:

python -m venv venv

macOS/Linux:

python3 -m venv venv
3. Activate the virtual environment

Windows PowerShell:

.\venv\Scripts\Activate.ps1

If PowerShell blocks it:

Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\venv\Scripts\Activate.ps1

macOS/Linux:

source venv/bin/activate
4. Install dependencies
pip install -r requirements.txt
🔑 Configuration

Create:

.streamlit/secrets.toml

Add your API credentials:

OPENAI_API_KEY = "your-api-key"

TWILIO_ACCOUNT_SID = "your-account-sid"
TWILIO_AUTH_TOKEN = "your-auth-token"
TWILIO_CONTENT_SID = "your-content-sid"

Never commit secrets.toml to GitHub.

The .gitignore should contain:

.streamlit/secrets.toml
venv/
__pycache__/
*.pyc
.env
▶️ Run the Application

Start MacroSnap with:

streamlit run app.py

Then open the local URL shown in the terminal, usually:

http://localhost:8501
💬 Twilio Integration

MacroSnap can be extended to send generated nutrition summaries through Twilio.

The basic workflow is:

User enters meal
       ↓
MacroSnap AI analyzes meal
       ↓
Calories + Protein + Carbs + Fat
       ↓
Daily summary generated
       ↓
Twilio
       ↓
Message sent to user

Custom Twilio Content Templates may require an upgraded Twilio account. The core MacroSnap application can still be developed and tested without this feature.

🔒 Security

Never expose API credentials in source code.

❌ Don't do:

api_key = "sk-your-real-key"

✅ Use Streamlit Secrets:

import streamlit as st

api_key = st.secrets["OPENAI_API_KEY"]
🎯 Future Improvements
📷 Food image recognition
🍽️ Automatic meal detection
📈 Weekly and monthly nutrition analytics
🎯 Personalized nutrition goals
🗓️ Meal history
📱 Mobile-friendly interface
💬 WhatsApp integration
🔔 Daily nutrition reminders
📊 Interactive nutrition dashboard
