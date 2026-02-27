# Daily Email Digest — n8n Template

## What it does
Aggregates content from multiple RSS feeds and sends a beautifully formatted daily email digest at your preferred time.

## Use Cases
- Morning news roundup from your favorite tech blogs
- Industry monitoring (competitors, market trends)
- Team knowledge sharing — curated content delivered daily
- Personal learning feed

## How it works
1. **Schedule Trigger** fires daily at configured time (default: 8 AM)
2. **RSS Feed Reader** fetches latest items from all configured feeds
3. **Code Node** formats items into an HTML email digest
4. **Email Node** sends the digest to configured recipients

## Installation
1. Import `workflow.json` into n8n (Menu → Import from File)
2. Edit the Code node — update the `config` object with your feeds and email
3. Configure your SMTP credentials in n8n (Settings → Credentials → SMTP)
4. Activate the workflow

## Configuration
See `config.example.json` for all options:
- `feeds`: Array of RSS feed URLs
- `max_items_per_feed`: Limit items per source
- `recipient_email`: Where to send the digest
- `send_time_hour`: Hour to trigger (24h format)

## Screenshots
> [Workflow screenshot placeholder]

## Requirements
- n8n v1.0+
- SMTP credentials (Gmail, SendGrid, etc.)

## License
Single-use commercial license. See purchase terms.
