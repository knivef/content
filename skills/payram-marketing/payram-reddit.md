# PayRam Reddit Post Generator

Draft a Reddit post for PayRam based on the current day's content bucket. Reddit posts must read like a community member sharing a genuine observation or resource, not a brand. Never pitch. Always educate or discuss.

## Step 1: Determine the Bucket

Derive from today's day if not specified:

| Day | Bucket | Format |
|-----|--------|--------|
| Monday | Industry (Stablecoins/Payments) | Long (discussion post) |
| Tuesday | Product Feature/Update | Long (Show & Tell) |
| Wednesday | Educational | Long (educational post) |
| Thursday | Narrative | Long (opinion/discussion) |
| Friday | Product Positioning | Short (Q&A / observation) |
| Saturday | Meme / Fun | Short (meme or community) |
| Sunday | Community / Engagement | Short (community thread) |

## Step 2: Thursday Narrative Selection

Calculate: `(ISO week number - 1) mod 9 + 1`

| # | Narrative | Reddit Angle |
|---|-----------|-------------|
| 1 | Your PSP Is Selling Your Customers Back to You | "I looked into what [PSP] actually does with merchant data. Here is what I found." |
| 2 | Data Privacy Is Architecture Not Policy | "Privacy policies don't change data flows. Here is the difference." |
| 3 | Hidden Cost of Free Analytics | "Stripe Sigma is built on your transaction data. Here is how that works." |
| 4 | The Merchant Who Built the Customer List | "Your PSP knows your best customers as well as you do. Whose asset is that?" |
| 5 | Self-Hosted as Competitive Infrastructure | "Treating your payment layer like infrastructure instead of a vendor. Thoughts?" |
| 6 | Your Competitors Are Getting Smarter About You | "Same PSP, same vertical, aggregated benchmarks. Is this a problem?" |
| 7 | What Zero Collection Actually Means | "Walked through how a self-hosted gateway handles data vs. a hosted one." |
| 8 | iGaming Operators Sitting on a Data Time Bomb | "iGaming PSPs offer 'player insights' products. Where does that data come from?" |
| 9 | iGaming and the Card-to-Crypto Privacy Problem | "Players use crypto for privacy. Their onramp usually defeats the purpose." |

Frame the post as a personal investigation, take, or question — not a product feature announcement.

## Step 3: Research (Industry + Educational Only)

Use WebSearch for 1-2 recent stories (past 7 days):
- "stablecoin payments news [current month year]"
- "crypto merchant payments [current month year]"
- "self-hosted payment gateway [current month year]"

Anchor to the most relevant story. Fall back to evergreen angle if nothing surfaces.

## Format Rules

### Long Post (Mon, Tue, Wed, Thu)
- **Title:** Clear, curiosity-driven, not promotional. Max 300 characters.
- **Body:**
  - Opening paragraph: frame the observation, question, or finding (2-3 sentences)
  - 2 to 4 sections with plain headers (no markdown bold — use `**Header**` sparingly, Reddit renders it)
  - Bullet points allowed where they help readability
  - Mention PayRam once in context if relevant — never as the focus
  - Close with an open question inviting community response
- Length: 300 to 600 words

### Short Post (Fri, Sat, Sun)
- **Title:** Direct question or punchy take
- **Body:** 2 to 4 sentences, neutral tone
- Frame as a take, observation, or community question
- No product pitch whatsoever

### Show & Tell Format (Tuesdays)
- Title: "I built / set up / tested [X] — here is what I found"
- Focus on the experience and outcome, not the product spec
- Include one specific detail that makes it feel real (setup time, a specific step, a surprise)

## Subreddit Selection

Always suggest the 1 to 2 most relevant subreddits for the post:

| Bucket | Best Subreddits |
|--------|----------------|
| Industry | r/CryptoCurrency, r/stablecoins, r/fintech |
| Product | r/selfhosted, r/entrepreneur, r/webdev |
| Educational | r/CryptoCurrency, r/personalfinance, r/fintech |
| Narrative | r/entrepreneur, r/ecommerce, r/stripe, r/smallbusiness |
| Positioning | r/selfhosted, r/SaaS, r/entrepreneur |
| Meme / Fun | r/CryptoCurrency, r/Bitcoin |
| Community | r/entrepreneur, r/fintech, r/AMA |

## Brand Voice Rules

- Community-first. Write as a participant, not a marketer.
- Anti-PSP sentiment is high in r/entrepreneur, r/ecommerce, r/stripe — meet them where they are
- If mentioning PayRam: once, in context, not as a pitch. Treat it as one relevant data point.
- Never use: "revolutionary," "game-changing," "best-in-class," "check out our product"
- Never use em dashes
- Spell "onchain" without a hyphen
- Reddit users will flag anything that reads like marketing. When in doubt, make it more neutral.

**Verified product facts (use only if contextually natural):**
- Networks: Ethereum, Base, Polygon, Tron, Bitcoin
- No setup, subscription, or rolling reserve fees
- No merchant KYC, no customer data collection
- Self-hosted, non-custodial, permissionless
- MCP server works with Claude and GitHub Copilot
- Setup in under 10 minutes
- Docs: docs.payram.com

## Output

Label the post before the copy:

```
<!-- REDDIT | [BUCKET] | [DAY, DATE] | [SHORT or LONG] -->
Suggested subreddits: r/[sub1], r/[sub2]
```

Then return:
- **Title:** [post title]
- **Body:** [post body]

---

## Final Step: Save to Notion

After outputting the post, save it to the PayRam Content Calendar in Notion using the `notion-create-pages` tool.

**Data source ID:** `599eaa85-81e2-465a-a2c0-668556e61d44`

**Page properties to set:**
- `Post Title`: the Reddit post title
- `Channel`: `Reddit`
- `Content Bucket`: the bucket for this post (Industry / Product / Educational / Narrative / Positioning / Meme / Fun / Community)
- `Format`: `Short`, `Long`, or `Show & Tell` as appropriate
- `Status`: `Draft`
- `Scheduled Date`: today's date (ISO format)
- `Week`: the ISO week number as a number
- `Post Copy`: the full post body text
- `Notes`: the suggested subreddits (e.g. `r/fintech, r/CryptoCurrency`)
- `Narrative Angle`: only set if Thursday — use the matching value from the select options (e.g. `3 Hidden Analytics Cost`)

Confirm the save with a single line: `Saved to Notion ✓`
