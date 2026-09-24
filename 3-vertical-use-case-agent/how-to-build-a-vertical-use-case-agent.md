# How to build a vertical use case agent

_A method for finding use cases in a market you have not sold into yet, without inventing them._

---

## What this is

An agent that takes a vertical or sub-vertical you do not serve, reads your own customer evidence, reads outside research on that market, and tells you which of your proven customer needs would transfer there, which challenges native to that market you could serve, and which of your proven needs will break if you carry them across.

It runs in three gates with a human review between each, and it is built so that it can refuse.

The refusal matters more than it sounds. Point a capable model at a rich research file and an empty evidence base and ask it for use cases, and it will give you use cases. They will be well written, structurally complete, and entirely invented. The whole design below exists to stop that one thing.

---

## The prerequisite nobody mentions

**This only works if you already have a structured customer evidence base.** Not a CRM. Not a folder of call recordings. A file where every claim about a customer traces to a specific thing a specific customer said, on a date, with a link back to the source.

If you do not have that, build it first. The agent is a reader. It cannot be better than what it reads, and pointed at a pile of assertions it will produce confident assertions.

The minimum useful shape:

| Part | What it holds | Why the agent needs it |
|---|---|---|
| Account register | One row per account: vertical, ICP fit, and an **independence group** | So counts are of independent companies, not of rows |
| Observation log | One row per thing a customer said, with a source reference and the customer's own words | The source of truth. Everything else is a summary |
| Use case rollup | What came up, by week, with the observation IDs behind every line | So the agent can see what is already served |
| Pattern register | Things recurring across accounts, with a status ladder and thresholds | So the agent can tell a pattern from one loud customer |
| Counter evidence | Accounts that were asked and did **not** have the problem | Without this, every pattern drifts upward forever |
| Signals | Things that recur with nowhere to go yet, named in the customer's words | This is where undiscovered use cases actually live |

Two conventions carry more weight than the rest. **Count independent groups, not mentions**, because one account raising something in five calls is one account. And **keep a home for negatives**, because a file with nowhere to put a "no" will only ever get more confident.

---

## The three inputs

1. **The customer evidence base.** Above. Read-only to this agent, always.
2. **A served use case file.** The use cases you already name and message, each written as a general pattern rather than as a named account, so the agent has to match them to evidence rather than recognise a label. This is the "already covered" list, and it is what makes a candidate a candidate.
3. **A research file on the target market.** Written from outside sources, and written **blind to your customer data**, so that matching is the agent's job and not something already done for it.

The research file needs four safeguards, and they are what make the whole thing trustworthy:

- Outside sources only, each one named and dated, and only pages actually read.
- Written blind to the evidence base. No mapping section.
- **Your own topic gets no special weight.** Size topics by how much the market's own sources talk about them, not by how much you would like them to matter.
- A limits section saying what the file looked for and what it deliberately did not.

That third safeguard is uncomfortable by design. In our build, a 68 source research file on functional food and beverage contained the words carbon, emissions, footprint, climate and scope 3 exactly **zero** times, for a product that sells carbon accounting. That finding was worth more than any use case in the output.

---

## The gates

### Gate 0. Run type and evidence floor

Before anything else, three questions.

**Have I seen this vertical before?** If there is no output file for it, this is new, and the agent says so out loud:

> "This is a vertical I have not worked with before. I am going to apply the new-market process."

If there is one, it offers the additive run instead: look for more evidence on what is already recorded, rather than starting again. The two runs produce different things, and an agent that cannot tell them apart will keep rediscovering the same use cases and presenting them as new.

**What does the research file's own method allow?** Read its limits section first. Absence of a topic is evidence of low salience **only if somebody went looking for it.** A file that deliberately did not search for your topic cannot tell you your topic is absent from the market. Ours could not, and saying so was the difference between a real finding and an overreach.

**Is there enough evidence to proceed at all?** Resolve the industry onto an actual account set, count independent groups, and state the number. Below a floor, report the gap instead of producing output. A short honest answer beats a long invented one.

One practical trap here. Most evidence bases have a coarse vertical field and nothing finer. Ours had three values, and dairy, seafood and bakery existed only in free text notes. So the agent has to be told **how** to resolve an industry name onto accounts, and has to write the resolved list into its output. Leave it implicit and the account set quietly changes between runs, taking every count with it.

### Gate 1. Candidates

Three questions, and the third is the one that matters.

**What transfers?** A need proven in your evidence base, meeting a market condition confirmed in the research. Both halves required.

**What is market-native?** A challenge the research names that you could plausibly serve. No customer evidence behind it by definition.

**What breaks?** A proven need that will **not** hold in the new market.

That last question is the one everybody skips, and skipping it is the characteristic failure of this whole exercise. An agent that only finds matches is an agent that says yes to everything, and you cannot tell it apart from a working one by reading its output.

Our worked example: the second best evidenced pattern in the entire database was about collecting data from many small suppliers, where goodwill is the constraint and who signs the request matters more than how it is worded. It is proven, it is strong, and it does not transfer at all, because the target market buys from large industrial suppliers with sustainability functions instead of from farms and boats. Carrying it across would have produced confident, well cited, wrong positioning.

Then grade everything twice:

| Grade | Meaning | Gets positioning |
|---|---|---|
| **A. Transferred mechanism** | Proven need, confirmed market condition | Yes |
| **B. Market-native hypothesis** | Research only, no customer evidence | Yes, marked as hypothesis |
| **C. Breaks on transfer** | Proven here, will not hold there | No. Parked |

And grade **transfer strength separately from servability**. A need can transfer perfectly and still be one your product cannot serve. One of ours transferred on strong evidence and had near zero servability, because the regulation driving it was not about our product category at all. A single combined score would have buried that.

### Gate 2. Positioning

Dunford's components, in order, with two additions that do the real work.

1. **Competitive alternatives.** What they do today without you, including nothing. Label each as evidenced or inferred.
2. **Unique attributes.** Each tied to a specific observation. **State the known weaknesses of the same capability right here.** A positioning document that hides them survives until the first demo.
3. **Value and proof.** Name the proof points, and say which market they came from.
4. **Target market characteristics.** How to spot someone who cares a lot, **ending with a negative signal**: who looks similar and does not have this problem.
5. **Market category.** The highest leverage choice in the document, because it sets your comparison set and often your budget line. One of ours moved the buyer from sustainability to marketing and legal simply by being framed as claim substantiation rather than carbon accounting, which mattered because the evidence base showed there was no sustainability budget line to buy from.
6. **Relevant trend.** One line. Garnish.

Then: **what would falsify this.** Every entry closes with the condition under which the whole position is wrong. It takes one sentence and it is the only part that keeps the document honest as it ages.

Do one worked sample and agree the shape before running the rest.

### Gate 3. Messaging

Category, primary message, value proposition, two or three pillars with named proof, objections answered honestly, and the vocabulary to use and avoid.

Take the words to use from the market's own sources and from customer verbatims. Take the words to **avoid** from your Grade C breaks, because the language that works in the market you serve is usually exactly what marks you as an outsider in the one you do not.

---

## Why the breaks are kept

Parked, never deleted, and re-checked on every pass.

A break is not a dead end. It is a thing that is not true **yet**. Markets move, and you will point the agent at the same vertical more than once. Delete the breaks and you re-derive them every run, and lose the reason they were rejected the first time.

This is the same discipline as keeping counter evidence in the evidence base. Things climb a ladder as evidence accrues, and nothing is thrown away because it failed once.

---

## Validating it

**The validation run must be done by an agent that has never seen the answer key.**

If you are testing whether the agent can discover use cases you planted deliberately, then any agent that has read the planting spec will find them, report success, and tell you nothing. Hold the key outside the run and score from there. In our own build the author of the process had read the answer key earlier in the same session, which made a clean self-score impossible and had to be said out loud rather than worked around.

Build the answer key into the data with three grades: the thing named explicitly, the thing described in the customer's own words with the framework never named, and the thing recoverable only by joining two sources. Then include deliberate negatives: accounts where the use case is absent, and at least one account that looks like a match and is not. Without negatives you cannot tell a working agent from one that agrees with everything.

---

## What the output actually is

In a market where you have no customers, the output is a **discovery agenda**, not a messaging brief.

Grade A, the strongest grade available, means a proven mechanism meeting a confirmed market condition with zero customer evidence in the target market. That is a good hypothesis and a solid basis for going and asking. It is not proof, and a document that looks like a positioning deck will be read as proof unless it says otherwise on the first page.

Say it on the first page.

---

## The short version

| Design choice | The failure it prevents |
|---|---|
| Research is context, never evidence | Inventing customers out of market reports |
| An evidence floor that can refuse | Confident answers about markets you know nothing about |
| Read the research file's limits first | Concluding something is absent when nobody looked |
| Ask what breaks, not just what transfers | An agent that says yes to everything |
| Grade transfer and servability separately | Positioning for things you cannot sell |
| Park the breaks, re-check every pass | Re-deriving the same rejections forever |
| State the negative signal in every position | Targeting everyone who superficially resembles a buyer |
| Falsifier on every entry | Documents that quietly go stale and stay confident |
| Validate with an agent that has not seen the key | A test that always passes |

---

_Method developed 15 to 16 September 2026. The worked example throughout is a fictional carbon accounting company, built as teaching data._
