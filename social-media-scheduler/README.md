# Social Media Scheduler — n8n Template

## What it does
Receives content via webhook (or form) and posts simultaneously to Twitter/X and LinkedIn. Perfect for scheduling social media content from any tool or CMS.

## Use Cases
- Blog post promotion — auto-share new articles
- Product launches — coordinated multi-platform posts
- Content calendar execution — feed from Notion/Airtable
- Marketing automation — trigger posts from any webhook-capable tool

## How it works
1. **Webhook** receives POST with content, platforms, hashtags, optional image
2. **Parser** formats text for each platform (280 char limit for Twitter)
3. Posts in parallel to **Twitter/X** and **LinkedIn**
4. **Logs** result and returns confirmation

## Installation
1. Import `workflow.json` into n8n
2. Set up credentials:
   - Twitter/X: OAuth 2.0 (Developer Portal → API keys)
   - LinkedIn: OAuth 2.0 (LinkedIn Developer → App)
3. Activate the workflow
4. POST to `https://your-n8n.com/webhook/schedule-post`

## API Usage
```bash
curl -X POST https://your-n8n.com/webhook/schedule-post \
  -H "Content-Type: application/json" \
  -d '{
    "content": "Just launched our new automation template! 🚀",
    "platforms": ["twitter", "linkedin"],
    "hashtags": ["automation", "n8n", "nocode"],
    "link": "https://yoursite.com/templates"
  }'
```

## Screenshots
> [Workflow screenshot placeholder]

## Requirements
- n8n v1.0+
- Twitter/X Developer Account + API keys
- LinkedIn App with posting permissions
