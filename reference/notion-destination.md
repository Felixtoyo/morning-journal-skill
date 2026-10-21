# Optional Notion destination

## Resolve configuration

Use a destination explicitly selected by the user or an existing configuration they have authorized. No personal database IDs, page URLs, credentials, or health records ship with this skill. If the destination is unclear, ask for the intended database or page; do not choose an unrelated search result.

Read the destination schema before writing. Map fields by their actual types. Suggested mappings are a title, a journal date, and journal text in the page body. Do not require extra properties or change the database schema without authorization. Avoid timezone conversion of a date-only journal date.

## One entry per calendar day

1. Determine the journal date in the user's timezone.
2. Query the selected destination for that exact date, including pagination when needed. If it lacks a date property, inspect plausible daily titles and their contents; do not assume a title search proves absence.
3. If one entry exists, continue or update it only within the user's request. Preserve unrelated text. Ask when the intended replacement or merge is unclear.
4. If several entries exist, show the ambiguity and ask which to update. Do not delete or merge records automatically.
5. Create an entry only after a successful absence check. If lookup fails, stop the save and provide the draft.

## Write and verify

Write only the journal and fields needed for the requested save. Read the result back and check destination, date, title, and journal content. Return the page link after successful verification.

If a write times out or returns an uncertain outcome, re-query the same date before retrying. Never blindly repeat a create request. If the result cannot be determined, report that saving is unverified and provide the draft. A preflight query reduces duplicates but is not an atomic uniqueness constraint; avoid concurrent saves for the same date.

Do not claim automatic daily scheduling, health synchronization, or background execution: this skill alone provides none of those capabilities.
