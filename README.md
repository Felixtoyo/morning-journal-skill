# Morning Journal Skill

A lightweight AI Skill for guided morning journaling, health-data reuse, and optional Notion archiving.

## Features

- One-question-at-a-time reflection in your preferred language.
- Reuses information you have already provided; never invents missing metrics.
- Separates health observations from subjective wellbeing.
- Optional Notion archiving with a daily duplicate check and read-back verification.
- Works as a text-only journal without a Notion connection.

## Use

Download this repository and give its `SKILL.md` and supporting `reference/` folder to your skill-capable assistant. For an assistant that discovers skills from a local directory, place the contents in a folder named `morning-journal` in its supported skills location. Installation paths and discovery behavior depend on the host application; a GitHub repository alone does not install or activate a skill.

Example request:

> Start my morning journal. Ask one question at a time and reuse the sleep data I already shared.

Or:

> 帮我写今天的晨间日记，一次只问一个问题，先不存 Notion。

## Optional Notion setup

Connect Notion through your assistant's supported integration, grant access to the destination you choose, and explicitly request saving. The assistant must inspect the actual schema and check for an existing entry on the same local calendar date before writing. No Notion connection means the assistant returns journal text without saving it.

This repository contains no credentials or private destination IDs. Keep your own configuration outside the public repository. Only connect health sources you want the assistant to use; there is no built-in health API, scheduler, or automatic synchronization.

## Files

```text
SKILL.md
README.md
LICENSE
reference/journal-format.md
reference/notion-destination.md
examples/example-session.md
```

## Privacy and limitations

Journal entries can contain sensitive personal information. Review what you ask your assistant to send to Notion. This skill is for reflection, not medical advice. Daily duplicate prevention depends on successful lookups and is not an atomic database constraint.

This v1.0.0 package was reconstructed from the agreed feature summary because the earlier ZIP was unavailable; it is not a byte-for-byte recovery of that archive. The example session is fictional.

## License

MIT — see [LICENSE](LICENSE).
