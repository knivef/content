---
name: content-review
description: Use this skill whenever the user wants to proofread, edit, review, or improve a blog post, article, or long-form content before publishing. Trigger on: "proofread this", "edit this post", "review my article", "check this before I publish", "edit my blog", "review this content", "polish this draft", "clean this up".
version: 1.0.0
---

# Content Review Skill

Reviews, corrects, and improves any blog post, article, or long-form content before publication. The goal is not grammatical cleanliness -- it is making the content genuinely useful, credibly human, and worth reading.

Run all four passes in sequence. Do not combine them.

---

## Step 1: Read the Editing Guide

Before starting any edits, read the full editing guide at:

`references/editing-guide.md`

This file is authoritative on structural rules, Google quality standards, the AI pattern audit, and line-level editing. Do not skip this step.

---

## Step 2: Receive the Content

Ask the user to paste the full content they want reviewed if they have not already done so. Also ask:

- Is there a specific concern or problem they already know about?
- Is there any section that should not be changed?

If the content is already in the message, proceed directly to Step 3.

---

## Step 3: Pass 1 -- Structural Edit

Read the entire post before making any changes. Evaluate the architecture:

- Is the central argument clear within the first 3 sentences?
- Does each section advance the argument or stall it?
- Is the most important information at the top of each section?
- Does the conclusion land on a specific point, action, or recommendation?

Flag and fix:
- Buried lede -- move the main point to the top
- Padding sections -- cut or merge
- Redundant coverage -- merge or cut duplicate sections
- Weak opening -- rewrite if it opens with preamble, promise, or rhetorical question
- Weak conclusion -- rewrite if it summarizes instead of landing on a point

---

## Step 4: Pass 2 -- Google Quality Edit

Check the revised content against Google's helpful content standards:

- [ ] Does the post provide original information, analysis, or perspective?
- [ ] Does every factual claim have a named, verifiable source?
- [ ] Is the most useful content at the top of each section?
- [ ] Does the title accurately describe the content without exaggeration?
- [ ] Would a reader finish this and know what to do next?
- [ ] Is there a byline with author context?
- [ ] Does the post demonstrate first-hand experience?
- [ ] For YMYL topics: are claims backed by authoritative sources?

For any failure: fix it directly or flag it clearly if it requires information only the author has (e.g., adding a byline, naming a source).

Also apply the People-First test: was this written to help a specific reader, or to rank for a keyword? Flag these patterns if found:
- Covers a topic with no real experience behind it
- Answers vaguely and redirects to a contact form
- Includes sections that are topically adjacent but not genuinely useful
- Promises to answer a question that has no real answer

---

## Step 5: Pass 3 -- AI Pattern Edit

Work through the post section by section. Flag and rewrite every instance of these patterns (detailed rules in `references/editing-guide.md`):

1. **Inflated meaning** -- phrases like "stands as a testament to", "plays a vital role", "watershed moment"
2. **Promotional tone** -- "breathtaking", "rich heritage", "must-see", "world-class"
3. **Editorial commentary** -- "it's important to note", "needless to say", "it goes without saying"
4. **Overused connectors** -- limit "moreover", "furthermore", "in addition", "in contrast" to one use per post each
5. **Negation structures** -- rewrite every "It's not just X, it's Y" as a direct positive claim
6. **Vague authority** -- name the source or cut the claim; no "studies show", "experts agree", "research suggests"
7. **Empty -ing endings** -- cut participial phrases that add no information
8. **Bold label bullet points** -- remove bold labels from bullet items; rewrite as prose if needed
9. **Uniform sentence structure** -- introduce rhythm variation where paragraphs read with the same cadence
10. **No specificity** -- flag any major section with no named examples, data points, or direct experience

---

## Step 6: Pass 4 -- Line-Level Edit

Work sentence by sentence:

- Cut filler words: "very", "quite", "basically", "essentially", "actually", "just", "simply"
- Rewrite passive constructions in active voice
- Split or cut any sentence over 30 words
- Remove redundant pairs: "each and every", "first and foremost", "end result", "future plans"
- Check all pronouns ("it", "this", "they") have an unambiguous referent

---

## Step 7: Final Checklist

Before returning the edited content, verify every item in the Final Publication Checklist in `references/editing-guide.md`. If anything fails, fix it now.

---

## Step 8: Output

Return:
1. The fully edited post as clean Markdown
2. A brief editing summary covering:
   - Structural changes made and why
   - Google quality issues found (and whether they were fixed or flagged for the author)
   - Count of AI patterns removed
   - Any items that require the author's input to resolve (missing sources, byline, direct experience gaps)
