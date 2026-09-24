# Use case database: functional food and beverage

_Output of `/vertical-use-case-agent`. One file per vertical. Re-read on every later run of this vertical._

**Status. Paused after Gate 2, partway.** Gate 0 and Gate 1 done and reviewed. Gate 2 positioning written for A-1 (shape approved) and A-2 (presented, owner stopped the run before reviewing it). A-3, A-4 and A-5 not yet positioned. Gate 3 messaging not started for anything. Resume point at the bottom.

---

## 1. Run header

| Field | Value |
|---|---|
| Date | 16 Sept 2026 |
| Run type | **New vertical.** No earlier output file existed. New market process: what transfers, what is market native and servable, what breaks. |
| Customer evidence | `structured-database-w36.md` (2026-W33 to 2026-W36), chosen by the owner for this run over `structured-database.md` (W33 to W35) |
| Rollup freshness | Every `Recomputed as of` line reads 2026-W36, matching the last week in the log. Nothing stale. |
| Research file | `research-subvertical-functional-food.md` (15 Sept 2026, leakage read 16 Sept) |
| Served use cases | `use-case-context.md` |
| Resolved account set | **None.** See below. |
| Coverage | **0 independent ICP groups, 0 observation rows.** |
| What this output is | A discovery agenda. Nothing here is evidence grade. |

### Lead with the gap

The database holds **no evidence about functional food customers**. Every candidate in this file is a need proven in other food segments and carried across. Grade A means a mechanism proven elsewhere meeting a market condition confirmed by the research, with zero customer evidence in this market. Read every position below as what we would test, not what we know.

### What the research file's limits allow

- **Sustainability was sized small on purpose** (Part 9). Only EUDR and passing mentions were kept, and nothing further was searched. Silence on carbon demand in functional food is therefore **not** evidence of low salience. Nobody looked.
- Consequence: **no candidate can have a confirmed carbon demand condition.** The conditions confirmed below are structural only: supply, regulation, manufacturing, margins.
- Part 6 (software and data) leans on vendor surveys. Read as direction of travel, not measured need.

### Account resolution

The database has no sub vertical field. Accounts were selected by register notes, then widened with a `Terms` and full text search.

| Account | Considered because | Why it is out |
|---|---|---|
| `greenpulse-nordic` | Register: "Plant protein" | An input supplier to the category, not in it. One row, an NPS comment on trust (O-0445), nothing about the problem. |
| `proteinfabriken` | Name only | Register says "Other ingredients". 0 rows. |
| `artriket` | Name only (pea) | Register silent on product. 2 rows, both investor diligence (O-0114, O-0255). |
| `havreland` | Name only (oat) | Register silent. 0 rows. |
| `kallvatten`, `saftkallan`, `bryggeri-kvarnen`, `nordic-brew-collective`, `falkenberg-bryggeri` | Beverages | None functional. |

**Search result.** 0 hits for whey, kvarg, skyr, energy drink, caffeine, GLP, fibre, gut, reformulation, novel food, health claim, sports. The 5 hits for "protein" are milk protein payment (O-0567) and ready meal protein suppliers (O-0381).

### Reported, not fixed

- The observation log is **680 rows**. The database's own rule says the log should move to its own file at about 300. This run read every register, index and rollup in full and pulled log rows by targeted search. It did not read all 680 rows in sequence.
- Nothing was written to either structured database.

---

## 2. Grade A and B use cases

### Candidate summary

Transfer strength and servability are graded separately. A need can transfer strongly and still be one the product cannot serve.

| # | Use case | Transfer | Servability | Gate 1 | Gate 2 | Gate 3 |
|---|---|---|---|---|---|---|
| A-1 | A forced change of origin | Medium | High | Approved | **Written, shape approved** | Not started |
| A-2 | A brand with no factory | Strong | Medium | Approved | **Written, not yet reviewed** | Not started |
| A-3 | A claim to defend | Strong on how they buy | Low | Approved | Not started, blocked on the market question | Not started |
| A-4 | Whey's footprint moves with its price | Medium | High for dairies, medium for brands | Approved | Not started, blocked on the market question | Not started |
| A-5 | EUDR on cocoa and coffee | Medium | Low | Approved | Not started | Not started |
| B-1 | One record per product of ingredient, origin and supplier | n/a | Low | **Cut** (recommended, not approved) | n/a | n/a |

---

### A-1. A forced change of origin

**Grade A.** Transfer medium, servability high.

**The candidate.** Duties and supply limits are forcing buyers to replace a protein source. Carbon can ride along with a switch that is already happening. It will not decide whether to switch.

- **Database mechanism.** Carbon moves purchasing only at equal price: "the price was the same so I took the better one" (O-0399, V-17), "If it had cost more he would not have" (O-0400). Nobody has put a price on a tonne (P-11, `new`, 4 groups).
- **Research condition.** EU provisional duties of 40.5 to 67.4% on Chinese pea protein (R-19). Lantmännen's Swedish pea and faba isolate plant, due 2027 (R-20). Vega moved pea sourcing after lead findings (R-22). Caseinates used as a whey alternative (R-16).

#### Positioning

_Hypothesis grade. No functional food customer evidence._

**In one line.** When a buyer has to replace a protein source and more than one alternative sits at a similar price, carbon can decide which alternative wins. It won't decide whether to switch.

**1. Competitive alternatives**

| What they do today | Label |
|---|---|
| Nothing. Buy on price, quality and security of supply. "Carbon is not in their world at all" (O-0097). "Carbon is one line out of about twenty and I do not think it moves anything" (O-0079). | database evidenced |
| Switch on duty or contamination alone (R-19, R-22). | research inferred |
| A spreadsheet price comparison plus supplier certificates of analysis. "Nobody has ever given me that" (O-0475, unclassified account). Certificates of analysis per CH-05. | database evidenced (weak) plus research inferred |
| A spend based tool. "It just took our spending by category" (O-0071). It cannot see origin. | database evidenced |
| The supplier's own figure. Supplier factors "Mostly unopened" (O-0004, off ICP). | database evidenced (weak) |

**2. Unique attributes**

| Attribute | Evidence | Known weakness in the same capability |
|---|---|---|
| Separate footprints for one ingredient by origin | A 15% gap on a cheese line "almost entirely explained by the origin resolution" (O-0319). C-04 evidenced by V-03, V-05, V-17. | All evidence is cheese, cod, haddock, starch and chilli. **Unverified whether the factor library separates pea or whey isolate by origin and process.** For processed protein fractions, factory energy may matter more than origin. |
| An answer purchasing can use without filling anything in | "If it asks me to fill anything in, I will not" (O-0477). "One page a quarter showing their own suppliers ranked" (O-0087). Usable in a procurement director's "own team meeting" (O-0298). | P-08 (`new`, 3 groups): the supplier screen opens alphabetically and hides the difference (O-0088, O-0095). "I do not understand what I am supposed to do with this screen" (O-0331). |

**3. Value and proof**

- **Value.** The buyer is switching anyway. Among alternatives at similar prices, they pick one with a documented footprint difference, and the decision is on record.
- **Proof.** V-17: a purchasing manager moved 60% of a starch volume unasked (O-0399). V-27: 431 suppliers reduced to 12 covering 68% of the footprint (O-0616).
- **Honest size.** "If it had cost more he would not have" (O-0400). The move was "about one point one percent of the group footprint" (O-0401).
- **Which market the proof came from.** Nordic multi brand owners, on starch and a general supplier base. None from functional food, none on protein.
- **External use filter.** 4 proof rows checked, 3 excluded: V-03 `not delivered`, V-05 `partial`, V-17 shareable `unknown`. **Only V-27 can be used externally**, and it is about supplier coverage, not origin. Clearing permission on V-17 is the most useful single chase.

**4. Target market characteristics**

- Buys plant protein isolate or concentrate in volume, and is re-sourcing away from China on duties (R-19) or contaminant findings (R-22).
- Has at least two qualified alternatives at similar prices: European, North American, or Swedish from 2027 (R-20).
- A sourcing manager owns the decision through a tender or supplier review (the database pattern: O-0399, O-0475).
- Above the ICP size floor.
- **Negative signal.** Whey based brands look like the same buyer and are not: locked into forward contracts with no choice of supplier (C-2). Also brands whose customer specification or price point locks the supplier (V-21, O-0392), and any buyer whose remaining alternatives stay far apart on price after the duties.

**5. Market category**

**A sourcing comparison used inside the tender, on the procurement budget, not a carbon accounting tool.** This moves the comparison set from Verdanta and Klimatly to a spreadsheet price comparison, and moves the budget away from a sustainability function the research cannot show exists. Evidence for the move: S-06 "New lines never come off again" (5 groups, O-0132) and O-0477.

Weakness: Rootline does not sell a procurement only offer. The nearest thing is Tre Kronor's read only login.

**6. Relevant trend**

Supply chains shortening (69% of executives, R-52), EU pea duties from April 2026 (R-19), Swedish pea isolate capacity in 2027 (R-20).

**What would falsify this.** The alternatives to Chinese pea protein turn out far apart on price, so carbon never breaks a tie. Or switch decisions for 2027 are locked before anyone asks about carbon. Or purchasing at functional brands ignores carbon even at equal price (the one database case sat inside a group with a sustainability function). Or the factor library cannot separate protein isolates by origin.

---

### A-2. A brand with no factory

**Grade A.** Transfer strong, servability medium.

**The candidate.** The recipe and process data sit with R&D or the contract manufacturer, and in this market they change constantly.

- **Database mechanism.** P-09 "The data sits with somebody else" (`growing`, 10 groups, Conversation only). "They think of recipes as theirs" (O-0084). "The specs are in a different system and I do not have access" (O-0485). Strongest case is an unclassified grocer and counts for nothing: "we put our name on eleven hundred products that somebody else makes" (O-0629), "We hold the specification" (O-0636).
- **Research condition.** Vitamin Well merging with its bar manufacturer EMPWR (R-29). More than 60% of development activity is reformulation (R-26). Product data spread across several systems (R-56, R-57).

**Owner note from Gate 1.** Recommended as an implementation risk note rather than a use case. Owner kept it as a use case. Its most honest use may still be as a qualification question and onboarding plan rather than outbound messaging.

#### Positioning

_Hypothesis grade. No functional food customer evidence, and **no evidence that anyone in this market needs product level footprints at all.**_

**In one line.** When someone else makes the product and the recipe keeps changing, the hard part of a product footprint is getting the data from whoever holds it, not the calculation. That is the part the product is built to run.

**1. Competitive alternatives**

| What they do today | Label |
|---|---|
| Email the manufacturer a questionnaire. Supplier factors "Mostly unopened" (O-0004, off ICP). A trader treats "their sourcing as commercially confidential" (O-0294). | database evidenced |
| Rebuild by hand from what the brand holds: "by hand, over about three weeks, from packaging artwork files because there was no other source of truth" (O-0631, unclassified). | database evidenced (unclassified only) |
| A spend based average. "It just took our spending by category" (O-0071). | database evidenced |
| Wait for the PLM or specification system (R-56, R-58, R-59). | research inferred |
| Buy the factory (R-29). Brings the data in house. | research inferred |

**2. Unique attributes**

| Attribute | Evidence | Known weakness in the same capability |
|---|---|---|
| Messy material data mapped on our side | "They did the material mapping on their side as promised" (O-0226, V-12). C-05 evidenced. | That was a customer's own records across four entities, **never a third party manufacturer's.** Loading is slow with no progress message (P-07, `growing`: O-0055, O-0094, O-0333). |
| A supplier module that chases the data holder | Group procurement's request "is answered inside a week and the same request from group sustainability sits for four months" (O-0209, V-10). | The module is not what works, the signature is (C-06 only partly evidenced). If manufacturing capacity is scarce (R-29), the brand is asking a favour: the same break as C-3. |
| Assessed values with a name and a date where primary data will not come | "Then I will do thirty farms from memory" once it could be recorded as an assessed value (O-0574). "It tells me which of my numbers are actually just somebody's word" (O-0637, unclassified). | Excel export "loses the flags" (O-0329). **Nobody is notified when a supplier changes an answer:** "I found out by accident that one of them had changed their feed in July" (O-0582). In a market where recipes change constantly, this gap matters most. |

**3. Value and proof**

- **Value.** The data often already exists with the manufacturer, and the product turns "contact everyone" into a short list.
- **Proof.** V-26: the mill everyone assumed unwilling "have it... they have been collecting it since twenty twenty four because a Danish customer asked them for it" (O-0594). V-27: "It stopped being an impossible project and became a manageable list" (O-0616).
- **Which market the proof came from.** A Swedish bakery's grain mill and a Nordic multi brand owner. **No proof involves a contract manufacturer or a changing recipe.**
- **External use filter.** 5 proof rows checked, 4 excluded: V-12 shareable `unknown`, V-26 `internal only` on a lost account, V-10 and V-19 `partial`. **Only V-27 passes**, the one external proof point across both positions.

**4. Target market characteristics**

- Makes most of its volume through contract manufacturers and holds the specification, not the process data (grocer version: O-0636).
- Demand growing faster than its manufacturing (R-29), reformulating often (R-26).
- Holds a specification to the ingredient. No bill of materials means no product footprint, and the ICP file says those deals stall in implementation.
- Has a reason to need product numbers. **Unverified. First discovery question.**
- **Negative signals.** A brand that just bought or merged with its manufacturer looks like the target, but the data is now inside its own group: a different, internal sale. A brand whose specification says "vegetable oil and the manufacturer chooses" (O-0636) has nothing to model.

**5. Market category**

**Collecting supplier data where the supplier is the factory**, inside the supplier engagement category Rootline already has. The comparison set stays at email questionnaires and rebuilding by hand, which the product beats. **Avoid PLM and "specification management".** Described in those words, the comparison set becomes Specright, Centric and TraceGains (R-56 to R-58), and Rootline loses on every attribute that is not carbon.

**6. Relevant trend**

Brands buying their factories because "demand outruns supply" (R-29).

**What would falsify this.** Contract manufacturers in functional food already hand over recipe and process data under contract, so there is no access problem. Or capacity is so scarce that brands will not risk asking for anything extra. Or, whatever the first two show, discovery finds no reason at these brands to need product level numbers.

---

### A-3. A claim to defend

**Grade A.** Transfer strong on how they buy, servability low. **Positioning not run.**

- **Database mechanism.** Deals with a claim to defend survived the reporting rollback (O-0527, O-0528). A commercial claim has to survive an investor looking for a problem (O-0501, O-0504, O-0505). 2 ICP groups, not a registered pattern. Richest case is the unclassified grocer, counting for nothing: a range pulled off shelf for three days after a public challenge (O-0632), and "a filter that tells them which of their claims rest on nothing" (O-0644, O-0676). B-03 competitor claim is `new` at 1 group.
- **Research condition.** Stockholm food control enforces by complaint, brand by brand (R-36, R-37). US risk is class actions (R-38). "GLP-1 friendly" has no definition (R-39).
- **Why servability is low.** The claims under attack in the research are health and function claims under Regulation 1924/2006, which the product cannot substantiate. Only environmental claims are servable, and the research did not look for them.
- **Vocabulary risk noted for Gate 3.** "Claims" said to a functional brand's legal team will be heard as health claims.
- **Blocked on.** Who the market is: the brand's legal team, or a supplier defending its own claim. Agent recommendation: the brand, because the evidence is about the party whose name is on the claim.

### A-4. Whey's footprint moves with its price

**Grade A.** Transfer medium, servability high for dairies and medium for brands. **Positioning not run.**

- **Database mechanism.** An allocation choice decides whether the number jumps later: "I would rather explain a bigger number once" (O-0535), settled at kickoff (O-0673). A competitor figure cannot be compared without knowing its allocation (O-0499). S-01 "Something that happened before I worked here is still in my number" (5 groups). Use case 2 proof: V-01, V-09, V-11.
- **Research condition.** Milk is cheap while protein is dear (R-18). WPC up about 108% and WPI about 139% in two years (R-15).
- **Assumption added by the agent, not in either file.** Under economic allocation, a price rise shifts footprint share onto whey. Standard LCA practice, but verify with a solutions engineer before it goes further.
- **Blocked on.** Who the market is: the dairy that makes the whey (already served) or the functional brand that buys it. Agent recommendation: the dairies, the only buyer servable at high confidence.

### A-5. EUDR on cocoa and coffee

**Grade A.** Transfer medium, servability low. **Positioning not run.**

- **Database mechanism.** EUDR opened the conversation and scope grew to everything (O-0460, unclassified account, counts for nothing). S-02 "I don't know whether it even applies to what we buy" (2 groups): "Deforestation. We are a dairy in Östergötland" (O-0364).
- **Research condition.** EUDR applies from 30 Dec 2026 for large and medium operators, 30 Jun 2027 for micro and small (R-24). Coated bars depend on cocoa (R-23). Functional coffee is a live format (R-11).
- **Why servability is low.** Due diligence under EUDR is traceability and geolocation, not carbon. The company file lists EUDR as a why now but no capability.
- **Against it.** Compound coatings and cocoa free analogues may remove the cocoa exposure anyway (R-23).

### B-1. One record per product of ingredient, origin and supplier (cut)

Market native (CH-10), no database evidence. Cut on servability: the product is not PLM or GS1 Validoo, and the interface is a known weakness. Agent recommended cutting; the owner approved only the Grade A candidates, so it was not carried.

---

## 3. Parked Grade C list

Proven in the database, and the research says the mechanism will not hold in this market. Never positioned, never messaged. Re-read on every pass and report movement in either direction.

| # | What breaks | Proven here | Why it breaks there | What would move it |
|---|---|---|---|---|
| **C-1** | **Carbon as a formulation criterion.** The trap: CH-02 is the category's biggest challenge and the product models recipes. | "Formulation decisions here are made on cost and flavour profile, full stop" (O-0010). A lower carbon chilli not used on price point (O-0392, V-21). P-03 "Nobody here has changed a single decision because of it" (`confirmed, pending judgement gate`, 10 groups). | About 70% of developers prioritise cost reduction while adding protein, 66% clean label (R-26). Carbon is not among the stated priorities. | A lower carbon reformulation option that is also the cheaper one, found in discovery. |
| **C-2** | **Routinely comparing suppliers of high protein whey** (use case 5) | Works only at equal price (O-0399, O-0400). No price on a tonne (P-11). | Whey is sold forward and "essentially unavailable to new buyers seeking significant volume" (R-15), some suppliers sold out for 2026 (R-14). No choice of supplier, nothing to break a tie on. Survives only inside A-1. | New capacity landing in 2027 (R-16) reopening a spot market. |
| **C-3** | **Supplier engagement that reaches the farm, for a brand's protein inputs** (use case 4) | Supplier goodwill is scarce (P-02, `confirmed, pending judgement gate`, 13 groups). The signature decides (O-0209, V-10). Farm response lifted (V-13, V-24). | The brand is the weak party asking a favour of a supplier it depends on for allocation (R-15), and farms sit behind a handful of global processors (R-16). Counter case shows the variable is scarcity: protein suppliers "would say yes without much friction" when supply is not tight (O-0381). Still holds for the dairy selling the whey. | Whey supply loosening, or a brand that owns a dairy supply relationship. |
| **C-4** | **"Next year it takes an afternoon"** | Value compounds because recipes persist: V-23 (O-0452), V-22 (O-0420), "three weeks of recipe entry" for 22 products (O-0580). | More than 60% of development is reformulation and redesigns are full (R-26, R-27). 50% plan SKU rationalisation (R-52). **V-23 is the only `named`, shareable proof point in the database**, so losing it here matters. | Evidence of a stable core range under the reformulation churn. |

### Could not be graded: the research did not look

_Proposed by the agent as a recorded category. The owner did not rule on it; by default these go to the discovery agenda._

- Use case 1, customer or retailer scorecards on functional products.
- AFNS-1 and B-03, a carbon figure on pack.
- Use case 2, audit and CSRD at a brand of Vitamin Well's size.
- Use case 6, reduction targets. Not raised as a candidate, per the note in `use-case-context.md`.

### Constraints that carry over (not candidates)

- **P-01 "There is no second person"** (`confirmed, pending judgement gate`, 19 groups) meets Swedish food companies unable to hire (R-33).
- **S-06 "New lines never come off again"** (signal, 5 groups) meets margins squeezed by promotions (R-50) and cost programmes (R-52).

---

## 4. Out of scope, named once

Real challenges in this market that the product cannot serve.

- CH-01 protein prices and supply security.
- CH-02 taste, texture, shelf life and processing.
- CH-04 energy drink age limits and caffeine rules.
- CH-05 contaminants, allergens, packing errors and recalls.
- Health and nutrition claims under Regulation 1924/2006.
- CH-06 novel food approval, GRAS, the US "healthy" rule, the UK sugar levy on milk drinks, FSMA 204 traceability. Note: S-04 "Forwarded it to me with a question mark" (4 groups) shows non carbon regulatory notices already landing on the carbon owner. This market would send more of them. Still not ours.
- CH-07 production capacity and hiring.
- CH-08 trade spend and retailer power.
- CH-09 which functional trend lasts.

---

## 5. Discovery agenda

The questions that would move any of this from hypothesis to evidence. Ask these before any messaging goes out.

**Is there demand at all** (blocks everything)
1. Has any retailer, customer, investor or board asked a functional brand for carbon numbers on its products? When, and with a date attached?
2. Who at a functional brand would own that question today?
3. Do functional brands make environmental claims on pack or online, alongside the health and function wording?

**A-1, forced change of origin**
4. Who is re-sourcing plant protein away from China, and what are the alternatives on the shortlist?
5. How far apart on price are those alternatives after duties?
6. Is the 2027 sourcing decision already made?
7. Does purchasing use anything besides price, quality and supply security when prices are close?
8. Internal: does the factor library separate pea and whey isolate by origin and process?
9. Internal: can V-17 be cleared for external use?

**A-2, brand with no factory**
10. Does the contract manufacturer hand over recipe and process data under contract today? Has anyone asked?
11. How often does a live product's recipe change, and who is told?
12. Does the brand hold its specification to the ingredient, or does the manufacturer choose?

**A-3, claim to defend**
13. Which environmental claims, if any, does the brand carry, and what backs them?
14. Has any claim been challenged, and who handled it?

**A-4, whey's footprint moves with its price**
15. Internal: which allocation method do served dairies use for whey, and would a price move shift their numbers?
16. Have whey buyers ever asked a dairy about the footprint of the protein fraction?

**A-5, EUDR**
17. Which functional brands are in scope as operators for cocoa or coffee, and are they reformulating away from cocoa anyway?

**Grade C checks**
18. Is there a lower carbon reformulation option that is also cheaper? (C-1)
19. Is any whey buyer outside forward contracts with a real choice of supplier? (C-2)

---

## 6. Decisions log

| Date | Decision | By |
|---|---|---|
| 16 Sept 2026 | Industry set to functional food, the only research file available. | Owner |
| 16 Sept 2026 | Customer evidence taken from `structured-database-w36.md` (W33 to W36) rather than the W33 to W35 file the skill names. | Owner |
| 16 Sept 2026 | Run type set to new vertical: no earlier output file. | Agent |
| 16 Sept 2026 | Resolved account set is empty; coverage 0 groups. Output leads with the gap. Adjacent accounts listed with reasons for exclusion. | Agent |
| 16 Sept 2026 | Research silence on carbon treated as unsearched, not low salience, per the file's own Part 9. No carbon demand condition counts as confirmed. | Agent |
| 16 Sept 2026 | A-1 to A-5 approved. | Owner |
| 16 Sept 2026 | B-1 not carried: agent recommended cutting, owner approved only the Grade A candidates. | Owner |
| 16 Sept 2026 | C-1 to C-4 parked by default. | Agent |
| 16 Sept 2026 | "Could not be graded" proposed as a recorded list, not ruled on. Defaulted to the discovery agenda. | Agent, pending owner |
| 16 Sept 2026 | A-2 kept as a use case against the agent's recommendation to downgrade it to an implementation risk note. | Owner |
| 16 Sept 2026 | A-1 worked sample shape approved for the remaining positions. | Owner |
| 16 Sept 2026 | Run stopped after A-2 positioning. A-2 not reviewed. File written at the stop. | Owner |
| 16 Sept 2026 | Reported, not fixed: observation log at 680 rows against the database's own 300 row split point. | Agent |

---

## Resume point

1. Owner reviews A-2 positioning.
2. Owner answers the market question for A-3 (brand or supplier) and A-4 (dairy or brand). Agent recommendation: brand for A-3, dairies for A-4.
3. Run Gate 2 for A-3, A-4, A-5 in the approved shape, stopping after each.
4. Gate 3 messaging only from approved positions, with the unverified demand warning at the top. Vocabulary to avoid already collected: "next year it takes an afternoon" (C-4), "reach the farm" (C-3), "claims" unqualified (A-3), "PLM" and "specification management" (A-2), "carbon accounting" as the category (A-1).
5. Owner rules on whether "could not be graded" becomes a standing category in the skill.
