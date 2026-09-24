---
name: vertical-use-case-agent
description: Finds potential use cases and applications for a market the company has not sold into yet, by testing which proven customer needs transfer, which market-native challenges are servable, and which proven needs break on transfer. Gated: candidates, then Dunford positioning, then messaging, with an owner review between each. Use when the user asks to run the vertical use case agent, find use cases for a new vertical or sub-vertical, or explore a new market.
---

# Vertical use case agent

Finds **potential use cases and applications for a new market**. That is the primary job. The agent is pointed at a vertical or sub-vertical the company has not sold into, and asked what it could serve there.

## The one rule

**Research is context. It is never evidence about a customer.**

A finding in a research file can explain why a need shows up in the customer database, or sharpen the words used in positioning. It can never stand in for an observation, a proof point or a count. The failure this prevents: given a rich research file and a database with nothing to match it against, the path of least resistance is to generate use cases out of the research and dress them in positioning language. Every one is fiction, and fiction written in this format is very convincing.

Corollary: **a refusal is a valid answer.** If the evidence is not there, say so and stop. That is the agent working.

## Inputs and outputs

| | Path |
|---|---|
| Customer evidence, the source of truth | `~/Desktop/Claude/Projects/AI Workshops/Clients/PMA/Demo 16:09:2026/share/structured-database.md` |
| Served use cases, the "already covered" list | `.../share/use-case-context.md` |
| Sub-vertical research, owner-supplied | `.../share/research-subvertical-<slug>.md` |
| Output, one per vertical | `.../share/use-case-database-<slug>.md` |
| Design decisions behind this skill | `.../Demo 16:09:2026/internal/build/use-case-agent-design.md` |

**Never read.** `vertical-use-cases-fb.md`, `00-roster.md`, `account-portfolio.md`, and any file whose name contains `answer-key`, `planting` or `build-spec`. These are the answer key and the build specs for validating this agent. If the agent can read them the exercise is circular and proves nothing.

**Never write** to `structured-database.md`. Its own rules say every agent other than the weekly ingest agent may write nothing, and must not edit, tidy or reformat any table, including rollups that look stale. A stale rollup gets reported, not fixed.

## Procedure

### Gate 0. Run type and evidence floor

Run this before anything else. It is the gate that stops the agent answering a question it has no business answering.

**1. Ask which industry**, unless the user already named one.

**2. Decide the run type** by checking whether `use-case-database-<slug>.md` exists.

*No file. This is a new vertical.* Say so plainly, then proceed:

> "This is a vertical I have not worked with before. I am going to apply the new-market process: test which proven needs transfer, flag which market-native challenges are servable, and record which proven needs break on transfer."

*File exists. This vertical is known.* Offer the additive run instead:

> "I have worked this vertical before. Would you like me to look for additional evidence for the use cases already recorded?"

An additive run re-counts evidence for existing entries, checks the parked Grade C list for movement in either direction, and opens a new candidate only where genuinely new evidence supports one. It never rewrites an entry that has not changed.

**3. Read the research file's limits section first.** Every research file should say what it went looking for and what it deliberately did not. Absence of a topic is only evidence of low salience when somebody looked for it. Draw no conclusion from silence that the file's own method cannot support, and say which it is in the output.

**4. Resolve the industry onto an account set.** The database has no sub-vertical field. `Vertical` accepts only Ingredient producer, Multi brand owner and Off ICP. Dairy, seafood and bakery live only in free text register notes and in `Terms`. So:

- Read the account register and select accounts by register notes.
- Widen with a `Terms` search, because `Terms` holds the customer's own words.
- **Write the resolved account list into the output.** An unstated account set silently changes between runs and every count changes with it.

**5. Count coverage and state it.** Independent ICP groups, and observation rows. Then:

| Coverage | What to do |
|---|---|
| 5 or more independent ICP groups | Run evidence-led. The market is served; look for unserved needs inside it. |
| 1 to 4 groups | Run new-market. Say the coverage is thin and that findings are transfer-based. |
| Effectively none | Run new-market, and **lead the output with the gap**. State plainly that the database holds no evidence for this market and that nothing downstream is evidence-grade. |

Never pad a thin count into a strong one. Report the number.

### Gate 1. Candidates

Three questions, in this order.

**1. What transfers?** Take the needs proven in the database, the served use cases, the patterns and the signals, and test each against the market conditions in the research. A transfer needs both halves: a mechanism proven in the database, and a condition confirmed in the research.

**2. What is market-native?** Take the challenges named in the research and ask which the product could plausibly serve. These have no database evidence by definition.

**3. What breaks?** Take proven needs and ask which will **not** hold in the new market. This is the most valuable question and the easiest to skip. An agent that only finds matches is an agent that says yes to everything.

Grade every candidate twice.

| Grade | Meaning | Positioning and messaging |
|---|---|---|
| **A. Transferred mechanism** | Proven in the database, meeting a condition confirmed in the research. The strongest grade available in a market with no customers. | Yes |
| **B. Market-native hypothesis** | A real challenge in the research, no database evidence. | Yes, marked hypothesis-grade |
| **C. Breaks on transfer** | Proven here, and the research says the mechanism will not hold there. | **No.** Parked and re-checked every pass |

Then grade **transfer strength and servability separately**. A need can transfer strongly and still be one the product cannot serve. Collapsing them into one score hides this and produces confident positioning for things the company cannot sell.

Rules for this gate:

- **Cite observation IDs on every database claim.** A claim with no row behind it does not go in.
- **Count independent groups, not mentions or account IDs.** One account raising a thing in five calls is one account.
- **Check the `Recomputed as of` line** before quoting any status or count. If it lags the log, recount from the log or caveat plainly.
- **Read the counter evidence table.** It is where the negatives live, and negatives are what make a transfer test honest. Several of the most useful findings come from rows recorded as counter evidence.
- **Name what is out of scope.** Real challenges the product cannot serve are worth listing once so nobody chases them twice.

Stop. Show the candidate list and wait for the owner to keep, cut or redirect.

### Gate 2. Dunford positioning

Run only the candidates the owner kept, and only Grades A and B. Six parts, in this order, plus the falsifier.

| # | Part | The rule that makes it useful |
|---|---|---|
| 1 | **Competitive alternatives** | What they do today without us, including doing nothing. Label each one **database-evidenced** or **research-inferred**. Never a list of named vendors only. |
| 2 | **Unique attributes** | Capabilities, each tied to an observation ID or proof point. **State the known weaknesses in the same capability here.** A positioning document that hides them gets found out in the first demo. |
| 3 | **Value and proof** | The benefit the attributes enable, proof points named, and a plain statement of which market the proof came from. |
| 4 | **Target market characteristics** | How to recognise someone who cares a lot. **Always end with a negative signal**: who looks similar and does not have this problem. |
| 5 | **Market category** | The context that makes the value obvious. Highest leverage part, because it sets the comparison set and often the budget line. A category change can move the buyer and the budget at once. |
| 6 | **Relevant trend** | One line. Garnish, per Dunford. |
| | **What would falsify this** | Closes every entry. The condition under which the whole position is wrong. |

Do **one** worked sample first, show it, and get the shape agreed before running the rest.

Stop. Wait for the owner.

### Gate 3. Messaging

Only from approved positioning. Per use case: the category, a primary message, a value proposition, two or three pillars each carrying named proof, the objections with honest answers, and the vocabulary to use and avoid.

The vocabulary section is not decoration. Take the words from the research file's own "how they talk about it" material and from customer verbatims in the log. Take the words to **avoid** from the Grade C breaks, because the language that works in the served market is usually the language that marks you as an outsider in the new one.

If Gate 0 found the market's demand unverified, say so at the top: this is what you would say **if** discovery confirms the demand exists.

Stop. Wait for the owner.

### Write the output

`use-case-database-<slug>.md`, containing:

1. Run header: date, run type, the resolved account list, the coverage count, and what the research file's limits allow.
2. Grade A and B use cases with positioning and messaging.
3. **The parked Grade C list**, with the reason each one broke and the evidence behind it.
4. Out of scope, named once.
5. A discovery agenda: the questions that would move any of this from hypothesis to evidence.
6. A decisions log.

## Why Grade C is kept

A break is not a dead end. It is a thing that is not true **yet**. Markets move, the agent gets pointed at the same vertical repeatedly, and deleting a break means re-deriving it every run and losing the reason it was rejected.

This mirrors the customer database: negatives get a home, nothing is deleted, and things climb a ladder as evidence accrues. Every pass re-reads the parked list and reports movement in either direction. Grade C items never get positioning or messaging until they change grade.

## What the output is

In a market with no customers, the output is a **discovery agenda**, not a messaging brief. Grade A means proven mechanism plus confirmed market condition, with zero customer evidence in the target market. Say that in the document rather than letting the format imply more confidence than the evidence carries.

## Validating this agent

The validation run must be done by an agent that has **never read the answer key**. An agent that has seen the planted use cases cannot give a clean score on its own recall, and will produce a result that looks like success. Hold the key separately and score from outside.
