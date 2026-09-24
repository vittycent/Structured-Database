# Prompt: load week 36 into the structured database

From the PMM Alliance session, *Vertical messaging from internal data*, 16 September 2026.

This is the prompt behind the live demo. Copy the block below into your own AI tool and run it against the files in this pack. It takes one week of a company's raw commercial record and turns it into rows in a database that anything downstream can read.

## Before you run it

You need three things open or attached:

1. `structured-database.md`, the database as it stands with weeks 33 to 35 loaded. This is the input.
2. `example-data/`, the raw sources. Week 36 is 31 August to 6 September 2026.
3. Your own AI tool. Any of them. This is not a prompt that depends on a particular model.

The sixteen week 36 sources are listed inside the prompt so nothing has to be guessed.

**Do not attach `00-roster.md`.** It is the answer key for how this data set was built, it is not in this pack, and a run that reads it proves nothing.

## What you should get

A week 36 column in every rolling table, about two hundred new observation rows, and every count in every register recomputed from those rows rather than typed. `structured-database-w36.md` in this pack is one finished version, so you can compare. Yours will not match it row for row and it is not supposed to. Two honest runs over the same week disagree on wording and agree on findings. Compare the findings.

## Running it on your own data instead

Swap the file list for your own week: whatever carries a customer's voice. Calls, email threads, survey responses, CRM notes, a Slack channel. Keep the rules. They are the part that transfers.

---

## The prompt

```
You are loading one week of customer evidence into a structured database.

## Your inputs

1. `structured-database.md`. Read it first and read all of it, especially the
   section called "How this file works". It states the rules this file is
   governed by and they override anything you would otherwise do by habit.
2. The sources for 2026-W36, which is 31 August to 6 September 2026:

   Sales calls
     example-data/05-transcripts-sales/02-vretstorp-konserv-technical-deep-dive.md
     example-data/05-transcripts-sales/05-vinga-sjomat-evaluation-call.md
     example-data/05-transcripts-sales/12-karnhuset-group-board-feedback-call.md
     example-data/05-transcripts-sales/14-handelsbolaget-nord-own-brand-session.md
     example-data/05-transcripts-sales/19-hedlunds-bageri-loss-debrief.md
     example-data/05-transcripts-sales/22-nordflor-brands-negotiation-and-close.md
     example-data/05-transcripts-sales/23-klaralven-kvarn-discovery.md

   Customer success calls
     example-data/06-transcripts-cs/03-nordvik-dairy-qbr.md
     example-data/06-transcripts-cs/04-lysekil-konserv-onboarding.md
     example-data/06-transcripts-cs/09-kallvatten-renewal-review.md

   Internal
     example-data/09-internal-calls/03-pipeline-review-w36.md

   Email threads
     example-data/10-email-threads/04-vinga-sjomat-klimatly-comparison-question.md
     example-data/10-email-threads/06-nordflor-brands-legal-redline-dpa.md
     example-data/10-email-threads/09-hedlunds-bageri-break-up-email-and-reply.md
     example-data/10-email-threads/11-bergstrand-group-renewal-correspondence.md
     example-data/10-email-threads/18-klaralven-kvarn-inbound-scorecard.md

   Structured sources, week 36 rows only
     example-data/03-nps.md          responses dated 2026-08-31 to 2026-09-04
     example-data/04-csat.md         the two responses marked 2026-W36
     example-data/07-slack-export.md the threads under the 2026-W36 heading
     example-data/02-deals-won-lost.md  the note added 2026-09-04 only

## Never read

Any file that is a build spec or an answer key, including anything named
roster, planting or build-spec, and any file that tells you in its own header
that it does not ship with the data. If you can read the answer, the exercise
proves nothing.

## The rules that matter most

These are in the database already. They are repeated because they are the ones
that get broken.

- Append only. Nothing already in the file is edited, reworded or deleted.
- One idea per row. A row holding three ideas gets clustered wrong by whatever
  reads it next.
- Their words, not ours. Verbatim goes in double quotes. Anything not in quotes
  is a paraphrase and must never later be presented as a customer quote.
- Every row carries a source ref: the file path plus a timestamp or a date. A
  row with no source ref is not a valid row.
- Every row reaches at least one summary. A row that reaches none is invisible.
- Controlled fields take only the listed values. Propose a new value, never coin
  one silently. No blanks in controlled fields: write unknown or not applicable.
- Voice is customer or relayed. Anything one of our own people says about a
  customer, including deal notes, internal calls and Slack, is relayed. It
  counts like any other row and is never quoted externally as a customer quote.
- Buying stage is where the account was when the thing was said, not where it is
  now.
- Count accounts, not mentions. Count distinct independence groups, not distinct
  account IDs. Only ICP accounts move a status.
- Do not move a status by feel. Recount from the observation log and apply the
  written criteria. If a rollup and the log disagree, the log wins.

## Work in four gates. Stop at each one and wait.

GATE 1. Coverage and accounts.
  List every source you reviewed, whether or not it produced anything, as rows
  for the coverage log. Add any new accounts to the account register and
  classify ICP fit now. Say explicitly which existing account rows need
  correcting and why. Flag any account that may not be independent of another:
  same parent, same adviser, same consortium, or the same person involved in
  both. Do not guess independence. Raise it.
  Then stop and show me the coverage rows and the register changes.

GATE 2. Observations.
  Append one row per thing a customer said, in the observation log's exact
  column order, IDs allocated in sequence from the Next IDs line. Tag use case,
  pattern, insight, proof, pressure and signal only where the row genuinely
  belongs. Leaving a tag blank is correct and common. A row with a pattern
  carries no signal.
  Then stop. Tell me how many rows you produced per source, and name any source
  that produced none.

GATE 3. Recount, do not retype.
  Recompute every register from the observation log: the pattern register and
  its evidence index, the signals table, the pressure register and its evidence
  index, and the computed evidence status in the value claims table. Show your
  working for any status that moved, as a count against the written criteria.
  Open a new pattern only where two or more independent accounts describe the
  same behaviour. Open a new signal only where two or more independent accounts
  keep saying the same thing and it has no use case, pattern or pressure to go
  to. Name a signal in the customers' words, never after a framework, a
  regulation or one of our own product modules.
  Then stop and show me every count that changed and every status that moved.

GATE 4. Summaries and the write up.
  Fill the new week's column in the use case table and in each insight table.
  Every bullet ends with the account ID and the observation IDs it was written
  from. Close each cell with a line listing the rows in that cell no bullet
  summarises. Update the metadata block, the Next IDs line, every
  "Recomputed as of" line, and the decisions log.
  Anything you could not resolve goes in Open for the owner, with the evidence
  and what it would change either way. Do not resolve an ambiguity silently.

## What I will judge this on

Not how much you wrote. Whether I can take any claim in a summary, follow it to
a row, follow that row to a timestamp in a transcript, and find the customer
actually saying it.
```

---

## Why the prompt looks like this

Three things in it do most of the work, and they are the parts worth stealing.

**The gates.** Four stops with a human in between. A single prompt that goes from raw transcripts to a finished document in one pass produces something that looks right and cannot be checked. The stop after the observations is the one that matters: if the rows are wrong, everything downstream is confidently wrong.

**Recount, do not retype.** The most common failure is an agent carrying a number forward because it was in the file last week. Every count in the finished database is derived from the rows underneath it, which means anybody can recompute it and catch a lie.

**Do not resolve an ambiguity silently.** The interesting output of a week is often the thing the data cannot settle. A run that quietly picks an answer hides exactly the question you needed to see.
