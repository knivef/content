# PayRam Weekly Telegram Broadcast | Run Orchestrator
## What this does
Runs the full weekly broadcast generation workflow.
Calls each skill in sequence and assembles the final output.
Run this every Monday morning before 4PM IST.
---
## Inputs required before running
Confirm these before starting:
1. Week number (ISO week of the current Monday)
2. Narrative focus this week: Agentic payments OR Card-to-crypto onramp OR specify other
3. Competitor to highlight: name one OR leave blank to auto-rotate
4. Any specific feature or update to prioritize: name it OR leave blank to auto-select
---
## Step 1: Research product update
Read skills/tg-broadcast/payram-product-update.md and follow it.
- Fetch latest from docs.payram.com, payram.com, mcp.payram.com
- Identify the most relevant feature for this week's narrative focus
- Draft the product update section in Telegram HTML
---
## Step 2: Draft competitor comparison
Read skills/tg-broadcast/payram-competitor-compare.md and follow it.
- Use the competitor from inputs, or rotate to the next one
- Pick the strongest factual differentiator relevant to this week's narrative
- Draft the competitor section in Telegram HTML
---
## Step 3: Build buttons
Read skills/tg-broadcast/payram-button-builder.md and follow it.
- Confirm the ISO week number
- Match buttons to the product update and narrative focus
- Generate inline keyboard JSON and human-readable preview
---
## Step 4: Assemble full broadcast
Read skills/tg-broadcast/payram-broadcast-formatter.md and follow it.
- Combine all sections with correct structure and dividers
- Apply all formatting rules
- Output the complete Telegram HTML block
---
## Step 5: Final output
Return three things:
1. Complete broadcast — ready to paste into Telegram
2. Button JSON — ready to pass to Telegram bot API
3. Team summary — 3-line plain-text brief for Sheefa and Prabhat to review before sending
---
## Broadcast styleguide (quick ref)
- Telegram HTML only: <b>, <i>, <code>, <a href="">
- Bullets: •
- Dividers: ---
- Tone: casual, direct, peer-to-peer
- No em dashes
- Spell "onchain" without a hyphen
- UTM format: ?utm_source=tgbroadcast2026wkX
- Sends: Monday 4PM IST
