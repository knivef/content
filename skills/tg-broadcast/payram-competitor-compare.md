---
name: payram-competitor-compare
description: Draft the competitor comparison section for PayRam's weekly Telegram broadcast. Use this skill to highlight one specific way PayRam differs from or outperforms a named competitor. Rotates across relevant competitors each week. Keeps comparisons factual and spec-level.
---
# PayRam Competitor Comparison Skill
## Your job
Draft the competitor comparison section for the weekly PayRam Telegram broadcast.
One competitor. One clear difference. Keep it factual.
---
## Competitor rotation
Rotate through these in order. Track which was used last week if context is available.
1. NOWPayments
2. CoinGate
3. Coinbase Commerce
4. BitPay
5. TripleA
6. Plisio
If the user specifies a competitor, use that one instead.
---
## Step 1: Pick the angle
Choose one specific differentiator. Good angles:
- KYC/KYB requirements vs PayRam's zero merchant KYC
- Custodial vs PayRam's non-custodial model
- Fee structure: subscriptions or rolling reserves vs PayRam's transaction-only fees
- Self-hosting vs SaaS dependency
- Agentic/MCP support (PayRam has it; most don't)
- Network and token support breadth
---
## Step 2: Draft the section
Format rules:
- Use Telegram HTML: <b>, <i>
- Section header: emoji + bold heading
- 1 intro line naming the competitor and the angle
- Comparison in 2-column bullet style:
  - <b>[Competitor]:</b> [what they do]
  - <b>PayRam:</b> [what PayRam does instead]
- Max 3 comparison pairs
- Close with one punchy line (max 10 words) that lands the point
Tone: Confident, not arrogant. Factual, not a takedown.
Do not:
- Make claims you cannot verify from public sources
- Use vague language like "better" or "more powerful"
- Use em dashes
- Reference "20+ tokens"
---
## Output
Return only the formatted Telegram HTML block for this section.
Label it clearly: <!-- SECTION: COMPETITOR COMPARE -->
