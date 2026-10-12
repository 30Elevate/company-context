# Changelog

## 0.2.2 - 2026-10-12

- The interview starts in the language the user wrote in. Before, the rules said "start in English" while the header said "in the user's language", and the assistant had to pick one.
- No example of good text from the user: the line is left out and the assistant never writes one itself. Tone is recorded in the user's own words, not the assistant's characterizations.
- When the file is not in English, the assistant offers to translate the headings.
- Found by running `USE-ANYWHERE.md` end to end on two assistants outside Claude.

## 0.2.1 - 2026-10-10

- Skills renamed to English, branded names: `interview` is now `company-context` (`/company-context:company-context`) and `wywiad-firma` is now `company-context-pl` (`/company-context:company-context-pl`). A generic name such as `interview` clashes with other skills once installed into a shared skills folder.
- Both skills now work when installed on their own, outside the plugin: each carries copies of its guardrails (`references/`) and templates (`assets/`), and refers to them by paths relative to the skill. Before, an agent that installed only the skill folder lost the guardrails and the templates.
- New install path for Codex, Gemini CLI and other agents that read Agent Skills: `npx skills add 30Elevate/company-context --skill company-context` (Polish: `--skill company-context-pl`).
- `scripts/sync-skills.mjs` keeps the copies in step with the source files (`--check` to verify).
- The interview links to the assistant roles on GitHub, because an installed skill does not include the `roles/` folder.

## 0.2.0 - 2026-10-10

- Renamed from firma-md to company-context. GitHub redirects the old repo URL.
- English is now the main language: new interview skill (`/company-context:interview`), portable prompt, guardrails, five assistant roles and four templates (B2B services, e-commerce, SaaS, solo consultant). The interview follows the user's language.
- The Polish edition moved to `pl/`. Its skill keeps the name `wywiad-firma` and now reads templates and guardrails from `pl/`.
- AGENTS.md rewritten for the two-language layout. The Polish skill now lists all five roles.
- Gemini note updated: Google is converting Gems into Skills from 17 November 2026.

## 0.1.0 - 2026-08-13

- First public release as firma-md (Polish).
