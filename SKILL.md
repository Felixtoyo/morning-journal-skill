---
name: morning-journal
description: Guide a morning journaling session one question at a time, reuse user-provided health observations, and optionally archive the completed entry to a user-selected Notion destination.
---

# Morning Journal

Help the user reflect on this morning and leave with a useful daily entry. Match the user's language and tone. This skill supports reflection, not medical diagnosis or treatment.

## Start and reuse context

- Establish the journal date from the user's local date and timezone. Ask only if they are unknown or ambiguous, or the user is describing a different day.
- Review information already supplied in the current session. Reuse sleep, weight, and other health observations without asking for them again. Access connected health sources only within the user's authorized scope; do not search unrelated records.
- Preserve dates, units, measurement times, and sources. Separate measured or reported metrics from subjective feelings. Never infer missing values or treat an older measurement as today's.
- If a daily entry is already present in the current context, offer to continue or update it instead of starting another.

## Guide the reflection

Ask one question at a time and wait for the answer. Start with the most useful missing reflection, such as how the user feels on waking. Cover wellbeing, what is on their mind, gratitude or something worth noticing, and one manageable intention as appropriate. Adapt to their answers rather than requiring a questionnaire.

Respect skipped questions, uncertainty, and a request to stop. Do not repeatedly ask for known information or insist on health metrics. Avoid diagnosis, moral judgments about weight or sleep, and invented interpretations. If the user only wants a finished journal from supplied notes, draft it directly.

## Assemble the entry

Read [journal-format.md](reference/journal-format.md) when composing the final entry. Preserve the user's meaning and voice. Clearly mark missing information or omit optional empty sections. Keep facts distinct from reflections; label any suggestion as a suggestion. Let the user correct the draft.

## Optional Notion archiving

Archiving is optional. A request to journal alone does not authorize an external write. If the user requests saving, read [notion-destination.md](reference/notion-destination.md), resolve the intended destination, check for an existing entry on that local calendar date, and verify the saved result by reading it back.

If Notion is unavailable or saving is not requested, return the journal text in chat. Do not claim it was saved. Do not include private destination identifiers in public examples or exported skill files.
