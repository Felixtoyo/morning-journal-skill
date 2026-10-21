# 大富晨间日记 · Morning Journal Skill

**[中文说明 / Chinese documentation](README.zh-CN.md)** · [Skill instructions](SKILL.md)

A bilingual, nine-grid morning journal inspired by 佐藤传《晨间日记的奇迹》. 大富晨间日记 combines one-question-at-a-time reflection, authorized **On This Day** recall, health-data reuse, and optional verified Notion archiving.

## The nine grids

Read left to right, top to bottom:

| 1. Dreams / long-term goals | 2. Joy and gratitude | 3. Today's three most important priorities |
| --- | --- | --- |
| 4. Health | 5. Money | 6. Relationships |
| 7. Learning and input | 8. Worries / obstacles / improvements | 9. One sentence of self-encouragement |

This is a user-configured practice inspired by the book, not a reproduction of its exact original template. Its principle: morning journaling makes subconscious thoughts visible and aligns them with your goals, rather than simply logging events.

## Features

- Establishes your local journal date and timezone.
- Asks one question per turn in the fixed grid order; fills known information directly.
- Reuses supplied sleep, weight, and health observations with dates, units, measurement times, and sources.
- Accepts short answers, blank answers, skips, and stops; never invents missing content or pads priorities to three.
- Looks up earlier years' same month/day in an already-authorized journal archive before the interview. Verified matches get a short dated recap; successful empty queries proceed directly; failed reads never become “no history.”
- Keeps yesterday's review off unless you request it.
- Returns a clear nine-grid entry with the core principle.
- Saves to Notion only when authorized: checks the exact local date, updates existing entries, and reads the saved result back to verify.
- Works in chat without Notion. A journal request or history lookup alone does not authorize saving.

## Use

Download this repository and provide `SKILL.md` together with `reference/` to your skill-capable assistant. For local skill discovery, place them in a folder named `morning-journal` in the host's supported skills location. Paths and discovery behavior depend on the host; a GitHub repository alone does not install or activate a skill.

> Start my morning journal. Ask one question at a time and reuse the sleep data I already shared. Do not save to Notion yet.

> 开始大富晨间日记，复用我已经提供的睡眠和体重；有授权历史档案就先回顾往年同月同日，先不保存。

## Optional archive and Notion setup

Select your journal archive and authorize your assistant's supported integration to read it for On This Day. Without an authorized source, recall is skipped. No historical records are bundled.

For saving, connect Notion, grant access to your chosen destination, and request a save. The assistant inspects its actual schema and queries the exact local journal date before writing. One existing entry is updated within your request; multiple entries require clarification; a failed lookup prevents creation. A write is reported as successful only after content read-back verification.

See [history lookup rules](reference/on-this-day.md) and [Notion save rules](reference/notion-destination.md).

## Files

- [SKILL.md](SKILL.md): interview workflow and authorization boundaries.
- [README.zh-CN.md](README.zh-CN.md): complete Chinese guide.
- [reference/journal-format.md](reference/journal-format.md): fixed nine-grid output.
- [reference/on-this-day.md](reference/on-this-day.md): scoped historical recall and query outcomes.
- [reference/notion-destination.md](reference/notion-destination.md): duplicate checks, updates, and verification.
- [examples/example-session.md](examples/example-session.md): fictional interview and failure scenarios.

## Privacy and limitations

Keep credentials, private destination IDs, and personal health/journal records outside this public repository. Review what you send to Notion. This skill supports reflection, not medical advice. It provides no built-in health API, scheduler, or automatic synchronization. Duplicate checks require successful lookups and are not an atomic uniqueness constraint; avoid concurrent saves for the same date.

## Discoverability

大富晨间日记 · 晨间日记 · 九宫格晨间日记 · 晨间日记的奇迹 · 佐藤传 · Notion 晨间日记 · morning journal · nine-grid journal · On This Day · health-data reuse

## License

MIT — see [LICENSE](LICENSE).
