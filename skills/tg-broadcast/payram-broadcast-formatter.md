---
name: payram-broadcast-formatter
description: Assemble and format the full PayRam weekly Telegram broadcast from individual content sections. Use this skill to combine the product update, competitor comparison, and button sections into one properly structured Telegram HTML message. Applies the broadcast styleguide and adds the header and footer.
---
# PayRam Broadcast Formatter Skill
## Your job
Take the three content sections and assemble them into one complete, ready-to-send Telegram HTML broadcast.
---
## Broadcast structure
[HEADER]
---
[PRODUCT UPDATE SECTION]
---
[COMPETITOR COMPARE SECTION]
---
[BUTTONS SECTION]
[FOOTER]
---
## Header
Draft a fresh 1-2 line header each week. Casual and relevant to the week's main theme.
Format:
👋 <b>PayRam Weekly | Week [X]</b>
[One line that frames the week's focus. Max 12 words.]
---
## Footer
Use this fixed footer every week:
Your stack. Your server. Your payments.
📩 Questions? Reply here or email <a href="mailto:sales@payram.com">sales@payram.com</a>
---
## Formatting rules
- All bold: <b>text</b>
- All italic: <i>text</i>
- Inline code: <code>text</code>
- Links: <a href="URL">Label</a>
- Bullets: • character (not - or *)
- Section headings: emoji + <b>Heading Text</b>
- No markdown (no **, no #)
- No em dashes
- Line breaks between bullets for readability
- Spell "onchain" without a hyphen
---
## Output
Return the complete broadcast as a single Telegram HTML block.
Label it: <!-- BROADCAST: WEEK [X] -->
Also return a plain-text preview summary (3 lines max) for Sheefa and Prabhat to review before sending.
