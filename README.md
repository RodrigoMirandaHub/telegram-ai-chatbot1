# telegram-ai-chatbot1
Telegram AI chatbot built with n8n, Groq (Llama 3.3) and Google Sheets for memory. Free and open source.


Telegram AI Chatbot with Memory — n8n + Groq + Google Sheets

📌What this project does
A fully functional AI chatbot running on Telegram, powered by Groq's Llama 3.3 model, with conversation history saved automatically to Google Sheets. Built entirely on free tools with zero cost.

💻Tech Stack
n8n — workflow automation (hosted on Railway)
Groq API — free AI inference (Llama 3.3 70b)
Telegram Bot API — messaging interface
Google Sheets — conversation memory storage

🛠How it works
User sends a message to the Telegram bot
n8n captures the message via Telegram Trigger
HTTP Request sends the message to Groq API with a custom system prompt
Groq returns an AI response
n8n sends the response back to the user on Telegram.

Both the user message and AI response are saved to Google Sheets with timestamp

📚What I learned
Building webhook-based automations with n8n
Integrating third-party APIs via HTTP Request
Using system prompts to customize AI behavior
Storing structured data in Google Sheets via API
Deploying n8n on Railway with environment variables.

🏢Flow Architecture
Telegram Trigger → HTTP Request (Groq) → Send Message → Append Row (user) → Append Row (assistant)

Setup
Clone this workflow JSON into your n8n instance
Add your Groq API key as Header Auth credential
Connect your Telegram bot token
Connect Google Sheets OAuth
Create a sheet with columns: chat_id, role, content, timestamp
Deploy and set webhook URL via Telegram API
