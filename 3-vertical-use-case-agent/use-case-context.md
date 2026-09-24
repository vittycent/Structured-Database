# Use case context: Rootline

_Owner: PMM. Read by `/use-case-agent` on every run._

The six use cases Rootline already names and messages. Each one says what the use case is, the general patterns it shows up as, how customers tend to say it, and what it is not. The patterns are written for any food and beverage company, not for a named account, so the agent has to match them to the evidence in `structured-database.md` itself.

**For the agent.** A need in the database that fits one of these patterns is a served use case, not a candidate. A recurring need that fits none of them is where you look.

_Built 15 Sept 2026 from the six Section 1 headings in `structured-database.md`. Written without the planting spec and without the frequency table._

---

## 1. Answer the customer's scorecard before the deadline

**What it is.** A customer asks for carbon numbers on specific products, with a date attached, and the company has to send something back that will be accepted.

**How it shows up.**
- A retailer or brand owner adds a carbon section to a supplier questionnaire or annual review that already exists. The sustainability question is one column in a commercial spreadsheet, not a project of its own.
- A customer sends a list of named products and asks for a footprint per product by a set date. The list is usually a fraction of the full range.
- The request travels inside a commercial moment such as a range review, a tender or a contract renewal, so the date is tied to a listing or a deal rather than to a reporting year.
- It arrives informally first. A buyer mentions that numbers will be needed next year, with no template and no date, and nobody internally owns it yet.
- It lands on someone whose job is not sustainability: the quality manager, the key account manager, finance, or the managing director of a small company.
- The request has sat untouched for weeks because something operational came first, and the deadline is now close.
- The company already answered once with industry averages or estimates, flagged as indicative, and expects the next round to ask for more.
- The deadline turns out to be negotiable, and asking for more time is part of how the company copes.
- After the scorecard is answered, the customer stops asking and the company struggles to see what else the tool is for.

**How they say it.** "The form from our customer." "The scorecard." "The questionnaire." "Our biggest customer wants numbers on these products by the autumn." "We sent averages for now." "It's one tab in the supplier review."

**Not this.**
- Someone checking whether the number is right, such as an auditor, investor or board. That's use case 2.
- Being asked what to change to bring the number down. That's use case 6.
- A number printed on pack for consumers. That's in Asked for, not served.

---

## 2. Get a number that survives the auditor

**What it is.** Someone outside the sustainability team checks where a number came from, and the company has to show its working rather than just the total.

**How it shows up.**
- An auditor or assurance provider asks questions on method, data sources and emission factors, and the company needs answers in days rather than months.
- Last year's figure is restated as data improves, and the company has to explain the change line by line instead of letting it look like an error.
- A board, owner, investor or lender asks why the number moved. They want real operational change separated from better data and from a change in method.
- An emission factor database is updated and the numbers shift with nothing changed in the business, so the company needs to know which factor version sits behind each figure.
- A group and one of its entities hold two different numbers for the same thing, and nobody can say which one is right or why they differ.
- A consultant, a previous provider or a customer produces a different figure for the same product, and the gap has to be traced to a specific choice such as origin, factor or allocation.
- The current number lives in a static report the company cannot open up. Errors found in it wait for next year's version.
- Switching provider means historic activity data is lost or unusable, and the base year has to be reset.
- The company is preparing for its first audit or verification and has no record of who changed what and when.

**How they say it.** "Where does this number come from?" "Can we show our workings?" "Why did it go up when we didn't change anything?" "The auditors will ask." "We have a PDF, not a model." "I need to explain this to the board in five minutes."

**Not this.**
- Sending numbers to a customer for the first time against a deadline. That's use case 1.
- Asking which ingredient or input drives the footprint. That's use case 3.
- Wanting someone else to build and sign the first year's footprint for them. That's in Asked for, not served.

---

## 3. Find out which ingredient is actually the problem

**What it is.** The company wants to know which ingredients or inputs drive its footprint, and it is often surprised by the answer.

**How it shows up.**
- An ingredient that is a small share of volume or spend turns out to be a large share of the footprint.
- Something the company did not think of as the product, such as packaging, turns out to be as big as a main ingredient.
- The company assumed its footprint sat in what it controls directly, such as its own energy, factory or trucks, and finds most of it sits in what it buys.
- Across a range, a few products or recipes carry most of the footprint, and the company wants to see which ones before looking at the rest.
- A breakdown by ingredient is asked for on a single product, because the total alone doesn't tell anyone where to look.
- The question comes up the first time numbers land, often in the same meeting, as "so what is it that makes this so high?"
- A manager wants a ranked list of hotspots to decide where to spend the team's limited attention.

**How they say it.** "What's actually driving this?" "Is it the packaging or what's inside?" "I thought it would be our trucks." "It's a tiny part of what we buy." "Which products should we look at first?"

**Not this.**
- Comparing two suppliers of the same ingredient. That's use case 5.
- Deciding what to change once the hotspot is known. That's use case 6.
- Explaining why the total moved from one year to the next. That's use case 2.

---

## 4. Get data out of suppliers without burning the relationship

**What it is.** The company needs data from its own suppliers, and it has to get it without annoying the people it depends on for supply and price.

**How it shows up.**
- A request goes out to many small suppliers, such as farms, growers or boats, and only a small share answer.
- Someone senior guards the supplier relationship and treats every extra form as a cost to goodwill.
- Who sends the request decides whether it gets answered. A request from purchasing or a senior name gets a reply, and the same request from sustainability sits.
- Procurement stops or delays outreach it didn't approve, and the request has to be reworked around their timing, such as after price negotiations.
- The request rides on a contact that already exists, such as a delivery note, mandatory paperwork, a quarterly review or a visit, and gets far more answers than a request on its own.
- The wording is rewritten to sound less like a climate survey: shorter, signed by a known person, honest about the time it takes.
- The company doesn't know what to ask its suppliers, and some have never been asked anything beyond price, weight and quality.
- A middleman such as a mill, importer or wholesaler won't pass on details about the suppliers behind it.
- Suppliers say yes and never deliver, or refuse and call the data a trade secret.
- Data stalls on vague descriptions, such as a packaging material with no specification, and the company isn't sure whether fixing it is its job or the supplier's.
- The company wants to start with a handful of key suppliers rather than the whole supplier base.

**How they say it.** "I can't keep sending them forms." "They answer purchasing, not us." "I don't even know what to ask them." "We only know them from the invoices." "They said yes and never sent anything." "It has to come from someone they know."

**Not this.**
- The company being asked for data by its own customer. That's use case 1.
- Comparing suppliers once the data is in. That's use case 5.

---

## 5. Tell the difference between two suppliers of the same ingredient

**What it is.** The company sees that two suppliers of the same ingredient carry very different footprints, and has to decide whether that difference should matter in how it buys.

**How it shows up.**
- Two suppliers of the same ingredient turn out to be far apart, and the gap is found by accident, such as when someone sorts a list live in a meeting.
- A single supplier sources the same ingredient from different regions of the world, and the region makes a material difference to the emissions. The same supplier name can hide very different numbers.
- The lower footprint supplier is the more expensive one, and the conversation turns into whether the company should pay more to reduce a number.
- Purchasing buys on price, quality and security of supply. Carbon is not one of the criteria, and nobody has said what a tonne is worth to the business.
- Two buyers in the same company weigh the difference in different ways, because there is no shared rule.
- A switch only happens when the price is the same, so carbon works as a tiebreaker and nothing more.
- A lower footprint option is found and not used, because the customer's price point or specification locks in the current supplier.
- Purchasing wants the comparison in a form it already uses, such as a short ranked list in its regular supplier reviews, not a new login or screen it doesn't understand.
- A buyer or sourcing manager asks to see the numbers for their own suppliers, so the pull comes from purchasing rather than sustainability.
- Leadership wants to tell owners or the board which suppliers matter and what the options are.
- The difference comes up in a meeting, gets called political or sensitive, and nobody writes it down or follows up.

**How they say it.** "Same ingredient, and double the number?" "So you want me to pay more?" "We buy on price and quality." "What is a tonne worth to us?" "Just show me my suppliers, ranked." "If the price is the same, I'll switch."

**Not this.**
- Finding which ingredient drives the footprint in the first place. That's use case 3.
- Getting the data out of suppliers. That's use case 4.
- A plan for bringing the whole footprint down. That's use case 6.

---

## 6. Now tell me what to do about it

**What it is.** The footprint is measured, and the company now wants to know what to change, in what order and at what cost, to bring it down.

**For the agent.** Rootline names this use case, but the product answer is thin: reduction scenarios exist inside the core platform and are on the roadmap. Evidence here is a need Rootline already talks about and a product gap, not a messaging gap. Don't raise it as a new candidate.

**How it shows up.**
- The first footprint is finished, often a couple of quarters in, and the next meeting is about what to do with it rather than the number itself.
- Measurement is described as done and as not enough on its own. Knowing the number is not the same as reducing it.
- The company has a public target and wants to see where it stands against it and what closes the gap.
- A board or owner asks for a costed reduction plan by a set date, in a form they can read quickly, not a set of inputs.
- Reporting is described as a cost the business carries, while a plan is where the value is.
- Reduction planning is raised as a condition of renewal. The customer buys measurement now and says it will look elsewhere if nothing changes.
- A promised next phase or roadmap item has been mentioned more than once and not delivered, and "on the roadmap" is heard as "no".
- A competitor shows a reduction pathway or curve that leadership understands straight away, even if it is rough.
- The customer renews for one more year without reduction planning and says they'll run a proper process next time.
- The customer leaves for a competitor or consultant that gives them a plan, even one they know is not precise.

**How they say it.** "So what do we actually do?" "We know the number, now what?" "Where are we against the target?" "My board needs a plan, not a report." "On the roadmap means no." "What's it going to cost us to get there?"

**Not this.**
- Finding which ingredient drives the footprint. That's use case 3.
- Deciding between two suppliers of one ingredient. That's use case 5.
- Explaining a change in the total to an auditor or board. That's use case 2.
