# n8n_airtable_telegram_leads
n8n Landing Page Lead Automation & CRM Notifier
An automated workflow built with n8n that handles incoming "Get early access" leads from a landing page, saves them directly into an Airtable CRM base, and instantly triggers real-time notifications via a Telegram Bot.
🚀 Key Features
Webhook Integration: Receives real-time POST requests from the landing page form via a secure tunnel (e.g., ngrok) on localhost.
CRM Sync (Airtable): Automatically creates a new record in the CRM Leads table containing user details (Full Name, Email, Company).
Instant Telegram Alerts: Sends a formatted HTML notification via a Telegram bot (Lead Flow Notifier) so the team can reach out to leads without checking the database manually.
Data Mapping: Dynamically extracts webhook payload fields and passes them across nodes seamlessly.
🛠 Tech Stack
n8n: Core workflow automation engine.
Webhook Node: Event-driven trigger for HTTP requests.
Airtable API: Cloud-based CRM storage.
Telegram Bot API: Instant mobile notifications.
ngrok: Local environment tunneling for testing webhooks.
📁 Repository Structure
My workflow.json — Exported n8n workflow file containing all nodes, triggers, and mappings.
README.md — Project documentation.
⚙️ How to Run
Clone or download this repository.
Download the My workflow.json file.
Open your n8n instance, click on options (...), and select Import from File....
Select My workflow.json to load the workflow into your canvas.
Set up your Airtable Credentials and link your target table (CRM Leads).
Set up your Telegram Bot Credentials (Bot Token and Chat ID) in the Send a text message node.
Run a test POST request to your webhook URL (via local testing or a live landing page form).
Toggle the workflow to Active.
🔮 Roadmap & Next Improvements
Add email confirmation auto-reply to the user upon submission.
Integrate scoring based on company size or email domain.
