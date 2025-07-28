🧠 What This Workflow Does
- ✅ Responds to missed calls in seconds
- ✅ Uses AI to handle conversations
- ✅ Tracks every lead automatically
- ✅ Alerts you for emergencies
🛠️ Setup Guide
Step 1: Import the Workflow
Copy the JSON file
In n8n, click “Import”
Paste and import
Step 2: Get Your API Keys
Twilio (for SMS)
Sign up at twilio.com
Get a phone number with SMS ($1/month)
Copy your Account SID and Auth Token
OpenAI (for AI responses)
Sign up at platform.openai.com
Create an API key
Add $5 credit to start
Airtable (for lead tracking)
Sign up at airtable.com (free)
Create a base called “Leads”
Add these fields:
Phone (Phone number type)
Status (Single select: New Lead, Contacted, Qualified, Converted)
Source (Text)
Created (Date)
Last Contact (Date)
Gmail (for alerts)
Use your existing Gmail
Enable 2FA
Connect via OAuth2 in n8n
Step 3: Add Credentials in n8n
Click on each node with a red credential warning
Add new credentials
Test each one
Step 4: Update Environment Variables
In n8n settings, add:
BUSINESS_NAME=Your Business Name
TWILIO_PHONE=+1234567890
NOTIFICATION_EMAIL=your@email.com
AIRTABLE_BASE=appXXXXXXXXXXXXXX
​
Step 5: Test Your Workflow
Test Missed Call:
curl -X POST https://your-n8n.com/webhook/missed-call-demo \  -H "Content-Type: application/json" \  -d '{"From": "+1234567890", "CallStatus": "no-answer"}'
​
Test SMS Reply:
curl -X POST https://your-n8n.com/webhook/sms-reply-demo \  -H "Content-Type: application/json" \  -d '{"From": "+1234567890", "Body": "I need emergency plumbing help!"}'