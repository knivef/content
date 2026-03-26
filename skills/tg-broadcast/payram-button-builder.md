---
name: payram-button-builder
description: Build the inline button block for PayRam's weekly Telegram broadcast. Use this skill to generate 2 to 3 Telegram inline buttons with correct UTM-tagged URLs. Week number must be provided or inferred from the broadcast date.
---
# PayRam Button Builder Skill
## Your job
Generate the inline button block for the weekly PayRam Telegram broadcast.
Buttons link to the feature or product update highlighted in the broadcast. Each button gets a UTM-tagged URL.
---
## UTM format
?utm_source=tgbroadcast2026wkX
Where X = the ISO week number of the Monday the broadcast is sent.
Use Python or date logic to confirm the correct ISO week number if unsure.
The broadcast sends every Monday at 4PM IST.
Example for Monday March 17, 2026 (Week 12):
https://docs.payram.com/card-to-crypto?utm_source=tgbroadcast2026wk12
---
## Button source list
Pick 2 to 3 buttons relevant to the week's content.
| Label | Base URL |
|---|---|
| 🦀 Ask your Agent to Deploy PayRam | https://mcp.payram.com |
| 💳 Activate Card-to-Crypto Onramp | https://docs.payram.com/card-to-crypto |
| 📖 Read the Docs | https://docs.payram.com |
| 📅 Book a Demo | https://calendly.com/payram-sales/30min |
| 🔍 Explore How Card-to-Crypto Works | https://payram.com/card-to-crypto |
| ⚡ Get Started Free | https://payram.com |
| 🛠 View Supported Networks | https://docs.payram.com/supported-networks |
Always match buttons to the section content. If the product update covers agentic payments, lead with the MCP/agent button.
---
## Output format
Return a JSON array for the Telegram bot inline keyboard:
{
  "inline_keyboard": [
    [{"text": "🦀 Ask your Agent to Deploy PayRam", "url": "https://mcp.payram.com?utm_source=tgbroadcast2026wkX"}],
    [{"text": "💳 Activate Card-to-Crypto Onramp", "url": "https://docs.payram.com/card-to-crypto?utm_source=tgbroadcast2026wkX"}]
  ]
}
Also return a human-readable preview:
Button 1: [label] → [full URL]
Button 2: [label] → [full URL]
Label output: <!-- BUTTONS: WEEK [X] -->
