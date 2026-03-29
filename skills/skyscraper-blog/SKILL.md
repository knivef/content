---
name: skyscraper-blog
description: Use this skill whenever the user wants to write a skyscraper blog post, a long-form SEO article designed to outrank competitors, or any content using the Skyscraper Technique. Trigger on: "skyscraper post", "skyscraper blog", "SEO blog post", "write a blog that outranks", "competitive blog", "link-building blog post".
version: 1.0.0
---

# Skyscraper Blog Skill

Produces a skyscraper-style blog post: the most useful, specific, and credible resource on a given topic -- written for a real audience, not a search engine. Follow these steps exactly.

---

## Step 1: Intake

Before writing anything, gather the following. Extract from the user's message if already provided. For anything missing, ask in a single consolidated question -- do not ask one field at a time.

Required:
- **Target keyword**: The primary search term this post should rank for
- **Target audience**: Who will read this (e.g., SaaS founders, e-commerce merchants, developers)
- **Improvement vector**: How this post will be better than what already ranks (see options in `references/writing-guide.md`)
- **Your expertise angle**: What first-hand knowledge, data, or perspective you bring to this topic

Optional (ask only if relevant):
- Any original data, case studies, or stats you want to include
- Competing articles you've already identified
- Target word count or publication deadline

If the user's message already covers most of this, proceed directly to Step 2 without asking.

---

## Step 2: Read the Writing Guide

Before drafting, read the full writing guide at:

`references/writing-guide.md`

This file is authoritative on research standards, structure rules, voice requirements, the AI pattern audit, and the Google quality checklist. Do not skip this step.

---

## Step 3: Research Audit

Identify 3 to 5 articles currently ranking for the target keyword. For each one, document:

- What it covers well
- What is outdated, missing, or shallow
- Whether it contains original data or just summarizes others
- Whether it could have been written by anyone with no real expertise

Summarize your findings as an "improvement brief" -- a short list of what your post will do that none of the competitors do. Share this brief with the user before writing if the improvement angle is not already confirmed.

---

## Step 4: Draft the Post

Generate the complete draft as clean Markdown. Follow all structure, voice, and formatting rules from the writing guide.

### Required structure

1. **Opening** (no heading) -- Lead with the most useful insight. State what the reader will get within the first 3 sentences. No preamble, no rhetorical questions.

2. **Body sections** (H2/H3) -- Each section must:
   - Advance a specific argument or answer a specific question
   - Contain at least one concrete example, data point, or real-world reference
   - Add something the competing articles do not have

3. **Closing** (no "In conclusion" or "In summary") -- End with a clear action, direct recommendation, or specific next step.

### Language rules to enforce

- No em dashes. Use -- (double hyphen) for pauses, or restructure the sentence.
- Active voice in all key claims.
- No filler openers: "In today's world," "In this article we will," "It goes without saying."
- Vary sentence length deliberately. Mix short (emphasis) and long (context).
- Take a clear stance. Do not hedge every claim.

---

## Step 5: AI Pattern Audit

Before outputting the draft, scan it against every item in the AI Pattern Audit section of the writing guide. This includes:

- Inflated meaning phrases (e.g., "stands as a testament to", "plays a vital role")
- Promotional filler (e.g., "breathtaking", "rich heritage")
- Editorial commentary (e.g., "it's important to note", "needless to say")
- Over-used connectors used more than once (moreover, furthermore, in addition)
- Negation structures ("It's not just X, it's Y") -- rewrite as direct positive claims
- Vague authority ("Studies show...", "Industry reports suggest...") -- name the source or cut the claim
- Empty -ing endings -- cut participial phrases that add no information
- Bullet points with bold labels -- rewrite as prose or remove the bold

Fix every instance found before proceeding.

---

## Step 6: Output

Return the final draft as clean Markdown.

Also provide a short summary:
- Word count
- Improvement vector used
- Top 3 things this post has that the competing articles do not
- Suggested outreach targets (the 3 to 5 posts it improves upon, for link-building follow-up)

Do not pad the draft to hit a word count. Stop when the reader's question is fully answered.
