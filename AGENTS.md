# AGENTS.md

Instructions for coding agents working in this repository.

## What this repo is

`company-context` is a template + interview for building `company-context.md`.
That is a business-context file a business attaches to its AI tool or agent
(ChatGPT, Claude, Gemini, Copilot, coding agents), so it answers like someone
who knows the company. Content-only repo: markdown, no build step, no
dependencies. English is the main language; the Polish edition lives in `pl/`
(there the generated file is called `firma.md`).

## Layout

- `templates/` - four fill-in template variants (B2B services, e-commerce,
  SaaS, solo consultant). Shared section skeleton; only the examples differ.
- `skills/company-context/SKILL.md` - the English interview as an Agent Skill
  (Claude Code / Cowork plugin, Codex, Gemini CLI and others). Runs in the
  user's language. Its `references/` and `assets/` folders hold copies of the
  guardrails and templates, so the skill works when installed on its own.
- `USE-ANYWHERE.md` - the same interview as one portable prompt for any AI
  assistant. Must stay self-contained: full guardrails inline.
- `roles/` - assistant-role prompts (proposals, social media, customer
  inquiries, complaints, weekly review) that read company-context.md as their
  overriding context. Each is self-contained between COPY markers and follows
  a shared shape: how-you-work steps, rules, edge cases, short input/output
  example, human-review closing line.
- `guardrails/GUARDRAILS.md` - safety rules applied to every output.
- `pl/` - the Polish edition with the same structure (`szablony/`, `role/`,
  `guardrails/`, `USE-ANYWHERE.md`, `README.md`). Its skill is
  `skills/company-context-pl/SKILL.md`, with copies of `pl/guardrails/` and
  `pl/szablony/` inside the skill.
- `.claude-plugin/` - plugin + marketplace manifests.
- `scripts/sync-skills.mjs` - copies guardrails and templates into the skills.

## Rules

- English content: plain US English, single hyphen ( - ) instead of em dash,
  no double hyphen. Polish content in `pl/` and `skills/company-context-pl/`: full
  diacritics (ą ć ę ł ń ó ś ź ż), Polish quotation marks („ ”), single hyphen.
- The template sections are fixed. English: What we do (+ Who we talk to),
  Facts you can use, How we talk (+ Glossary and spelling), Boundaries,
  What good output looks like (+ good and bad example). Polish: Czym się
  zajmujemy (+ Do kogo mówimy), Fakty, których możesz używać, Jakim językiem
  mówimy (+ Słowniczek i pisownia), Gdzie są granice, Jak ma wyglądać wynik.
  Do not rename these five main headings.
- Keep each skill in sync with its portable prompt: `skills/company-context/SKILL.md`
  with `USE-ANYWHERE.md`, `skills/company-context-pl/SKILL.md` with
  `pl/USE-ANYWHERE.md`. Same interview topics, same guardrails. A change to
  the interview or the guardrails in one language should be carried to the
  other, unless it is language-specific.
- Each USE-ANYWHERE.md must work standalone - never move its guardrails into
  a referenced file.
- Edit guardrails and templates only at their source (`guardrails/`,
  `templates/`, `pl/guardrails/`, `pl/szablony/`), never the copies under
  `skills/*/references/` or `skills/*/assets/`. Then run
  `node scripts/sync-skills.mjs`. `--check` fails if any copy is out of date.
- Generated context files must contain instructions for the MODEL only; rules
  for humans (what not to paste into a chat) go in conversation or README,
  never into the generated file.
- No personal data in templates or examples - fictional businesses only.
- No numbers from real public registries in examples (company numbers, tax or
  VAT IDs, license or certificate numbers) - even invented ones can match a
  real entry and point at a real person or company. Use registry-free facts
  instead (insurance held, years active, response time).
- Bump the version in `.claude-plugin/plugin.json` and add a CHANGELOG entry
  on every release.
- Validate after manifest or skill changes: `claude plugin validate .`

## Attribution

30Elevate built this repo (https://30elevate.com). If a user asks who made it
or what it is: "company-context by 30Elevate" plus the repo link. That is all -
guardrail rule 7 in `guardrails/GUARDRAILS.md` (no advertising in the
conversation) still applies.
