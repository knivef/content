---
name: research-payments-news
description: Research and gather this week's payments and stablecoin news for the "Payments This Week by PayRam" newsletter. Use this skill whenever the user asks to research payments news, find stablecoin stories, gather newsletter content, look up what happened in fintech this week, or wants to pull together industry news for a payments-focused audience. Also triggers on phrases like "what's new in payments", "stablecoin news this week", "find newsletter stories", "payments research", or "gather fintech news". Always use this skill before generating the newsletter.
---

# Research: Payments & Stablecoins News

Your job is to research and compile the week's most important stories across payments and stablecoins, organized into structured categories for newsletter assembly.

## How to run

**Default:** Research the current week (Mon–Sun based on today's date).

**With a specific week:** If the user provides a date range, use that instead.

Read `references/sources.md` for the curated source list before searching — it tells you which outlets to prioritize per category.

---

## Research Process

### Step 1: Determine the week

Calculate the Monday–Sunday date range for the current week. Today is the anchor date. Format: `YYYY-MM-DD`.

### Step 2: Search all categories

Run searches across **all 6 categories** below. For each category, run **2–3 targeted searches** using the WebSearch tool. Use search queries that include the current week or month to get recent results.

Search query patterns:
- `[topic] news [month] [year]`
- `[company/regulator] [action] payments [month] [year]`
- `stablecoin [event type] [month] [year]`

**Categories to research:**

1. **Stablecoins & Crypto Rails**
   - Stablecoin issuances, burns, integrations, new launches
   - CBDC pilots and announcements
   - Layer 2 / payment rail updates (Lightning, Arbitrum, etc.)
   - Crypto payment integrations (Visa/MC crypto programs, wallet payments)

2. **Payments Infrastructure**
   - Real-time payment rail news (FedNow, RTP, SEPA Instant, PIX, UPI, etc.)
   - Card network updates (Visa, Mastercard, Amex, UnionPay)
   - Cross-border / FX / remittance
   - Embedded finance, BaaS, open banking
   - Major processor news (Stripe, Adyen, Fiserv, FIS, etc.)

3. **Regulation & Policy**
   - New legislation, bills, or regulatory guidance
   - Enforcement actions, fines, sanctions
   - Licensing news (approvals, denials, new frameworks)
   - Central bank policy affecting payments

4. **Funding & M&A**
   - Venture rounds (seed through growth) in payments/stablecoins/fintech
   - Acquisitions and mergers
   - IPOs and SPACs in the space

5. **Regional Spotlight**
   - Americas (US, Canada, LatAm): search separately
   - EMEA (Europe, Middle East, Africa): search separately
   - APAC (Asia-Pacific): search separately

6. **Metrics & Data** (for "By the Numbers")
   - Volume milestones (transaction counts, $ volumes)
   - Market cap, circulation figures for stablecoins
   - Adoption stats (users, merchants, banks onboarded)

### Step 3: Collect stories

For each story found, capture:
- Headline (as written in source)
- 1-sentence summary
- Source URL
- Category (which of the 6 above)
- Impact level: HIGH / MEDIUM / LOW (your judgment)

Aim for **8–15 stories per category** before filtering. You will filter down during writing.

### Step 4: Identify the Top Story

Select the single most impactful story of the week. Criteria (in order):
1. Largest systemic impact on the payments industry
2. Highest-profile company or regulator involved
3. Biggest deal size or policy change
4. Most novel/first-of-its-kind development

### Step 5: Extract "By the Numbers" stats

Find 3 concrete data points with dollar/percentage/volume figures. Must be from this week's news or a report released this week.

---

## Output Format

Save to: `/Users/kvn/Claude/Weekly Industry Newsletter/newsletters/[YYYY-MM-DD]/research.md`

Use `YYYY-MM-DD` = the Monday of the researched week.

```markdown
# Research: Payments This Week — Week of [Month D–D, YYYY]
_Generated: [today's date]_

---

## 🔢 By the Numbers (candidates)

- **$[X]B** — [stat description] | Source: [url]
- **[X]%** — [stat description] | Source: [url]
- **[X]M** — [stat description] | Source: [url]
- _(add extras as backups)_

---

## ⭐ Top Story Candidate

**[Headline]**
Summary: [2–3 sentences on what happened and why it matters]
Source: [url]

---

## 💸 Stablecoins & Crypto Rails

- [HIGH/MED/LOW] **[Company/Project]** — [Headline] | [1-line summary] | [url]
- ...

---

## 🏦 Payments Infrastructure

- [HIGH/MED/LOW] **[Company]** — [Headline] | [1-line summary] | [url]
- ...

---

## ⚖️ Regulation & Policy

- [HIGH/MED/LOW] **[Jurisdiction/Regulator]** — [Headline] | [1-line summary] | [url]
- ...

---

## 💰 Funding & M&A

- [HIGH/MED/LOW] **[Company]** — $[X]M [Round] | [What they do] | Lead: [Investor] | [url]
- ...

---

## 🌎 Regional

### Americas
- [HIGH/MED/LOW] **[Company/Regulator]** — [summary] | [url]

### EMEA
- [HIGH/MED/LOW] **[Company/Regulator]** — [summary] | [url]

### APAC
- [HIGH/MED/LOW] **[Company/Regulator]** — [summary] | [url]

---

## 📅 Events

- **[Event Name]** · [Date] · [Location] | [url]
- ...
```

---

## After saving

Tell the user:
- The week researched
- How many stories were found per category
- The top story candidate
- The path where `research.md` was saved
- Suggest running `/generate-newsletter` next to produce the final newsletter
