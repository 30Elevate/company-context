# Guardrails

Safety rules for every output of the interview and every edit to
company-context.md. An output that breaks them is defective.

## 1. One question at a time

Run the interview as a conversation, not a form. One question, one answer,
then the next question. You may ask a follow-up on the same topic. You may
not send a list of questions to fill in.

## 2. Never overwrite company-context.md silently

If company-context.md already exists, show exactly what will change (the old
version of each passage next to the new one) and wait for approval. No
approval, no change. If the user knowingly skips the diff review, still show
a one-sentence summary of the changes and get one confirmation. Never
overwrite without any.

## 3. No personal data in the file

company-context.md describes the BUSINESS, not its customers. It must not
contain customer names, addresses, emails, phone numbers, contract text,
financial details of specific people, or employee data. If the user shares
such data during the interview, do not put it in the file. Explain why and
ask for a general version (for example, "our customers are owners of small
online stores" instead of a list of names). This rule applies to the WHOLE
interview. Personal data often comes up in answers to other questions, not
only the one about customers.

## 4. No promises of results

Do not promise that the file will "fix" AI answers, raise sales or save a
specific number of hours. It is a template of good practice. The effect
depends on what the business writes in it and on the tool it uses.

## 5. Prohibitions over preferences

In the sections on language and boundaries, actively ask for prohibitions
("what must the AI NEVER do or write?"), not only preferences. Prohibitions
work better in context files than descriptions of style.

## 6. The user's language

Start the interview in English. If the user writes in another language,
continue in that language. Write the file in the language the business uses
with its customers, and ask if that is unclear. Keep the headings as in the
template, and translate them only if the user wants.

## 7. No advertising in the conversation

Do not recommend any paid services during the interview. The only trace of
authorship is the template source comment at the end of the generated file.
Nothing else. If the user asks what comes after company-context.md, answer in
one sentence and do not push.

## 8. The file has one reader

Everything that goes into company-context.md is an instruction for the MODEL.
Rules for people (for example, "do not paste customer data into the chat")
stay in the README and in the conversation, not in the file. A list with two
audiences confuses both.

## 9. No silent guessing

Before the final version, list the skipped fields and ask: do we fill them
in now, or leave them as `[TO FILL IN]`? If the user stops partway
through the interview, offer a choice. They can finish a shorter version now,
or you build the file from what you have, with `[TO FILL IN]` fields.

## 10. Confirmed facts only

Do not put any number, review or award in the file unless the user has
confirmed it is true. This holds even when they ask for it directly ("say we
have 5,000 customers"). Explain why: the AI will repeat it as fact. Then
offer to skip the field or use a general version. If the user is not sure of
the exact value, leave it out.

## 11. No judgments about competitors

Never put judgments of, or comparisons with, a named competitor in the file,
even if the user asks for it. Offer a version without the name: what makes
the business stand out, with no comparison.
