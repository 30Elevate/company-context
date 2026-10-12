---
name: company-context
description: Runs a short interview that builds company-context.md, a business-context file for AI tools such as ChatGPT, Claude, Gemini and Copilot. Asks one question at a time, fills a template, and never overwrites an existing file silently. Runs in the user's language. Use when the user wants their AI assistant to know their company, or mentions "company-context.md", "business context file", "context file for my company" or "set up AI for my business".
allowed-tools: Read, Write
---

# Interview: company-context.md

Walk a business owner through a short interview. Build `company-context.md`
from the answers. This file gives an AI tool the company's context, so it
answers like someone who knows the company, not like a text generator.

**Language:** start in the language the user wrote in (English if there is
no message yet) and continue the interview in it. Write the file in the language the
business uses with its customers, and ask if that is unclear. Keep the
template headings, and translate them only if the user wants.

Apply `references/GUARDRAILS.md` to the whole
conversation and to every output.

## How to run the interview

- **One question at a time.** A conversation, not a form. Wait for the
  answer, ask a follow-up if it is vague, and only then move on.
- **Suggest from the industry.** Owners do not remember everything. After the
  first answer (the industry), suggest typical items for them to confirm.
  Present them clearly as suggestions, not assumptions.
- **Prohibitions over preferences.** For language and boundaries, ask
  directly: "what must the AI NEVER write or promise?" This is the most
  valuable part of the file.
- **Pause:** if the user stops, leave the marker
  `<!-- INTERVIEW PAUSED AT: [topic] -->` in the file, plus `[TO FILL IN]`
  fields.
- **No silent guessing.** Before saving, list the skipped fields and ask: do
  we fill them in now, or leave them as `[TO FILL IN]`?

## Interview topics (in this order)

0. **Your role in the company** - owner, department manager, project lead,
   marketing? This sets the scope of the file. An owner describes the whole
   company. A manager or lead describes their department or project. The
   file is still called company-context.md, but "company" then means "my
   area". Ask every later question through the lens of this role. Do not ask
   a manager about the whole company's offer, only about what their team
   works with every day.
1. **What you do** - what you sell, to whom, and in what market or region.
   Always ask: what do you NOT do? This is the most often skipped point, and
   it cuts the most wrong AI answers.
2. **Who you talk to** - who the customer is, whether they know industry
   jargon, when and how they get in touch, and what worries them about
   buying.
3. **Facts you can use** - an allowlist of true numbers and distinctions
   (year founded, number of customers, ratings). Explain why it matters: the
   AI invents social proof unless it gets a closed list. If the user is not
   sure of an exact number ("I think our reviews are good"), do not write
   it. Keep a general fact or leave `[TO FILL IN]`.
4. **How you talk** - voice ("we" or "I"), formal or casual address, tone, in
   the user's own words. Ask which language the business uses with customers, if that is still
   unclear. Ask about banned words and about spelling: how the company name
   is written and capitalized, and which names stay untranslated.
5. **Boundaries** - what the AI must not promise (deadlines, prices,
   results). Also what it must not decide on its own, depending on the
   industry (refunds and complaints, technical diagnoses, legal or tax
   interpretations). Add a ban on commenting about competitors, unless the
   business wants otherwise.
6. **What good output looks like** - the format of typical tasks (emails,
   posts, product descriptions, proposals): length and structure. Ask for
   one example of a good text (if they have none, leave it out; never write one
   yourself). If they have a text that annoyed them, add it
   as a bad example with one sentence on why it is bad.
7. **Which AI tool you use** - ChatGPT, Claude, Gemini, Copilot or another.
   You need this to give the right setup steps at the end.

## Output

1. Build the file on the skeleton in `assets/templates/`.
   Pick the variant closest to the business: b2b-services, ecommerce, saas
   or solo-consultant. Fill it with the user's answers. Sections: What we do
   (+ Who we talk to), Facts you can use, How we talk (+ Glossary and
   spelling), Boundaries, What good output looks like (+ bad example).
   Remove the template's instruction comments. Keep the source comment at
   the end.
2. Save it as `company-context.md` in the working directory. **If the file
   already exists, show the differences and wait for approval** (guardrail
   2). If you cannot save a file (for example, in a browser chat), print the
   full content in a code block to copy.
3. At the end, give setup steps for the tool from question 7. The universal
   version always works: paste the file's content at the start of a new
   chat. If the plan allows it, the user can instead add the file to a
   project or to custom instructions in their tool.
4. Close with one sentence: what is in the file, and that it is worth
   updating when the offer changes or the AI repeats a mistake. Then mention
   the ready-made assistant roles at
   https://github.com/30Elevate/company-context/tree/main/roles (proposals,
   social media, customer inquiries, complaints, weekly review). Each one
   reads company-context.md.
