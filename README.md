# Structured database and vertical use case agent

Two things a product marketer can build from their own company's internal data, shown on one worked example.

1. **A structured database.** It turns a week of sales calls, customer success calls, email threads, surveys and CRM exports into patterns, signals, proof points and value claims, with every row traced back to the exact thing a customer said.
2. **A vertical use case agent.** It reads that database plus outside research on a market you do not sell into yet, and tells you which of your proven customer needs would transfer there, which of that market's own challenges you could serve, and which of your proven needs would break on the way across.

Everything here is fictional. Rootline, a carbon accounting company selling to food and beverage producers, was invented as teaching data, along with its customers, its people, its numbers and its competitors. No real organisation is named anywhere.

From the PMM Alliance session *Vertical messaging from internal data*, 16 September 2026. Victor Arellano.

## Where to start

You do not need to know GitHub. Click a folder to open it and a file to read it.

| Step | Open | Why |
|---|---|---|
| 1 | [`1-example-company/`](1-example-company/) | Who Rootline is, the four segments it sells into, and its buyers. Ten minutes. |
| 2 | [`example-data/00-README.md`](example-data/00-README.md), then one sales transcript and one customer success transcript | The raw material. The README explains how the ten sources disagree. |
| 3 | [`2-structured-database/structured-database.md`](2-structured-database/structured-database.md), starting at "How this file works" | What the data looks like after it has been read week by week. |
| 4 | [`3-vertical-use-case-agent/how-to-build-a-vertical-use-case-agent.md`](3-vertical-use-case-agent/how-to-build-a-vertical-use-case-agent.md) | The method behind the agent, so you can build your own. |
| 5 | [`3-vertical-use-case-agent/use-case-database-functional-food.md`](3-vertical-use-case-agent/use-case-database-functional-food.md) | One run of the agent, on a market Rootline has no customers in. |

## What is in each folder

| Folder | What it holds |
|---|---|
| `1-example-company/` | The company, its ICP, and its buying personas, with the quotes marked for whether a customer actually said them. |
| `example-data/` | Four weeks of Rootline's commercial record, 2026-W33 to W36. Ten sources: 45 call transcripts, 18 email threads, CRM exports, NPS, CSAT, Slack and testimonials. Both tools read from here. |
| `2-structured-database/` | The database with weeks 33 to 35 loaded, the same database with week 36 loaded on top, and the prompt that loads a week. |
| `3-vertical-use-case-agent/` | The method write-up, the agent itself (`vertical-use-case-agent/SKILL.md`), its two inputs (the use cases Rootline already serves, and outside research on functional food), and the output of one run. |

## Three ways to use it

**Read it here.** Every file is plain text, and GitHub shows it formatted.

**Download everything.** Press the green **Code** button at the top of this page, then **Download ZIP**.

**Run it with an AI tool.**

- *Load a week yourself.* Open [`prompt-load-week-36.md`](2-structured-database/prompt-load-week-36.md). It is a copy and paste prompt that works in any AI tool. Attach `structured-database.md` and the week 36 sources it lists, run it, and compare what you get with `structured-database-w36.md`.
- *Run the vertical use case agent in Claude Code.* Download this repository, copy the folder `3-vertical-use-case-agent/vertical-use-case-agent` into `~/.claude/skills/`, open Claude Code in the repository's top folder, and type `/vertical-use-case-agent`.
- *Run the agent in another AI tool.* Give it the contents of `SKILL.md` as its instructions, and attach `structured-database.md`, `use-case-context.md` and the research file.
- *Run either one on your own data.* Swap the file list for a week of your own: whatever carries a customer's voice. Calls, email threads, survey responses, CRM notes, a Slack channel. Keep the rules. They are the part that transfers.

## Before you run anything

- **The answer keys are not here, on purpose.** Use cases were planted in the data so that a run can be scored. The files that say what was planted are kept out, because a run that can read the answer proves nothing.
- **The data is messy on purpose.** The cohort export was pulled on the 18th and is missing six live customers. The won and lost export was pulled on the 19th and is missing five deals that closed after it. Anyone who answers a question from one export alone gets a number that was never true on any single day. That is the exercise.
- **The functional food run is unfinished.** It stopped partway through Gate 2, positioning. Gate 3, messaging, has not been run, so the messaging guidance in the method is the design, not a tested result.
- **Your run will not match the examples row for row.** Two honest passes over the same week disagree on wording and agree on findings. Compare the findings.

## The week 36 pair

Two versions of the same database are in `2-structured-database/` on purpose. `structured-database.md` stops at week 35. `structured-database-w36.md` has week 36 loaded: 221 more observations, a new pattern, a new signal, six new proof points, and every count in every register recomputed.

Compare them and you are looking at exactly what one week of a commercial team's work adds to the picture of a buyer: which patterns gained accounts, which status moved and on what count, what got asked for that nobody can sell, and which questions the week raised without settling.
