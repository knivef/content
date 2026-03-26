---
name: payram-product-update
description: Research and draft the product features/update section for PayRam's weekly Telegram broadcast. Use this skill whenever you need to surface the most relevant PayRam product update, new feature, or capability highlight for the current week. Pulls from docs.payram.com and payram.com.
---
# PayRam Product Update Skill
## Your job
Draft the product update section for the weekly PayRam Telegram broadcast.
One focused feature per broadcast. It should feel like a useful tip from a teammate, not a press release.
---
## Step 1: Research
Fetch the latest from these sources before drafting:
- https://docs.payram.com
- https://payram.com
- https://mcp.payram.com
Look for:
- Recently added features or capabilities
- Underused but valuable features worth highlighting
- Features relevant to the current narrative focus (agentic payments OR card-to-crypto onramp)
If no new update is apparent, surface the most contextually relevant existing feature for this week.
---
## Step 2: Draft the section
Format rules:
- Use Telegram HTML: <b>, <i>, <code>, <a href="">
- Section header: emoji + bold heading
- 1 short intro line (max 12 words)
- 3 to 5 bullet points using •
- Each bullet: one clear benefit or fact, max 15 words
- End with one <code> block if there is a relevant prompt or command to show
Tone: Casual, direct, peer-to-peer. No marketing fluff.
Product facts to stay accurate on:
- Supported networks: Ethereum (ETH, USDT, USDC), Base (ETH, USDC, cbBTC), Polygon (USDC, USDT, POL), Tron (TRX, USDT), Bitcoin (BTC)
- No setup fees, no subscription fees, no rolling reserves, no KYB, no merchant KYC
- Transaction fees apply
- Self-hosted, non-custodial, permissionless
- MCP server works with Claude and Copilot
- Setup in under 10 minutes
- Spell "onchain" without a hyphen
Do not:
- Reference "20+ tokens"
- Use em dashes
- Use passive voice
- Invent features not in the docs
---
## Output
Return only the formatted Telegram HTML block for this section.
Label it clearly: <!-- SECTION: PRODUCT UPDATE -->
