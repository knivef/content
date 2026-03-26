---
name: generate-newsletter
description: Generate the "Payments This Week by PayRam" newsletter from researched news. Use this skill whenever the user asks to generate, write, create, or format the weekly newsletter. Also triggers on "write this week's newsletter", "format newsletter from research", "create payram newsletter", "assemble the newsletter", "produce the newsletter", or "turn research into newsletter". Requires research.md to exist (run research-payments-news skill first if it doesn't). Always produces a complete, publication-ready markdown newsletter following the PayRam styleguide.
---

# Generate: Payments This Week Newsletter

Your job is to take structured research notes and produce a publication-ready markdown newsletter following the PayRam styleguide exactly.

## Before you start

1. Read `STYLEGUIDE.md` at `/Users/kvn/Claude/Weekly Industry Newsletter/STYLEGUIDE.md`
2. Read `references/template.md` in this skill's directory for the full section template
3. Find `research.md` — either from the path the user provides, or auto-detect the most recent one in `/Users/kvn/Claude/Weekly Industry Newsletter/newsletters/`

If no `research.md` exists, tell the user to run `/research-payments-news` first.

---

## Generation Process

### Step 1: Parse research.md

Read the research file and extract:
- The week date range
- "By the Numbers" candidates
- Top Story candidate
- All stories per category with their impact levels

### Step 2: Filter and select

For each section, apply these selection rules:

**By the Numbers:** Pick exactly 3 stats. Prefer: largest dollar figures, most surprising percentages, most concrete adoption metrics.

**Top Story:** Use the research file's top story candidate unless you spot something clearly more impactful. The top story should be an event, not a stat.

**Stablecoins (5–8 items):** Include all HIGH items. Add MEDIUM items until you reach 8 max, prioritizing novelty and audience relevance.

**Payments Infrastructure (5–8 items):** Same as above.

**Regulation (3–6 items):** Include all HIGH items. Only add MEDIUM if directly relevant to US, EU, or major LatAm/APAC markets.

**Funding & Deals (4–10 items):** Include all deals with disclosed amounts. Sort largest to smallest. For undisclosed, add a note "(amount undisclosed)".

**Regional Spotlight (2–4 per region):** Avoid duplicating stories already in main sections unless regional context adds substantial new information.

**Events (3–6):** Include only events in the next 4–6 weeks with confirmed dates.

### Step 3: Write the newsletter

Follow the STYLEGUIDE formatting rules exactly:
- Use the formats defined in STYLEGUIDE.md for each section
- Bold company names, deal sizes, stat figures
- Every bullet must include a source link in parentheses at the end
- 1–2 sentences per bullet (except Top Story: 2–3 sentences)
- No bare URLs — all links embedded in text

### Step 4: Write the edition header

Calculate the edition number based on the week. Week 1 = first edition (March 9, 2026). Increment by 1 per week.

```markdown
# Payments This Week by PayRam
## Edition #[N] | Week of [Month D–D, YYYY]

> The week in payments, stablecoins, and the future of money — curated for builders.

---
```

### Step 5: Assemble and write the file

Save to: `/Users/kvn/Claude/Weekly Industry Newsletter/newsletters/[YYYY-MM-DD]/newsletter.md`

Use `YYYY-MM-DD` = the Monday of the newsletter's week.

---

## Quality checklist before saving

- [ ] All 9 sections present
- [ ] By the Numbers has exactly 3 stats
- [ ] Top Story has a bold hyperlinked headline + 2–3 sentences
- [ ] Every bullet in every section has a source link in parentheses
- [ ] Funding items sorted largest to smallest
- [ ] Regional section has all 3 sub-regions (Americas / EMEA / APAC)
- [ ] Footer is present
- [ ] No bare URLs (all links embedded in text)
- [ ] Total word count under 1,500 (aim for 900–1,200 for readability)

---

## After saving

Tell the user:
- Path to the saved newsletter
- Section item counts (e.g., "5 stablecoin items, 6 payments items...")
- Word count
- Any sections that had fewer items than the minimum (flag for manual review)
