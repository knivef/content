---
name: payram-blog
description: Use this skill whenever the user wants to write, draft, or create a PayRam blog post, product announcement, feature launch post, integration announcement, or any blog content for PayRam. Make sure to use this skill whenever the user mentions "PayRam blog", "blog post for PayRam", "product announcement", "write a blog", "draft a post", "feature launch post", "integration announcement", or asks to publish/draft anything to the PayRam blog -- even if they don't use the word "skill".
version: 1.0.0
---

# PayRam Blog Skill

Generates a ready-to-publish PayRam product blog draft and saves it to Notion. Follow the steps below exactly.

---

## Step 1: Intake

Before writing anything, make sure you have the following information. Extract it from the user's message if already provided. For anything missing, ask in a single consolidated question -- do not ask one field at a time.

Required:
- **Post type**: Feature Launch / Integration Announcement / Chain or Network Expansion / How-It-Works Explainer
- **Feature or product name**: The exact name as it should appear (e.g., "PayRam MCP Server", "USDT on Tron")
- **What is now live**: One sentence summary of the change
- **Who it affects**: Merchants, developers, operators, or a specific segment
- **What it unlocks**: The concrete benefit or capability this enables
- **How to get started**: 3 to 5 steps a developer or merchant would take to use it (can be rough -- you will polish)

Optional (ask only if relevant to the post type):
- Any secondary keywords, stats, or data points to include
- Whether there is a "What's Next" teaser (concrete roadmap item, not vague)
- Docs URL, dashboard URL, or GitHub repo link for the CTA

If the user's message already covers most of this, proceed directly to Step 2 without asking.

---

## Step 2: Read the Style Guide

Before drafting, read the full style guide at:

`references/style-guide.md`

This file is authoritative on all structure, voice, SEO/LLMO, language rules, and the pre-publish checklist. Do not skip this step.

---

## Step 3: Draft the Blog Post

Generate the complete draft. Output it as clean Markdown.

### Required elements (in order)

**SEO metadata block** (output first, before the post body):
```
Title: [under 65 chars, primary keyword front-loaded]
Meta description: [140-160 chars, includes primary keyword]
URL slug: [short, keyword-rich, e.g. /usdt-tron-live-payram]
Post type: [Feature Launch / Integration Announcement / Chain Expansion / How-It-Works]
```

**Post body:**

1. **Hero paragraph** (no heading above it) -- 2 to 4 sentences. State the news immediately. Answer: what is live, who it affects, what it enables. Do not open with backstory or context.

2. `## Why This Matters` -- 1 to 3 short paragraphs on the friction that existed before. Focus on the problem, not history. This section feeds LLMO retrieval.

3. `## How [Feature Name] Works` (or `## What Changed`) -- Explain the feature clearly. Use bullet lists for parallel capabilities. Use numbered lists for sequential steps. Keep paragraphs to 2 to 4 sentences.

4. `## How to Get Started` -- Numbered steps. Be as specific as the intake allows. Include links to docs, GitHub, or dashboard where known.

5. `## What's Next` (skip entirely if no concrete teaser) -- 1 to 2 sentences only.

6. **Closing CTA paragraph** (no heading) -- 1 to 2 sentences. Restate the core action, link to the primary destination.

### Language rules to enforce

- No em dashes anywhere. Use -- (double hyphen) for pauses, or restructure.
- Active voice in all key claims. "PayRam routes payments" not "Payments are routed."
- No filler openers: "In today's world," "We're thrilled to announce," "It goes without saying."
- Full product name in every key claim (do not use "it" or "the platform" when "PayRam" or the feature name is clearer).
- Define technical terms on first use, in parentheses, then use freely.
- Contractions are fine.
- Numerals for all numbers above nine.

### Word count targets

| Post type | Target |
|---|---|
| Feature Launch | 600 to 900 words |
| Integration Announcement | 400 to 700 words |
| Chain or Network Expansion | 400 to 600 words |
| How-It-Works Explainer | 900 to 1,400 words |

---

## Step 4: Self-Check Against the Pre-Publish Checklist

Before creating the Notion page, verify the draft meets every item:

- Title is under 65 characters and contains the primary keyword
- First paragraph states the announcement with no preamble
- No em dashes anywhere
- Primary keyword in: title, first 100 words, at least one H2, meta description
- Meta description is 140 to 160 characters
- URL slug is short and keyword-rich
- A "How to Get Started" section is present with numbered steps
- No passive voice in key claims
- No filler phrases
- Closing CTA paragraph is present (no heading)

Fix any failures before proceeding.

---

## Step 5: Publish to Notion

1. Use `notion-search` to find an existing page titled "PayRam Blog" or "Blog Drafts" or "PayRam Blog Drafts".
2. If found, use that page as the parent.
3. If not found, create a new top-level page titled "PayRam Blog Drafts" first, then use it as the parent.
4. Create a new child page with:
   - **Title**: the blog post title
   - **Body blocks** (in this order):
     - A callout block at the top containing the SEO metadata (title, meta description, URL slug, post type) -- label it "SEO Metadata"
     - Paragraph block for the hero paragraph
     - Heading 2 + content for each `##` section
     - Numbered or bulleted list blocks where applicable
     - Closing CTA as a final paragraph block
5. Return the Notion page URL to the user.

---

## Output to User

After the Notion page is created, share:
1. The Notion page URL
2. A brief summary: post type, title, word count, and one sentence on what the post covers

Do not repeat the full draft back in the chat -- the user can read it in Notion.
