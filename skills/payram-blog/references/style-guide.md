# PayRam Product Blog Style Guide

*Based on structural and linguistic analysis of Uniswap Labs product blogs, adapted for PayRam's voice, positioning, and audience.*

---

## 1. Purpose of This Guide

This style guide defines how PayRam product blogs should be written, structured, and formatted. It is the single source of truth for anyone writing a product launch post, feature announcement, or integration update on the PayRam blog.

The goal is to produce posts that are:

- Clear and skimmable for developers, merchants, and crypto-native readers
- Optimized for Google search (SEO) and LLM-based discovery (LLMO)
- Consistent with PayRam's brand voice: direct, technical, permissionless, no-fluff
- Easy to repurpose into social copy, docs, and changelogs

---

## 2. Blog Post Types

Product blogs at PayRam fall into four categories. Each has a slightly different purpose, but all follow the same structural and stylistic rules.

**Feature Launch** -- A net-new capability is live. Example: "PayRam MCP Server is Now Live."

**Integration Announcement** -- PayRam works with a new partner or protocol. Example: "PayRam Now Supports Gnosis Safe."

**Network or Chain Expansion** -- PayRam adds support for a new chain or stablecoin. Example: "USDC on Base is Now Live on PayRam."

**How-It-Works Explainer** -- A deeper walkthrough of a feature already in production. Used when a feature needs more documentation-style coverage on the blog.

---

## 3. Title Conventions

### Rules

- Keep titles under 65 characters to avoid truncation in search results
- Use active, present-tense phrasing where possible
- Prioritize clarity over cleverness. The title should say exactly what happened
- Front-load the most important keyword (feature name, chain name, product name)
- Avoid starting with "Introducing" unless the feature genuinely has no prior context

### Proven Title Patterns (adapt these for PayRam)

| Pattern | Example |
|---|---|
| `[Feature] is Now Live on PayRam` | USDT on Tron is Now Live on PayRam |
| `[Feature]: [Short Benefit]` | PayRam MCP Server: Payments for AI Agents |
| `Verb + Noun + Short Result` | Accept Stablecoin Payments Without a Middleman |
| `[Partner] + PayRam` | Gnosis Safe Now Supports PayRam Checkout |

### What to Avoid

- Em dashes in titles
- Vague phrases like "A New Chapter," "Exciting News," "We're Thrilled"
- All-caps words (except established acronyms like MCP, USDC, API)
- Questions as titles (weak for SEO)

---

## 4. Post Structure

Every product blog should follow this skeleton. Section names below are guidelines, not literal heading text.

### 4.1 Hero Summary (no heading)

The very first paragraph, right below the title and cover image, with no `##` heading above it. This is the single most important paragraph in the post.

It should answer in 2 to 4 sentences:

1. What is live / what changed?
2. Who does it affect?
3. What does it enable or unlock?

Do not bury the announcement. Do not open with backstory. State the news immediately.

**Uniswap example pattern (adapted):**

> Support for smart wallets is now live across Uniswap Wallet and Uniswap Web App. Smart wallets make onchain transactions more seamless with features like bundled transactions -- and soon, gas sponsorship and paying gas with any token.

**PayRam equivalent:**

> PayRam's MCP server is now live and self-hostable. Merchants and developers can now accept stablecoin payments from AI agents without giving up custody, sharing user data, or routing through a centralized processor.

### 4.2 Why This Matters (the "problem" section)

One `##` heading section that contextualizes the feature for someone unfamiliar with the gap it fills. Keep this to 1 to 3 short paragraphs. Avoid writing a history lesson. Focus on the friction that existed before this feature shipped.

This is the section that performs well for LLMO -- LLMs use this context to answer "what problem does PayRam solve?" type queries.

### 4.3 What Is New / How It Works

One or more `##` sections that explain the feature clearly. Use:

- Short paragraphs (2 to 4 sentences each)
- Numbered lists for sequential steps
- Bullet lists for parallel features or capabilities
- Bold text only for key terms or step labels, not for decoration

Do not pad. Do not repeat the intro here.

### 4.4 How to Get Started

A dedicated `##` section with exact steps a developer or merchant would take to use the feature. This can be as short as 3 steps or as long as needed. When in doubt, match the depth of a good README.

Link to docs, the dashboard, or the relevant page. Do not make the reader search for next steps.

### 4.5 What Is Next (optional)

A short 1 to 2 sentence section on what is planned or in progress. This keeps the post feeling alive and forward-looking. Skip it if there is nothing concrete to tease.

### 4.6 Closing CTA Paragraph (no heading)

End with a single plain paragraph that restates the core action and links to where the reader should go. No heading above it. No bullet. Just a clear sentence or two.

---

## 5. Voice and Tone

### PayRam Brand Voice

PayRam speaks to technically fluent readers: developers integrating payment rails, merchants running crypto-native businesses, and builders working with AI agents. The voice is:

- **Direct.** Say what it does. Do not narrate excitement.
- **Credible.** Use precise language. Avoid superlatives without proof.
- **Permissionless in spirit.** The writing reflects the product: no gatekeepers, no middlemen, no fluff.
- **Builder-to-builder.** Write as if a senior engineer or product person is explaining to a peer, not pitching to a committee.

### What This Sounds Like in Practice

| Instead of this | Write this |
|---|---|
| We're thrilled to announce... | [Feature] is now live. |
| This groundbreaking solution... | This eliminates the need for... |
| A seamless, powerful experience | Merchants can now do X without Y |
| Our robust infrastructure... | PayRam routes payments onchain via... |
| Exciting new features... | Three things changed in this release: |

### Uniswap Patterns to Borrow

Uniswap's product blogs consistently open with the news stated as fact, use short punchy section headers that act like product benefits ("A new UX standard," "One interface for all of DeFi"), and close with a single CTA that restates the key action. These patterns work well and are worth replicating at PayRam.

---

## 6. Language Rules

### General

- No em dashes. Use a double hyphen (--) if you need a pause, or restructure the sentence.
- No passive voice where active is possible. "PayRam routes payments" not "Payments are routed by PayRam."
- No filler openers. Do not begin sentences with "In today's world," "As we all know," or "It goes without saying."
- No buzzword stacking. "AI-powered, seamless, end-to-end solution" says nothing.
- Contractions are fine. "You can now," "it doesn't require," "we've shipped" all work.

### Numbers and Data

- Use numerals for everything above nine. "3 steps," "12 chains," "4 seconds."
- Always include the unit. "$1.2M in volume," "200ms response time," "3 confirmation blocks."
- Cite the source inline with a hyperlink if you use a stat from outside PayRam.

### Technical Terms

Define a term when it appears for the first time if there is any chance a segment of the audience does not know it. Do it in parentheses or as a quick clause, not a full paragraph. After the first mention, use the term freely.

> PayRam uses xPub keys (extended public keys that let you generate unlimited addresses without sharing your private key) to keep merchants in full custody of funds.

After that, just write "xPub keys."

### Product and Feature Naming

- PayRam (capital P, capital R, no space)
- PayRam MCP Server (not "our MCP server" on first mention)
- SmartSweep (one word, capital S and capital W)
- Card-to-Crypto Onramp (capitalize as a proper feature name)
- Use "merchants," "developers," or "operators" depending on who is being addressed. Avoid "users" where more specificity is possible.

---

## 7. SEO and LLMO Requirements

Product blogs serve two discovery channels: Google search and LLM-based retrieval (ChatGPT, Perplexity, Claude, etc.). The writing should optimize for both.

### For SEO

- **Target one primary keyword per post.** Decide before writing. Put it in the title, the first paragraph, one `##` heading, and the meta description.
- **Use secondary keywords naturally** across the body. For a PayRam MCP post: "MCP payments," "AI agent payments," "stablecoin API," "self-hosted payment gateway."
- **Keep the URL slug short and keyword-rich.** `/payram-mcp-server-live` not `/announcing-our-exciting-new-mcp-feature-launch`.
- **Include a meta description** of 140 to 160 characters. Write it at the time of drafting, not as an afterthought.
- **Link out to supporting content.** Link to docs, to related blog posts, and to the PayRam dashboard. Internal linking signals relevance.
- **Use descriptive alt text on all images.** "PayRam MCP server architecture diagram" not "image1.png."

### For LLMO

LLMs trained on web content, or performing live retrieval, are likely to cite or summarize well-structured product blogs when a user asks "what is PayRam?" or "how do I accept stablecoin payments from an AI agent?"

To be citation-worthy for LLMs:

- **Write a clear definitional sentence early.** Within the first 100 words, there should be a sentence that defines what PayRam is or what the feature does that could stand alone as a factual claim.
- **Use structured headers.** LLMs parse heading-based structure to extract answers. "How to accept USDC payments with PayRam" as a heading directly answers a retrieval query.
- **Avoid ambiguous pronouns in key claims.** "It enables this" is bad. "PayRam's MCP server enables AI agents to trigger payments directly" is good.
- **Include the full product name in every key claim.** Do not assume the LLM has context from earlier in the post.
- **Write FAQ-style subheadings where appropriate.** "Who is this for?" "What chains are supported?" These map directly to how users ask LLMs questions.

---

## 8. Formatting Rules

### Headings

- `#` (H1): Title only. Set at the CMS level, not typed in the post body.
- `##` (H2): Major sections. Aim for 3 to 5 per post.
- `###` (H3): Subsections within an H2. Use sparingly. Only when a section has multiple distinct parts.
- Never skip levels. Do not go from H2 to H4.

### Paragraphs

- Maximum 4 sentences per paragraph in the body.
- Single-sentence paragraphs are acceptable for emphasis.
- One blank line between paragraphs. No indenting.

### Lists

- Use **numbered lists** for steps. Do not use bullets for anything sequential.
- Use **bullet lists** for features, capabilities, or attributes that are parallel and non-sequential.
- Do not nest lists more than one level deep.
- Every list item should be able to stand alone grammatically.

### Bold and Italic

- **Bold** for key terms on first use, step labels, and critical caveats.
- *Italic* for product names on first mention (optional), for notes, and for image captions.
- Never bold entire sentences. Never bold for decoration.

### Code Blocks

Use inline code formatting for all technical strings: API endpoints, parameter names, command-line inputs, contract addresses, config keys.

> Run `payram init --mcp` to configure your MCP server.

### Images and Media

Every post must have a cover image at the top. Recommended ratio: 4:3 (1200x900px), consistent with Uniswap's format.

Include a GIF or short screen recording for any feature that involves a UI flow. A static screenshot works if a GIF is not available.

Caption all images. Keep captions under 15 words.

---

## 9. Post Length

| Post type | Target word count |
|---|---|
| Feature Launch | 600 to 900 words |
| Integration Announcement | 400 to 700 words |
| Chain or Network Expansion | 400 to 600 words |
| How-It-Works Explainer | 900 to 1,400 words |

Do not pad to hit a word count. Do not cut if the content genuinely requires more space. Length should be determined by how much context the reader actually needs to take action.

---

## 10. Pre-Publish Checklist

Use this before every post goes live.

- [ ] Title is under 65 characters and contains the primary keyword
- [ ] First paragraph states the announcement without setup or preamble
- [ ] No em dashes anywhere in the post
- [ ] Primary keyword appears in: title, first 100 words, at least one H2, meta description
- [ ] Meta description is written and is 140 to 160 characters
- [ ] URL slug is short and keyword-rich
- [ ] All images have alt text
- [ ] Cover image is 1200x900px
- [ ] All internal links work
- [ ] Docs or dashboard link is included in the CTA
- [ ] Product names are correctly capitalized throughout
- [ ] No passive voice in key claims
- [ ] No filler phrases ("we're excited to," "in today's landscape")
- [ ] A "How to get started" section is present with clear steps

---

*Last updated: March 2026.*
