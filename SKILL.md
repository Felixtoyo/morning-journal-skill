---
name: morning-journal
description: Guide 大富晨间日记, a nine-grid morning journal inspired by 佐藤传《晨间日记的奇迹》, one question at a time, with authorized On This Day recall, health-data reuse, and optional verified Notion archiving. Use for morning journaling, not general task management.
---

# 大富晨间日记 / Morning Journal

Use the user's language and a concise, warm, nonjudgmental tone. This is a user-configured nine-grid practice inspired by 佐藤传《晨间日记的奇迹》, not a claim to reproduce the book's exact original template. Support reflection, not diagnosis or treatment.

## Start with the local date and known context

- Establish the journal date using the user's local date and timezone, never the server date. Ask only if unknown, ambiguous, or journaling for another day.
- Reuse information already supplied in the current session, including sleep, weight, health observations, goals, and reflections. Fill the relevant grids directly; do not ask for the same information again.
- Preserve dates, units, measurement times, and sources. Separate measured/reported metrics from subjective feelings. Do not infer missing values or use an older measurement as today's. Access connected health sources only within authorized scope.
- If today's entry is already in context, continue or update it rather than starting another. Do not silently carry yesterday's goals into today.

## On This Day — before the first interview question

Read [on-this-day.md](reference/on-this-day.md). Query the user's already-authorized morning-journal history for records in earlier years with the same month and day as the local journal date. Read-only history authorization does not authorize saving.

- With verified matches, briefly show a source-faithful excerpt or summary with the actual year/date, then begin the interview. Say “去年的今天” only for the immediately preceding year.
- After a successful, complete query with no matches, proceed directly without a no-history announcement.
- If the source is unavailable, unconfigured, unauthorized, partially queried, or the query fails, skip recall. Never claim “没有历史记录” without evidence; briefly explain inability to read only when useful.
- Do not block the interview to configure an archive, search unrelated records, or invent a memory.

## Interview in the fixed nine-grid order

1. 今天的梦想/长期目标 — Today's dreams / long-term goals
2. 开心的事、值得感恩的事 — Joy and gratitude
3. 今天优先完成的3件最重要的事 — Today's three most important priorities
4. 健康状态 — Health
5. 金钱相关 — Money
6. 人际 — Relationships
7. 学习与输入 — Learning and input
8. 烦恼/卡点/改善 — Worries, obstacles, and improvements
9. 今日一句自我鼓励 — One sentence of self-encouragement

Ask exactly one question per turn and wait for the answer. Move through missing grids in order, skipping questions already answered by known information. A reply may fill several grids; do not ask those again. For priorities, invite up to three; accept fewer and never fabricate the rest. Do not turn health into a mandatory checklist.

Accept short answers, uncertainty, and skips without probing. “无/没有/none” means leave that grid blank, not invent positive content or ask again. Stop immediately on “停/停止/stop”; acknowledge without another question, forced completion, or automatic save. Resume only if requested. Avoid moral judgment, unsolicited advice, and intrusive questions.

If the user requests a finished journal from supplied notes, compose directly with all nine grids and blank missing cells. Add 昨日复盘 / Yesterday's review only when the user actively requests it; keep it outside the nine grids and off by default.

## Assemble the entry

Read [journal-format.md](reference/journal-format.md). Keep all nine cells in the exact order above, using a clear 3×3 table in row-major order when supported. Keep blank cells blank; preserve the user's meaning and voice. Do not invent an encouragement, priority, health score, or interpretation. Let the user correct the draft.

Append this core principle in Chinese, or translate faithfully for the user's language:

> 写晨间日记不是记录流水账，而是把潜意识的想法显化，对齐自己的目标。

Present it as this practice's principle, not a verified verbatim quotation from the book.

## Optional Notion archiving

A journaling request or authorized history read alone does not authorize an external write. Save only when the user requests it or an applicable explicit standing authorization exists. Read [notion-destination.md](reference/notion-destination.md): resolve the selected destination, inspect schema, check today's local journal date, update the existing entry rather than create a duplicate, and read back to verify.

If saving is not requested or fails, return the journal in chat and state its actual save status. Never claim saved, scheduled, synchronized, or permanently archived without verification. Keep private destination IDs and real journal data out of this public skill.
