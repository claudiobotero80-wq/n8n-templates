# Lead Capture Notifier — n8n Template

## What it does
Receives form submissions via webhook, saves leads to Google Sheets, and sends instant notifications via email and Slack.

## Use Cases
- Landing page contact forms
- Event registration capture
- Quote/demo request forms
- Any web form that needs CRM-like tracking

## How it works
1. **Webhook** receives POST with lead data (name, email, phone, etc.)
2. **Parser** normalizes data from any form format
3. In parallel:
   - **Google Sheets** saves lead to spreadsheet
   - **Email** sends notification to sales team
   - **Slack** posts to #leads channel
4. Returns `200 OK` to the form

## Installation
1. Import `workflow.json` into n8n
2. Set up credentials: Google Sheets OAuth, SMTP, Slack Bot Token
3. Update the Google Sheets node with your spreadsheet ID
4. Update email recipient and Slack channel
5. Point your form's action URL to: `https://your-n8n.com/webhook/lead-capture`
6. Activate

## Form Integration
```html
<form action="https://your-n8n.com/webhook/lead-capture" method="POST">
  <input name="name" required>
  <input name="email" type="email" required>
  <input name="phone">
  <input name="company">
  <textarea name="message"></textarea>
  <input name="source" type="hidden" value="website">
  <button type="submit">Send</button>
</form>
```

## Screenshots
> [Workflow screenshot placeholder]

## Requirements
- n8n v1.0+
- Google Sheets API credentials
- SMTP credentials
- Slack Bot Token (optional)
