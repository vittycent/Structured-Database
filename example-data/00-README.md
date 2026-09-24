# Rootline example data set

_Built for the PMM Alliance session, 16 September 2026. Everything here is fictional: the company, the customers, the people, the numbers and the competitors. No real organisation is named anywhere._

**Everything in this folder happened in four weeks: 2026-W33 to W36, 10 August to 6 September 2026.** Today is the end of W36. Every recorded call took place inside that window, every export was pulled inside it, every survey was sent or compiled inside it, and every email thread was sent inside it. People refer to the past constantly, because that is how people talk, but nothing outside the window is itself a produced artefact — with one deliberate exception, a genuine historical churn notice in `10-email-threads/13-aalborg-food-group-churn-notification.md`, which explains itself.

Ten sources on the same fictional company, designed so that the same accounts appear across several of them and the versions do not always agree.

| File | Source | Size |
|---|---|---|
| `00-roster.md` | Master roster. **Build spec and answer key, does not ship** | 28 accounts with a call, 13 employees |
| `01-cohort-customers.md` | CRM export pulled 18 Aug, customers closed FY25, churn detail and a Q4 watchlist | 50 accounts |
| `02-deals-won-lost.md` | CRM export pulled 19 Aug, closed opportunities, picklist reason plus free text note | 10 won, 7 lost |
| `03-nps.md` | Relationship NPS, sent 11 Aug, closed 4 Sep | 46 responses, NPS +0 |
| `04-csat.md` | Transactional CSAT on onboardings and QBRs held in the window | 10 responses |
| `05-transcripts-sales/` | Sales call recordings | 22 calls, ~88,000 words |
| `06-transcripts-cs/` | Customer success calls | 20 calls, ~69,000 words |
| `09-internal-calls/` | Weekly pipeline reviews. **Internal. Not customer speech** | 3 calls, ~20,000 words |
| `07-slack-export.md` | `#kundfeedback` channel export, 10 Aug to 4 Sep 2026 | 14 messages, 33 thread replies |
| `08-testimonials.md` | Published testimonials and review site entries | 5 |
| `10-email-threads/` | Email correspondence extending or contradicting the calls | 18 threads, ~4,900 words |

## How the sources connect

Forty five recorded calls across four weeks, of which three are internal pipeline reviews, against three account executives, three customer success managers and two SDRs. That is a normal load for a company this size, and it is deliberately not a complete record: most conversations a company has are never recorded, and most accounts in the CRM never get a call worth keeping.

**Tenure is the axis, not time.** The sixteen customer success calls are sixteen different customers at different points in their life with Rootline: five onboardings for accounts that closed in the weeks just before the window, five check ins at three to six months, three quarterly reviews, two renewal reviews and one renewal decision. Nobody runs an onboarding and a quarterly review three weeks apart. Ask the same question at four tenures and the answer changes.

Three accounts appear at more than one stage, which is what makes progression readable: Vinga Sjömat at discovery and evaluation, Nordflor Brands at demo and procurement, Kärnhuset Group at data architecture and board feedback.

## The exports are already stale, on purpose

This is the single most important thing to understand before counting anything.

- `01-cohort-customers.md` was pulled on the 18th and covers contracts starting between July 2025 and June 2026. **Six live customers are missing from it** because they closed after that window, four of whom onboarded during these four weeks. It also still lists two accounts that have churned.
- `02-deals-won-lost.md` was pulled on the 19th. **Five deals in the current cycle closed lost after that date and are not in it.** Every one of them has a recorded call where the account executive says plainly why it went. The export's own picklist would tell you the company mostly loses to nothing in particular.

Anyone who answers a question from one export alone will get a number that was never true on any single day.

## What this is for

Running the extraction, clustering and messaging sequence from the session on a realistic pile rather than on one clean transcript. It is deliberately imperfect: stale exports, blank fields, untracked metrics, structured CRM fields that contradict their own free text notes, marketing language quoted back as customer language, internal calls that read like customer speech, and at least two conclusions that look obvious from one source and are wrong.

**`00-roster.md` and the frequency table in `../../internal/answer-keys/example-context-use-cases.md` are the answer key.** Keep them out of anything handed to attendees.
