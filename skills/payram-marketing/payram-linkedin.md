# PayRam LinkedIn Post Generator

Draft a LinkedIn post for PayRam based on the current day's content bucket. Posts should read like a thoughtful founder sharing something useful, not a brand announcement.

## Step 1: Determine the Bucket

Derive from today's day if not specified:

| Day | Bucket | Format |
|-----|--------|--------|
| Monday | Industry (Stablecoins/Payments) | Long-form |
| Tuesday | Product Feature/Update | Long-form |
| Wednesday | Educational | Long-form |
| Thursday | Narrative | Long-form |
| Friday | Product Positioning | Short |
| Saturday | Meme / Fun | Short |
| Sunday | Community / Engagement | Short (Week Recap) |

## Step 2: Thursday Narrative Selection

Calculate: `(ISO week number - 1) mod 9 + 1`

| # | Narrative |
|---|-----------|
| 1 | Your PSP Is Selling Your Customers Back to You |
| 2 | Data Privacy Is Architecture Not Policy |
| 3 | Hidden Cost of Free Analytics |
| 4 | The Merchant Who Built the Customer List |
| 5 | Self-Hosted as Competitive Infrastructure |
| 6 | Your Competitors Are Getting Smarter About You |
| 7 | What Zero Collection Actually Means |
| 8 | iGaming Operators Sitting on a Data Time Bomb |
| 9 | iGaming and the Card-to-Crypto Privacy Problem |

Lead with the core tension. Use the narrative's data and content hooks. Name PSPs by name (Stripe, PayPal, Square, Nuvei, PaySafe) when referencing their practices. Be factual, not inflammatory.

## Step 3: Research (Industry + Educational Only)

Use WebSearch for 1-2 recent stories (past 7 days):
- "stablecoin payments news [current month year]"
- "crypto payments merchant adoption [current month year]"
- "payments infrastructure news [current month year]"

Anchor the post to the most relevant story. Fall back to an evergreen angle if nothing recent surfaces.

## Format Rules

### Long-form (Mon, Tue, Wed, Thu)
- 400 to 800 words
- Opening line: 1-2 sentences, story-driven or tension-first — no product mention in the first 2 sentences
- Use **Bold Headers** for sections (markdown bold)
- Bullet points allowed, use - prefix
- Translate any crypto/tech term in plain language on first use
- Close with a clear CTA: book a demo, visit docs.payram.com, or reply with a question
- 3 to 5 hashtags on the final line, separated by spaces

### Short (Fri, Sat, Sun)
- 3 to 5 lines, no headers, no bullets
- Conversational, first-person or second-person voice
- Line 1 is the hook — end it without a period to create a curiosity gap
- End with a question to drive comments
- No hashtags on short posts (optional: 1-2 max)

### Week Recap (Sunday)
- 200 to 350 words
- Reference the week's themes without being exhaustive
- Personal and forward-looking tone
- Close with what's coming next week or an open question

## Brand Voice Rules

- Casual, direct, like a founder talking to another founder
- Never use em dashes
- Spell "onchain" without a hyphen
- Lead with the problem or tension, never with the product
- No corporate speak: no "leverage," "synergy," "best-in-class," "innovative," "cutting-edge"
- Privacy is an architectural argument, not a moral one
- Avoid: "we take your privacy seriously," "privacy-first" without technical backing

**Preferred phrases:**
- "zero collection by design"
- "architectural guarantee, not a policy promise"
- "self-hosted infrastructure"
- "you own the payment layer"
- "payments without surveillance"
- "infrastructure, not a platform"

**Verified product facts:**
- Networks: Ethereum, Base, Polygon, Tron, Bitcoin
- No setup, subscription, or rolling reserve fees
- No merchant KYC, no customer data collection by PayRam
- Self-hosted, non-custodial, permissionless
- MCP server works with Claude and GitHub Copilot
- Setup in under 10 minutes
- Docs: docs.payram.com

## Output

Label the post before the copy:

```
<!-- LINKEDIN | [BUCKET] | [DAY, DATE] | [SHORT or LONG] -->
```

Then return the post copy, ready to paste into LinkedIn.

---

## Final Step: Save to Notion

After outputting the post, save it to the PayRam Content Calendar in Notion using the `notion-create-pages` tool.

**Data source ID:** `599eaa85-81e2-465a-a2c0-668556e61d44`

**Page properties to set:**
- `Post Title`: A short descriptive title for the post (5-8 words summarising the angle)
- `Channel`: `LinkedIn`
- `Content Bucket`: the bucket for this post (Industry / Product / Educational / Narrative / Positioning / Meme / Fun / Community)
- `Format`: `Short` or `Long` as appropriate
- `Status`: `Draft`
- `Scheduled Date`: today's date (ISO format)
- `Week`: the ISO week number as a number
- `Post Copy`: the full post text
- `Narrative Angle`: only set if Thursday — use the matching value from the select options (e.g. `2 Privacy Is Architecture`)

Confirm the save with a single line: `Saved to Notion ✓`
