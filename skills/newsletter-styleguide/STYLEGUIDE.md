# Payments This Week by PayRam — Style Guide

> **Newsletter name:** Payments This Week by PayRam
> **Tagline:** "The week in payments, stablecoins, and the future of money — curated for builders."
> **Cadence:** Weekly, published Wednesday mornings
> **Format:** Markdown (Substack/Beehiiv/email compatible)

---

## Header Format

```
# Payments This Week by PayRam
## Edition #[N] | Week of [Month D–D, YYYY]

> The week in payments, stablecoins, and the future of money — curated for builders.
```

---

## Sections (in order)

Every edition must contain all sections. Omit a section only if there is genuinely zero content (rare).

| # | Section | Emoji | Words / Items |
|---|---------|-------|---------------|
| 0 | Intro | — | 50–80 words, 2–3 sentences |
| 1 | By the Numbers | 📊 | Exactly 3 stats |
| 2 | Top Story | 🔥 | 1 item, 40–60 words |
| 3 | Stablecoins & Crypto Rails | 💸 | 5–8 bullets, max 25–30 words each |
| 4 | Payments Infrastructure | 🏦 | 5–8 bullets, max 25–30 words each |
| 5 | Regulation & Policy | ⚖️ | 3–6 bullets, max 25–30 words each |
| 6 | Funding & Deals | 💰 | 4–10 items, sorted largest to smallest |
| 7 | Regional Spotlight | 🌎 | 2–4 bullets per region (Americas / EMEA / APAC) |
| 8 | PayRam Update | 🔵 | 1 item, bold headline + 40–80 words |
| 9 | Events | 📅 | 3–6 items |
| 10 | Footer | n/a | Fixed PayRam tagline |

---

## Section Formats

### Intro

A short editorial paragraph placed immediately after the tagline, before By the Numbers. Sets the tone for the week — 2–3 sentences, 50–80 words maximum. No section header, no emoji.

```markdown
[2–3 sentences summarising the week's dominant theme. What was the defining shift? Why does it matter now? What should readers carry into the sections below.]
```

**Rules:**
- No section header or emoji — plain paragraph only
- 50–80 words maximum
- Capture 1–2 defining themes, not a list of everything covered
- Write in present tense for ongoing implications, past tense for specific events
- No em dashes; no bare URLs; no source links in this section

---

### 📊 By the Numbers

Three impactful stats or data points from the week. Each stat must have a source link.

```markdown
## 📊 By the Numbers

- **$[X]B** [What it represents] ([Source](url?utm_source=payram))
- **[X]%** [What it represents] ([Source](url?utm_source=payram))
- **[X]M** [What it represents] ([Source](url?utm_source=payram))
```

**Rules:**
- Figures only — no editorializing in this section
- Use B/M/K for billions/millions/thousands
- Prefer dollar amounts, volume figures, adoption stats, market share
- No em dashes between the figure and the description; use a space only

---

### 🔥 Top Story

One featured story with the most industry-wide impact. 40–60 words maximum.

```markdown
## 🔥 Top Story

**[Headline linked to article](url?utm_source=payram)** [2–3 sentences: what happened, why it matters, what to watch. 40–60 words total.]
```

**Rules:**
- Bold the headline with a link
- Follow the headline with a single space, not an em dash
- "Why it matters" angle mandatory
- Avoid editorializing about PayRam or competitors

---

### 💸 Stablecoins & Crypto Rails

Bulleted list of stablecoin and crypto payment rail news.

```markdown
## 💸 Stablecoins & Crypto Rails

- **[Company/Project]** [What happened. Why it matters. Max 25–30 words.] ([Source](url?utm_source=payram))
- **[Company/Project]** ...
```

**Rules:**
- Bold the company/project name at the start of each bullet
- Maximum 25–30 words per bullet (excluding the source link)
- No em dashes; use periods or commas to separate clauses
- Source link in parentheses at the end, with `?utm_source=payram` appended to the URL
- Topics: stablecoin issuances, CBDC updates, Layer 2 payment rails, wallet integrations, DeFi payment protocols

---

### 🏦 Payments Infrastructure

Traditional and emerging payments infrastructure news.

```markdown
## 🏦 Payments Infrastructure

- **[Company]** [What happened. Max 25–30 words.] ([Source](url?utm_source=payram))
```

**Rules:** Same as Stablecoins section.

Topics: card networks (Visa/MC/Amex), real-time payment rails (FedNow/RTP/SEPA Instant), open banking, B2B payments, cross-border transfers, payment processors, embedded finance, BaaS.

---

### ⚖️ Regulation & Policy

Regulatory, legislative, and policy developments globally.

```markdown
## ⚖️ Regulation & Policy

- **[Country/Regulator]** [What was proposed/passed/rejected. Max 25–30 words.] ([Source](url?utm_source=payram))
```

**Rules:**
- Lead with the jurisdiction or regulator name in bold, not the company name
- Flag enforcement actions, new licensing requirements, sandbox launches, and court decisions
- Include jurisdiction flag emoji where space allows: 🇺🇸 🇪🇺 🇬🇧 🇸🇬 🇦🇪 🇧🇷 etc.
- No em dashes; use periods or commas to separate clauses

---

### 💰 Funding & Deals

All fundraising rounds and M&A this week. Two sub-formats:

**Funding:**
```markdown
- **[Company]** ([one-line description]) raised **$[X]M [Round]** led by [Investor]. ([Source](url?utm_source=payram))
```

**Acquisition:**
```markdown
- **[Acquirer]** acquired **[Target]** for **$[X]M**. [One-line strategic rationale.] ([Source](url?utm_source=payram))
```

**Rules:**
- Always bold company names and deal size
- Include the round type (Seed / Series A / Series B / etc.)
- If lead investor unknown, omit that clause rather than guess
- List from largest to smallest deal
- No em dashes; use periods to separate clauses

---

### 🌎 Regional Spotlight

Organized into three subsections. Use the region header format below.

```markdown
## 🌎 Regional Spotlight

### 🌎 Americas
- **[Company/Regulator]** [What happened. Max 25–30 words.] ([Source](url?utm_source=payram))

### 🇪🇺 EMEA
- **[Company/Regulator]** [What happened. Max 25–30 words.] ([Source](url?utm_source=payram))

### 🌏 APAC
- **[Company/Regulator]** [What happened. Max 25–30 words.] ([Source](url?utm_source=payram))
```

**Rules:**
- Stories here should not duplicate the main sections above unless regional context adds significant value
- Prefer stories about emerging markets, regional launches, and local regulatory moves

---

### 🔵 PayRam Update

First-party content: one feature launch, product milestone, or company news item per edition. Placed between Regional Spotlight and Events. Clearly labeled as PayRam content so readers understand the source.

```markdown
## 🔵 PayRam Update

**[Bold headline describing the feature or milestone]**

[2–3 sentences. What launched or happened. Who benefits. Why it matters. 40–80 words. End with a CTA link.]

[Try it → payram.com](https://payram.com)
```

**Rules:**
- One item only per edition. No bullet list.
- Bold headline at the top, plain prose below
- 40–80 words for the body copy (excluding headline and CTA)
- End every entry with a CTA linking to the relevant payram.com page
- No UTM tags on payram.com links
- Write in second or third person; do not use "we"
- **Facts only.** Every claim must be verifiable from payram.com, docs.payram.com, or a published press release/article. Do not invent corridors, integrations, milestones, or features.
- Acceptable topics: verified product milestones, published feature launches, confirmed integrations, press-released funding, or events PayRam has publicly announced attending

**Verified PayRam facts (as of March 2026):**
- Self-hosted private stablecoin payment gateway — no custodians, no KYC required
- Founded by Siddharth Menon (co-founder of WazirX, India's largest crypto exchange); quote: "The future of internet commerce runs on infrastructure you own, not services you rent."
- Publicly launched: November 10, 2025 ([Globe Newswire](https://www.globenewswire.com/news-release/2025/11/10/3184810/0/en/PayRam-Unveils-Private-Stablecoin-Payment-Gateway-For-Merchants-Individual.html))
- **MCP server integration (March 2026):** AI agents (Claude, Copilot, n8n) can deploy a stablecoin gateway in minutes, with no KYC or human intervention ([AccessNewsWire](https://www.accessnewswire.com/newsroom/en/blockchain-and-cryptocurrency/payram-enables-agents-to-go-live-with-a-self-hosted-stablecoin-paymen-1144001))
- $100M+ in on-chain volume processed
- 100+ active merchants globally
- Supports USDT and USDC on Ethereum, Base, Polygon, Tron, and Bitcoin; Solana and TON on roadmap
- Fees: under 1% vs. industry average of 6.5%
- Available in 190+ countries via smart routing
- MCP features: invoice generation, balance checking, automated fund sweeps, card-to-crypto onramp
- Key verticals: iGaming, e-commerce, SaaS, freelancers, NGOs, AI agents
- Seed funding: BuidlersTribe (August 2022); amount undisclosed

---

### 📅 Events

Upcoming payments/fintech events in the next 4–6 weeks.

```markdown
## 📅 Events

- **[Event Name]** · [Month D–D, YYYY] · [City or Online] → [Link](url?utm_source=payram)
```

**Rules:**
- Bold the event name
- Only include events with confirmed dates
- Favor events with free or accessible registration tiers; note if invite-only

---

### Footer

```markdown
---

*Payments This Week is curated by [PayRam](https://payram.com) — the platform connecting the next billion people to global payments via stablecoins.*

*[Subscribe](#) · [Unsubscribe](#) · [payram.com](https://payram.com)*
```

---

## General Writing Rules

1. **Be direct.** Every word must earn its place. Cut adjectives, hedge words, and brand fluff.
2. **Lead with the news, not the company.** "Stripe launched X" not "X was launched today by Stripe."
3. **Data over description.** If a figure exists, use it. "Raised $40M" beats "raised significant funding."
4. **Link the source, not the homepage.** Every bullet links to the specific news article, not company.com. Always append `?utm_source=payram` to source URLs (use `&utm_source=payram` if the URL already has query parameters).
5. **No em dashes.** Replace ( — ) with a period, comma, or colon. Use an en dash (–) only for date ranges and number spans.
6. **Word limit.** Standard bullets: 25–30 words maximum (excluding the source link in parentheses). Top Story: 40–60 words maximum.
7. **No speculation without attribution.** If something is "expected to" or "may," cite who said it.
8. **Tense:** Use simple past for events, present for ongoing developments.
9. **Jargon:** Define acronyms on first use per edition (e.g., CBDC, RTP, BaaS). Don't define them every edition.
10. **Emoji:** Only use the designated section emojis. Do not add emoji to bullet text.

---

## Tone Reference

| Good | Avoid |
|------|-------|
| "Visa expanded FedNow access to 500 banks." | "Visa is excited to announce..." |
| "MAS fined [Bank] $2M for AML failures." | "Regulators took action against..." |
| "USDC circulation hit $50B for the first time." | "Stablecoins are growing really fast." |
| "Circle filed for an IPO via S-1 with the SEC." | "Circle is taking a big step toward going public." |

---

## UTM Tagging Reference

All source links in the newsletter body must include `utm_source=payram`:

- URL with no existing params: `https://coindesk.com/article?utm_source=payram`
- URL with existing params: `https://coindesk.com/article?ref=xyz&utm_source=payram`

Footer links to payram.com are exempt from UTM tagging.
