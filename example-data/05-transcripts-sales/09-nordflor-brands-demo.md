# Nordflor Brands / Rootline — demo

**Date:** 2026-08-18
**Week:** 2026-W34
**Duration:** 47 min 00 sec
**Type:** Sales call, third meeting
**Recorded in:** Conversation intelligence tool, auto transcribed, not corrected

**Rootline:** Sofia Bergström (Account Executive), Tobias Rahm (Solutions Engineer)
**Nordflor Brands:** Ylva Sandell (Group Sustainability Manager), Göran Wrede (Sustainability Director)
**Third party:** Per Brännström (assurance provider, observer)

---

[00:00:11] **Ylva Sandell:** Okay. Everyone can hear? Good. So, Per is here from our assurance provider. Per, this is Sofia and Tobias from Rootline. The reason I asked Per to join is that we have been burned before.

[00:00:25] **Sofia Bergström:** Thank you for the introduction, and thank you for being upfront about the history rather than letting us discover it partway through.

[00:00:34] **Per Brännström:** I'd rather set expectations honestly from minute one than have anyone assume a level of trust that hasn't been earned yet.

[00:00:43] **Sofia Bergström:** Burned how? I'd rather hear the specific shape of it than assume.

[00:00:47] **Ylva Sandell:** We built the last report on a model that our previous provider could not explain to Per when he asked. So we spent six weeks in March reconstructing things that should have taken an afternoon.

[00:01:02] **Sofia Bergström:** Six weeks is a lot to lose on something that should have been fast.

[00:01:07] **Ylva Sandell:** It was six weeks of two people, more or less full time, plus me checking in every day, so the actual cost was considerably more than six weeks of one person's calendar.

[00:01:20] **Per Brännström:** That is a polite version. There is a less polite one, but Ylva would rather I not use it in front of a vendor.

[00:01:30] **Ylva Sandell:** [laughs] It is the version I say in front of vendors. The real version has considerably more swearing in it.

[00:01:38] **Sofia Bergström:** Then I would suggest we let Per drive most of this. Per, ask us whatever you would ask us in an engagement.

[00:01:47] **Ylva Sandell:** That's exactly why I wanted him here rather than briefing him afterward and hoping the answers held up.

[00:01:54] **Sofia Bergström:** I'd rather have the real questions asked live than discover a gap after signature.

[00:02:00] **Per Brännström:** Happily. I will say up front that I am not here to recommend a vendor and I will not. My interest is whether the output is auditable.

[00:02:11] **Sofia Bergström:** That's a completely fair position and honestly the one I'd want from an assurance provider in the room.

[00:02:18] **Per Brännström:** Good. I say it at the start of every one of these so nobody spends the meeting trying to read a recommendation into a question I ask.

[00:02:29] **Sofia Bergström:** Understood.

[00:02:30] **Göran Wrede:** I'd rather you were this direct with us throughout the relationship than only in the sales process.

[00:02:36] **Sofia Bergström:** That's the intention, genuinely, I'd rather build that reputation slowly than lose it the first time something's inconvenient to say.

[00:02:45] **Ylva Sandell:** I'd rather you heard the real version than the polished one we'd have given a vendor two years ago before all of this happened. It's a better use of everyone's time, and it means I'm not maintaining two different stories.

[00:03:01] **Sofia Bergström:** That's exactly what I want, honestly. The polished version tells me nothing useful. It also makes me trust everything else you say more.

[00:03:10] **Per Brännström:** I ask because I've sat through demos where a vendor claims full coverage and it turns out three categories were simply never populated, blank rather than screened, and nobody flagged the difference until I asked directly.

[00:03:25] **Ylva Sandell:** How did that come out, in those cases? Did the vendor admit it readily or did it take pressure?

[00:03:32] **Per Brännström:** Varied. Some admitted it immediately once asked directly, which I respect. Others tried to argue the blank was itself a form of disclosure, which it is not. That argument has never once held up when I've pushed on it properly.

[00:03:49] **Ylva Sandell:** Per, why don't you take us through your own questions now, rather than us talking about hypotheticals.

[00:03:55] **Per Brännström:** First question. If I select a single line in the scope three inventory, can you show me the complete chain from that line back to a source document? This is the question I always start with, it tells me most of what I need to know.

[00:04:14] **Tobias Rahm:** Yes. Let me do it rather than describe it. Ylva, may I use the trial tenant?

[00:04:21] **Ylva Sandell:** Please, that's exactly what it's there for.

[00:04:23] **Tobias Rahm:** I'd rather show real screens than describe a diagram, it tends to answer follow up questions before they're even asked.

[00:04:31] **Ylva Sandell:** Go ahead, it has three of the brands loaded.

[00:04:35] **Tobias Rahm:** Which three, so I know what I'm navigating to?

[00:04:39] **Ylva Sandell:** The two on the older ERP and one of the larger brands on the main system, should give a reasonable spread.

[00:04:47] **Tobias Rahm:** Sharing. So here is the group inventory. I will pick purchased goods, and inside that, one of the brands, and inside that, a material. Sunflower oil. Here is the emissions figure for the year.

[00:05:01] **Per Brännström:** Why sunflower oil specifically, out of curiosity, rather than any other material?

[00:05:06] **Tobias Rahm:** No particular reason beyond it being one of the larger material lines in the trial data, it makes a good example because the chain back to source is genuinely long, several suppliers, several origins in a given year.

[00:05:21] **Per Brännström:** Now take me back.

[00:05:23] **Tobias Rahm:** Happy to. This is where most vendors stop, showing a nice front end number and hoping nobody asks what's underneath it.

[00:05:31] **Per Brännström:** I'm not most vendors' customers, so let's go further than that.

[00:05:36] **Tobias Rahm:** One click gives you the activity data, which is tonnage, by month, by site. Second click gives you the source of that tonnage, which in this case is a specific ERP extract with the extract date and a row count. Third click gives you the emission factor applied, with its source, vintage, geography and method. And there is a fourth thing, which is the change log.

[00:06:03] **Per Brännström:** Row count specifically, can you say more about why that matters to you as a design choice?

[00:06:10] **Tobias Rahm:** It's a cheap integrity check. If somebody re-runs the extract next month and the row count for the same period has changed without an obvious reason, that's a flag worth investigating before it becomes a number anyone reports on.

[00:06:25] **Per Brännström:** Show me the change log. I want to see the actual mechanism, not a description of it.

[00:06:32] **Tobias Rahm:** So this shows that on the twelfth of June somebody changed the origin assumption for this material from a European average to Ukraine specific, and it records who, and there is a comment field, which in this case says "confirmed with procurement, contract switched in Q1".

[00:06:51] **Per Brännström:** So the June change reflects a Q1 event, recorded five months late. Is that lag typical?

[00:06:57] **Tobias Rahm:** It happens, yes, particularly when a procurement change isn't immediately communicated to whoever owns the sustainability data. The system doesn't care when the change is logged, only that it's logged accurately and attributed to the right person, which is what actually matters for the audit trail.

[00:07:16] **Per Brännström:** And can that comment field be edited afterwards? That's usually where I find the gap in a vendor's story.

[00:07:24] **Tobias Rahm:** The comment can be amended, and the amendment is itself logged with the previous text retained. Nothing is deleted.

[00:07:31] **Per Brännström:** Can I see that, an amended comment with its history?

[00:07:35] **Tobias Rahm:** Here, this one was amended twice. Original text, first amendment with a timestamp and who made it, second amendment the same way. All three versions sit here, nothing overwritten.

[00:07:47] **Per Brännström:** That's a genuinely complete audit trail, more than most tools bother with on a comment field specifically.

[00:07:54] **Göran Wrede:** That's more than I expected on something as small as a comment field.

[00:07:59] **Per Brännström:** Can an administrator delete the log?

[00:08:02] **Tobias Rahm:** No. There is no interface for it and no permission level that allows it.

[00:08:07] **Per Brännström:** What about at the database level, below the interface? I ask because that's usually where the real answer lives.

[00:08:15] **Tobias Rahm:** The underlying records are append only at the database level as well, it's not simply an interface restriction that a sufficiently determined administrator could route around.

[00:08:26] **Per Brännström:** Good. That is the answer I wanted and it is not the answer I usually get.

[00:08:32] **Göran Wrede:** How often do you actually get that answer, roughly, across the vendors you evaluate?

[00:08:38] **Per Brännström:** Rarely. Most tools I look at have some version of an editable history, or an administrator override that technically exists even if it's never meant to be used. A genuinely locked log is unusual enough that I remember the vendors who have it.

[00:08:55] **Göran Wrede:** Per, is that unusual?

[00:08:57] **Per Brännström:** Reasonably, yes. I'd say maybe one in five vendors I evaluate has something close to what Tobias just showed. Most tools have a version history. Fewer have a locked one. The distinction matters because the question I have to answer is not what the number is, it is whether the number could have been changed after the fact by someone with an interest in it.

[00:09:23] **Göran Wrede:** Has that actually happened, somebody changing a number with an interest in it? Not necessarily here, generally.

[00:09:30] **Per Brännström:** I won't name a case, but yes, more than once in my career. Usually not malicious in intent, more a case of someone under pressure to hit a target adjusting an assumption without documenting why, and the documentation gap is what turns a judgment call into something that looks like manipulation after the fact.

[00:09:52] **Göran Wrede:** Right.

[00:09:53] **Per Brännström:** I want to move on to the second question, if everyone's satisfied with the first.

[00:09:58] **Ylva Sandell:** Go ahead, this is exactly what I asked you here for.

[00:10:03] **Per Brännström:** Second question. Restatements.

[00:10:04] **Göran Wrede:** This is the part I find most relevant to what I'm actually worried about, so I'm glad it's coming up.

[00:10:12] **Per Brännström:** It should be relevant to you specifically, restatements are exactly where a target commitment gets undermined if the underlying number isn't stable. When your factor library updates, what happens to last year's number? This is the one that catches most vendors out, if they haven't thought it through properly.

[00:10:32] **Tobias Rahm:** Nothing, unless you ask for it. Reporting periods lock when you close them. A locked period keeps the factors that were current when it was closed. If you want to restate a prior year on new factors you run it explicitly, and you get both versions side by side with the difference attributed by cause.

[00:10:54] **Per Brännström:** Who is able to trigger that explicit restatement? Any user, or a restricted set?

[00:11:00] **Tobias Rahm:** It's a permission gated action, typically limited to whoever owns the reporting function on the customer side, so it's not something a junior analyst can trigger accidentally while exploring the tool.

[00:11:13] **Per Brännström:** Attributed by cause. Meaning?

[00:11:14] **Tobias Rahm:** Meaning it separates how much of the change came from a factor update, how much from an activity data correction, and how much from a methodological change. Because those three have to be disclosed differently.

[00:11:28] **Ylva Sandell:** Does the disclosure language get generated automatically as well, or is that still something I'd write myself?

[00:11:35] **Tobias Rahm:** The three figures are generated automatically. The narrative explanation, the actual sentence a board reads, that's still yours to write, though the numbers underneath it are ready made rather than something you have to reconstruct.

[00:11:49] **Per Brännström:** [pause] Yes. They do. Every one of those three categories carries a different disclosure obligation.

[00:11:55] **Ylva Sandell:** Per, is that important?

[00:11:57] **Per Brännström:** It's the single most important thing on this call, if I'm honest, more important than anything about the interface itself. Everything else is secondary to whether I can trust the underlying process. A beautiful interface on top of an untrustworthy process is worse than an ugly interface on top of a solid one. I'd take the ugly, trustworthy one every single time.

[00:12:22] **Ylva Sandell:** That's useful to know, it tells me where to focus my own attention as I write the recommendation. I'll lead with that rather than bury it. It's the part the CFO will actually care about most.

[00:12:37] **Per Brännström:** It is the thing that cost you six weeks in March. Your number moved and nobody could tell me why it moved, and I could not sign something I could not explain.

[00:12:50] **Ylva Sandell:** Our number moved fourteen percent and I could not explain to the board why.

[00:12:55] **Sofia Bergström:** Was that in a board meeting specifically, or a written report that went to them?

[00:13:01] **Ylva Sandell:** A board meeting. Live. Somebody asked directly and I had about four seconds to decide what to say.

[00:13:09] **Göran Wrede:** Which was not a good meeting. I sat two seats down from her and I could see it not landing.

[00:13:17] **Ylva Sandell:** It was not a good meeting. I've had better ones.

[00:13:21] **Sofia Bergström:** Can I ask what you told them in the end? I ask because it tells me what the actual gap in confidence was.

[00:13:30] **Ylva Sandell:** I said it was better supplier data. Which was partly true, and which sounded exactly like what someone says when they do not know.

[00:13:40] **Sofia Bergström:** Did anyone on the board press further on it?

[00:13:44] **Ylva Sandell:** One director did, gently, and I could tell she didn't fully believe the answer, but there wasn't a follow up meeting scheduled to dig further, so it just sat there unresolved.

[00:13:56] **Sofia Bergström:** And this year? What would you say if the same question came up again.

[00:14:02] **Ylva Sandell:** This year I would like to be able to say, four percent of the movement is a factor update, three percent is because we corrected the tonnage on two sites, and the rest is a real reduction because we changed a supplier.

[00:14:19] **Göran Wrede:** That's a genuinely different board conversation from the one we had.

[00:14:23] **Ylva Sandell:** It's the conversation I should have been able to have the first time. I just didn't have the tool to produce those three numbers separately.

[00:14:33] **Tobias Rahm:** That is exactly the output. That's precisely the screen I want to show you next.

[00:14:40] **Sofia Bergström:** Ylva, can I ask what happened with the previous provider? Not to score points, but because I want to know what to avoid.

[00:14:49] **Ylva Sandell:** It was not malice. They were a small company and they built us something bespoke, and the person who built it left.

[00:14:58] **Sofia Bergström:** How big were they, roughly, as a company? I ask because it changes how surprised I am.

[00:15:05] **Ylva Sandell:** Small. Six or seven people total, from what I understood. A genuinely capable founder who built something clever, and then the whole thing depended on one person's memory of their own design.

[00:15:18] **Per Brännström:** That is the more common failure, in my experience.

[00:15:21] **Ylva Sandell:** And when he left, nobody at their end could explain the model, because it was in his head and in a set of spreadsheets he maintained. So when Per asked how a category was calculated, they had to reverse engineer their own product.

[00:15:39] **Per Brännström:** That's a fairly common failure mode with smaller boutique providers, in my experience. The rigour lives in one person's head rather than in the system itself.

[00:15:49] **Göran Wrede:** Is there a way to test for that in advance, before you've already committed to a vendor?

[00:15:56] **Per Brännström:** Ask them directly what happens if their lead technical person leaves tomorrow. The answer tells you almost everything.

[00:16:03] **Sofia Bergström:** How long did that take?

[00:16:05] **Ylva Sandell:** Three weeks, more or less, from the moment Per raised the question to when we had an answer we could stand behind.

[00:16:14] **Per Brännström:** Three weeks I spent chasing, and three weeks that were not billed to anyone as productive time, because nobody had budgeted for a reconstruction project. Three weeks is what I heard, but I'd rather hear it from you directly.

[00:16:30] **Ylva Sandell:** Three weeks. And the answer, when it came, was that two of our categories had been calculated on a method that did not match what we had disclosed.

[00:16:41] **Göran Wrede:** Which two categories, do you remember?

[00:16:44] **Ylva Sandell:** Purchased goods and packaging, the two largest, which is exactly why the fourteen percent was as large as it was rather than something we could have quietly absorbed.

[00:16:56] **Per Brännström:** Which meant a restatement. And a restatement is never a quiet event, in my experience.

[00:17:02] **Ylva Sandell:** Which meant the fourteen percent.

[00:17:04] **Göran Wrede:** And the board conversation. Which I sat through, for what it's worth, and it was not comfortable for anyone in the room.

[00:17:13] **Ylva Sandell:** And the board conversation.

[00:17:14] **Sofia Bergström:** So the fourteen percent was not better data at all. It was a methodology correction. Those get disclosed completely differently and read completely differently to an outside observer.

[00:17:26] **Ylva Sandell:** [pause] Yes. It was. I said better data because that is what I understood at the time.

[00:17:32] **Per Brännström:** That's worth saying plainly, actually. You didn't mislead anyone deliberately, you were given a wrong explanation and repeated it in good faith.

[00:17:41] **Ylva Sandell:** That's generous of you to say and I appreciate it, though it didn't feel that way sitting in front of the board at the time.

[00:17:52] **Per Brännström:** Which is a disclosure problem in itself, incidentally. Those are different things and they are reported differently.

[00:17:58] **Ylva Sandell:** I know that now, and it's a lesson I paid three weeks and a bad board meeting to learn.

[00:18:06] **Per Brännström:** Most people pay some version of that price to learn it. I'd rather this be the last time you pay it.

[00:18:15] **Ylva Sandell:** I know that now.

[00:18:16] **Tobias Rahm:** Can I show you something that might be useful then? If I open the restatement view here, and force a methodology change on this category, you get this. Three lines. Factor update, activity correction, methodology. And the methodology line requires a text justification before it will let you close the period.

[00:18:37] **Per Brännström:** Is that justification field free text, or does it draw from a controlled list of reasons?

[00:18:43] **Tobias Rahm:** Free text, deliberately. A controlled list tends to produce lazy selections that don't actually explain anything, we'd rather force somebody to write a real sentence.

[00:18:53] **Ylva Sandell:** It requires it?

[00:18:55] **Tobias Rahm:** It requires it, yes, no exceptions, regardless of how senior the person closing the period is.

[00:19:01] **Ylva Sandell:** I like that it doesn't have an exception path. An exception path is where the discipline always ends up leaking out. I've watched that exact thing happen at a previous employer, a control that existed on paper and got waived so often it stopped meaning anything.

[00:19:20] **Tobias Rahm:** You cannot lock the period without it. That is deliberate. It is the one field people always skip.

[00:19:27] **Per Brännström:** In my experience, forcing a field like that is the single highest leverage design decision a vendor can make. People will always skip an optional justification field.

[00:19:38] **Ylva Sandell:** That's genuinely reassuring to hear from someone who isn't trying to sell it to me.

[00:19:44] **Per Brännström:** That would have saved this company three weeks and me two.

[00:19:49] **Ylva Sandell:** I've thought about that a lot, actually, how one required field could have avoided the entire episode. It's a slightly maddening thing to sit with. Knowing exactly what would have prevented three weeks of pain, after the fact, is its own kind of frustration.

[00:20:06] **Per Brännström:** It's rarely one dramatic gap that causes these things. It's usually one small missing safeguard that happens to sit exactly where it matters most. That's precisely what happened here. That's precisely what happened here.

[00:20:20] **Göran Wrede:** Two weeks of your time, or two weeks generally?

[00:20:24] **Per Brännström:** My time specifically, going back and forth trying to reconcile a number I couldn't get a straight explanation for.

[00:20:32] **Ylva Sandell:** Tobias, which scope three categories do you actually cover? Because our last one covered four and told us the rest were immaterial without ever calculating them.

[00:20:42] **Per Brännström:** That's precisely the kind of thing I flag when I see it. Immaterial is a conclusion, not an assumption, and it should be shown as one.

[00:20:53] **Ylva Sandell:** That's what I've come to understand, yes, though I didn't have the language for it at the time.

[00:21:00] **Tobias Rahm:** All fifteen, though not all with the same depth. Purchased goods, upstream transport, waste, business travel, commuting, use of sold products, end of life, the whole list. For a food group, purchased goods will be eighty five percent or more, upstream transport maybe five, and the rest are individually small.

[00:21:20] **Ylva Sandell:** What about use of sold products? That one's always confused me for a food company, what does that even mean for us.

[00:21:29] **Tobias Rahm:** For most food products it's genuinely negligible or not applicable, since there's no energy consumption at the use stage the way there would be for, say, an appliance. It still gets screened rather than skipped, but the answer is usually a documented zero.

[00:21:46] **Ylva Sandell:** But calculated, not assumed away. I want to be completely clear that's what I'm asking, not just a rough estimate presented as calculated.

[00:21:56] **Tobias Rahm:** Calculated. And where a category is genuinely not applicable to you, that is recorded as a screening result with a reason, not left blank.

[00:22:06] **Per Brännström:** Can you show me what a screening result actually looks like in the interface, rather than just describe it?

[00:22:13] **Tobias Rahm:** Here. This category is screened as not applicable, with a two line justification and the name of who made that determination and when. It sits in the report exactly where the number would be, just clearly marked as a screening decision rather than a calculation.

[00:22:31] **Per Brännström:** That's the right way to handle it. A blank invites the reader to assume the worst, or the best, depending on who's reading.

[00:22:41] **Tobias Rahm:** Is that a distinction most customers understand right away, or does it usually need explaining?

[00:22:47] **Per Brännström:** That distinction matters more than people think.

[00:22:50] **Sofia Bergström:** Have you seen customers actually get burned by that distinction specifically? I'm curious whether that's a theoretical risk or something you've watched happen.

[00:22:59] **Per Brännström:** More than once, usually when a competitor or journalist compares two companies' reports and one of them has quietly left categories blank rather than screened, and it reads as an omission when it might have been a genuine non applicability. A blank and a screened out zero look identical in a report and mean completely different things.

[00:23:22] **Ylva Sandell:** Can I ask a slightly different question, since we're on coverage. Do you ever have to tell a customer that a category genuinely isn't material for them, and have they pushed back on that?

[00:23:36] **Tobias Rahm:** Regularly, actually. Franchising is a common one, most food producers screen it out immediately, and occasionally someone insists on calculating it anyway because a stakeholder asked, even once we've shown them it's a fraction of a percent.

[00:23:51] **Per Brännström:** Third question, and this is the one I care most about. Coverage and estimation. How much of the inventory is primary data and how do you present the rest?

[00:24:03] **Sofia Bergström:** Why is this the one you care most about, out of the three?

[00:24:08] **Per Brännström:** Because the first two are about process integrity, whether a number could have been tampered with or quietly restated. This one is about whether the number is actually any good in the first place, which is a different and in some ways more fundamental question.

[00:24:26] **Tobias Rahm:** Every line carries a data quality tier. Primary, supplier specific secondary, regional average, global average. And the report renders coverage as a percentage of emissions, not as a percentage of lines, which matters because ninety percent of your lines can be five percent of your number.

[00:24:45] **Per Brännström:** Can you show that split for the trial data, coverage by emissions versus coverage by line count?

[00:24:52] **Tobias Rahm:** Here. Sixty two percent primary data by emissions weight, twenty eight percent regional average, ten percent global average. By line count it would look completely different, closer to ninety percent of lines sitting in the global average tier, because that's where all the small immaterial purchases land.

[00:25:11] **Per Brännström:** Most tools report it as a percentage of lines. It's the single most common way I see coverage misrepresented, deliberately or otherwise.

[00:25:20] **Tobias Rahm:** I know. It flatters everyone. It's an easy number to report and a genuinely misleading one.

[00:25:26] **Per Brännström:** [laughs] It does. Every vendor I've sat through a demo with has led with the line count figure until I ask for the other one.

[00:25:36] **Göran Wrede:** Sofia, can I move us to a different subject for a minute.

[00:25:41] **Sofia Bergström:** Of course.

[00:25:42] **Göran Wrede:** Everything Per is asking about is about reporting. And reporting is Ylva's problem, and it is a real problem, and I want it solved. But my problem is the target.

[00:25:54] **Sofia Bergström:** Can you tell me about the target itself, roughly? The number and the year, so I understand the shape of what you're actually accountable for.

[00:26:04] **Göran Wrede:** Forty two percent reduction against a 2020 baseline by 2030. It went into the annual report two years ago and the CEO has referenced it publicly since.

[00:26:15] **Sofia Bergström:** Say more.

[00:26:16] **Göran Wrede:** I want you to understand this isn't abstract for me, it's a number my own name is attached to publicly. That changes how I weigh everything else in this meeting. It's the lens I'm running everything through today, whether I say so out loud or not.

[00:26:34] **Sofia Bergström:** I understand that, and I don't want to treat it as an abstraction either. It deserves a real answer, not a comfortable one. I'd rather you left this meeting with an accurate picture than a reassuring one. Accurate is more useful to you long term, even if it's less comfortable today.

[00:26:55] **Göran Wrede:** We committed to a reduction target. It is public. It is on the website and in the annual report and the CEO has said it out loud at two conferences. And we are two years in and I do not have a plan that gets us there, I have a number that tells me where we are.

[00:27:18] **Sofia Bergström:** Understood.

[00:27:19] **Göran Wrede:** So when I look at this, what I want to know is what it does about that. Not what it measures. What it actually does about the number once we have it.

[00:27:32] **Sofia Bergström:** Let me answer that in two parts, and the second part is going to be less satisfying than the first. I'd rather give you the honest shape of it than lead with the part that sounds better. That's just how I'd rather run this whole relationship.

[00:27:50] **Göran Wrede:** Go ahead.

[00:27:51] **Sofia Bergström:** The first part. Almost all of your reduction is going to come from sourcing decisions, because you are a food group and eighty five plus percent of your footprint is agricultural inputs. You cannot make a sourcing decision on a category average, because a category average says every supplier of sunflower oil is identical. The moment you can tell them apart, your procurement team has levers it does not currently have. That is a reduction capability and it comes directly out of the measurement.

[00:28:25] **Göran Wrede:** Do you have a real example of that happening, not a hypothetical one?

[00:28:30] **Sofia Bergström:** An oils and fats customer of ours had their sourcing manager see two suppliers of the same material with meaningfully different footprints, purely because we could differentiate them for the first time. He changed the book based on that, inside a quarter, without us doing anything beyond showing him the comparison.

[00:28:51] **Göran Wrede:** That's genuinely the kind of thing I want more of.

[00:28:55] **Sofia Bergström:** I'd rather give you one real example than ten hypothetical ones.

[00:28:59] **Göran Wrede:** Fine. And the second part. Go on, tell me the part I'm not going to like.

[00:29:06] **Sofia Bergström:** The second part is that we do not have an abatement planning module with cost curves and pathway modelling. We have scenario comparison, which lets you model what happens if you switch a supplier or change a specification. What we do not have is the thing that produces a board ready pathway to 2030 with a cost per tonne on each measure.

[00:29:31] **Göran Wrede:** What does scenario comparison actually let me do, concretely, short of the full pathway thing?

[00:29:37] **Sofia Bergström:** You could model, for instance, switching your second largest sunflower oil supplier to one with a lower footprint, and see the group level impact before you make the commercial decision. It's directional and useful, it just doesn't come with a cost per tonne figure attached or a multi year trajectory built around it.

[00:29:59] **Göran Wrede:** And is that coming? I need to know whether to wait for it or plan around its absence.

[00:30:06] **Sofia Bergström:** It is on the roadmap. I am not going to give you a date because I do not have one I would trust.

[00:30:15] **Göran Wrede:** I appreciate you not inventing a date just to close today.

[00:30:20] **Sofia Bergström:** I'd rather lose a point on this call than have you hold me to a date I made up under pressure.

[00:30:28] **Göran Wrede:** Mm.

[00:30:29] **Ylva Sandell:** Göran, can I say something. Before you decide how you feel about the roadmap answer.

[00:30:35] **Göran Wrede:** Yes.

[00:30:36] **Ylva Sandell:** I cannot build a pathway on the data we have now anyway. If someone gave me a beautiful planning tool tomorrow I would be planning on averages, and every measure in it would be a guess. I would rather have the data right first.

[00:30:53] **Göran Wrede:** I understand the logic. I still don't love being told twice in one meeting to wait.

[00:30:59] **Ylva Sandell:** I'm not asking you to love it. I'm telling you what would actually be true a year from now if we skipped straight to the planning tool.

[00:31:10] **Sofia Bergström:** For what it's worth, Ylva's right on the substance, even though I understand why it's frustrating to hear.

[00:31:18] **Göran Wrede:** I hear that. My concern is that we will get the data right and then have this same conversation in eighteen months about the next tool.

[00:31:28] **Sofia Bergström:** Can I ask what would actually reassure you on that, short of a firm date I can't give you?

[00:31:36] **Göran Wrede:** [pause] Honestly, I'm not sure there's a good answer to that. Probably just watching whether the measurement side stays solid for a year without us having the same conversation about data quality that we're having about Per's questions today.

[00:31:52] **Sofia Bergström:** That's a fair bar and I'd rather be held to that than to a promise about a feature that doesn't exist yet.

[00:32:01] **Göran Wrede:** Then let's hold you to it properly rather than let it slide.

[00:32:05] **Sofia Bergström:** That is a legitimate concern and I will not talk you out of it. I'd rather agree with you than pretend the concern isn't real.

[00:32:16] **Göran Wrede:** Okay. Then let us park it as phase two and get phase one right. I'm trusting that phase two actually happens and isn't just a polite way of saying no.

[00:32:28] **Sofia Bergström:** I'll make sure it's documented as a commitment on our side too, not just something said in a meeting and forgotten. I don't want this to be the kind of thing that quietly disappears once the deal is signed.

[00:32:44] **Göran Wrede:** I'd appreciate that. Put it in whatever you send after this call. I'd rather have it in writing than have to remember it was said.

[00:32:54] **Ylva Sandell:** Phase two. Written down, not just said in a meeting.

[00:32:58] **Göran Wrede:** Phase two. I'll hold us to it.

[00:33:01] **Sofia Bergström:** Noted. Ylva, can we talk about the practical side? You have twenty two brands.

[00:33:06] **Ylva Sandell:** Please, I've been waiting for the practical part, the rest has been important but this is where I actually make decisions.

[00:33:15] **Sofia Bergström:** Fair, let's get into the actual logistics then.

[00:33:18] **Ylva Sandell:** I have twenty two brands and four of them are on a different ERP. Two of those four came in through the acquisition in 2023 and they still run their own finance system because the integration project got postponed twice.

[00:33:34] **Sofia Bergström:** Do you know why it got postponed, out of curiosity? Sometimes there's a reason that tells me something useful about the account.

[00:33:43] **Ylva Sandell:** Budget, mostly, and then a change in IT leadership that reset priorities. Nobody's opposed to it happening, it's just never been urgent enough to win against other projects.

[00:33:54] **Tobias Rahm:** What are the four running? I want to know exactly what we're integrating with before I promise you anything.

[00:34:02] **Ylva Sandell:** Two on an older Microsoft product, one on something Danish that I cannot pronounce, and one on, I want to say, spreadsheets and hope.

[00:34:12] **Tobias Rahm:** For the Danish system, do you know roughly what version or vintage it is? Sometimes that changes how straightforward an extract is. It's worth knowing before we commit to a timeline for that entity specifically.

[00:34:26] **Ylva Sandell:** I genuinely don't know off the top of my head, I'd have to ask whoever administers that entity's finance function directly. I'll find out before we start rather than guess.

[00:34:38] **Tobias Rahm:** [laughs] Spreadsheets and hope is a more common ERP than people admit.

[00:34:43] **Ylva Sandell:** It's the smallest of the four by revenue, thankfully, so at least the mess is contained to something that doesn't move the group number much.

[00:34:53] **Tobias Rahm:** [laughs] The fourth one is genuinely the easiest, for what it is worth. A file drop with a defined template works fine and about a third of our customers run at least one entity that way.

[00:35:08] **Ylva Sandell:** A third? I assumed we were unusual having any entity that disconnected.

[00:35:13] **Tobias Rahm:** You're genuinely not unusual, every multi brand group we work with has at least one entity that's technically part of the group and operationally still running on its own systems, usually from an acquisition.

[00:35:26] **Ylva Sandell:** And the reporting still consolidates?

[00:35:28] **Tobias Rahm:** It does, the same underlying model handles a file drop entity exactly the way it handles a direct integration, just with a lower confidence tier attached.

[00:35:39] **Ylva Sandell:** That's genuinely one of the things I was most worried about coming into this call. Consolidation across mismatched systems has burned us before, not with carbon reporting specifically, but with finance consolidation generally.

[00:35:52] **Tobias Rahm:** It consolidates identically. The data quality tier will show that entity as lower resolution, which is honest.

[00:35:59] **Per Brännström:** Lower resolution meaning what, specifically, in terms of the underlying number?

[00:36:04] **Tobias Rahm:** It means the emission factors applied to that entity's data are more likely to be regional or global averages rather than supplier specific ones, simply because a file drop carries less structured detail than a direct system integration does.

[00:36:19] **Per Brännström:** Which I would want to see disclosed.

[00:36:22] **Göran Wrede:** Is that the kind of thing an assurance provider like you would actually push back on if it weren't disclosed?

[00:36:30] **Per Brännström:** Yes, and I have, more than once, refused to sign off on a report that blended data quality tiers without disclosure. It's exactly the kind of gap that looks fine until someone asks the wrong question at the wrong time. I've seen too many reports that quietly treat every entity as equally precise.

[00:36:52] **Tobias Rahm:** It is disclosed automatically.

[00:36:53] **Per Brännström:** Good, that's the correct default, disclosure by default rather than requiring somebody to remember to add it. Defaults matter more than most vendors realise. We spend more design time on defaults than on almost anything else in the product. You don't have to remember to flag it, the system does it for you.

[00:37:15] **Ylva Sandell:** Sofia, what does implementation look like for twenty two brands? Realistically, not the brochure. I've been burned by a brochure before, I'd rather hear the version with the rough edges left in.

[00:37:28] **Sofia Bergström:** Realistically, we would not do twenty two at once and I would push back if you asked. I would do the four largest brands by revenue first, which I assume is most of your footprint.

[00:37:42] **Ylva Sandell:** Would you actually refuse to do all twenty two at once if I insisted?

[00:37:48] **Sofia Bergström:** I'd push back hard, yes, because I've watched it go badly before, twenty two simultaneous onboardings with one person managing all of them tends to produce twenty two mediocre results rather than four excellent ones and eighteen that catch up properly.

[00:38:04] **Ylva Sandell:** The four largest are about sixty percent. I actually checked that figure before this call, I wanted a real answer rather than a guess.

[00:38:14] **Sofia Bergström:** Then those four in eight to ten weeks, the next eight over the following quarter, and the tail after that. You would have a defensible group number covering most of your emissions inside one reporting cycle.

[00:38:29] **Göran Wrede:** And the board sees a genuinely defensible number by when, in that sequence?

[00:38:34] **Sofia Bergström:** Within the eight to ten week window for the sixty percent that matters most, and I'd rather present that honestly as sixty percent well measured and the rest coming than pretend the whole group is finished before it is.

[00:38:50] **Ylva Sandell:** And who does the work? I need to know what I'm actually signing up for in terms of my own hours.

[00:38:58] **Sofia Bergström:** Our implementation team does the modelling. You provide data and make decisions. The thing that consumes your time is not the tool, it is chasing four entities for extracts.

[00:39:10] **Ylva Sandell:** Is there anything I can do in advance to make that chasing faster? I'd rather be prepared than caught out in week two.

[00:39:19] **Sofia Bergström:** Sending each entity a short heads up before the actual request lands tends to help a great deal, purely so it doesn't arrive as a cold ask from a name they don't recognise.

[00:39:33] **Ylva Sandell:** That I already do. That is my whole January.

[00:39:36] **Sofia Bergström:** Then this is at least a version of a task you're already running, not a new one on top of everything else.

[00:39:45] **Ylva Sandell:** That's a fair way to put it, yes. It's the same chase, just for a different reason.

[00:39:52] **Göran Wrede:** What is the number, Sofia? Let's actually get to it rather than keep circling.

[00:39:58] **Sofia Bergström:** For the group, all twenty two brands, corporate footprint, product footprints and supplier engagement, forty two thousand euros a year.

[00:40:06] **Göran Wrede:** Is that inclusive of the supplier engagement work, or does that get added later once you've started?

[00:40:13] **Sofia Bergström:** Inclusive from day one, the whole scope we've discussed today is in that number, nothing held back to be sold to you again in six months.

[00:40:23] **Göran Wrede:** I appreciate hearing that plainly, I've been burned before by a low headline number that turned out to be phase one of three. I'm not naming who, but it was a genuinely frustrating experience. I don't want to relive it here in detail.

[00:40:41] **Sofia Bergström:** That's precisely the pattern I don't want to repeat with you, given everything else we've talked about today. Especially after everything Per has already tested us on. We'd have nowhere to hide if we tried.

[00:40:55] **Göran Wrede:** That is less than I expected. Genuinely, I had a higher figure in my head.

[00:41:01] **Sofia Bergström:** That is a good sentence to hear.

[00:41:04] **Göran Wrede:** It's a good sentence for me to say as well, given I'm the one who has to defend the number internally.

[00:41:12] **Sofia Bergström:** Then we're aligned on that, at least. It makes the rest of the approval process considerably less nerve wracking for me. I'd rather have a predictable process than a fast unpredictable one.

[00:41:25] **Göran Wrede:** It is also less than we pay Per, no offence Per. I'm not sure what that says about our priorities, but there it is.

[00:41:35] **Per Brännström:** None taken. I am more expensive when the data is bad, which is the argument for buying good data.

[00:41:43] **Göran Wrede:** Is that actually true, or is that a line you've refined over the years?

[00:41:48] **Per Brännström:** [laughs] Both, honestly. It's refined because it's true. A clean inventory with a proper audit trail takes me a fraction of the time to sign off compared to one I have to reconstruct myself.

[00:42:02] **Ylva Sandell:** [laughs] Can you put that in writing? I'd frame it and put it on the wall of our office.

[00:42:10] **Per Brännström:** No. Absolutely not.

[00:42:11] **Sofia Bergström:** What are the next steps on your side? I want to understand your process rather than push mine on you.

[00:42:19] **Ylva Sandell:** I write a recommendation. Göran signs off.

[00:42:22] **Sofia Bergström:** Roughly how long does that recommendation typically take you to write, for something at this scope?

[00:42:28] **Ylva Sandell:** A few days, usually, though most of that is gathering the right supporting numbers rather than the writing itself. The writing part is genuinely the fast bit. It goes to the group CFO for anything above forty, so this will just clear the line and he will ask one question.

[00:42:49] **Sofia Bergström:** Has he been involved at all up to this point, or is this his first exposure to it?

[00:42:56] **Ylva Sandell:** First real exposure. He's aware something's been happening, he hasn't seen a number or a recommendation yet.

[00:43:03] **Sofia Bergström:** Which will be?

[00:43:04] **Ylva Sandell:** Whether it replaces anything, always the same question from him regardless of the purchase.

[00:43:10] **Sofia Bergström:** Does he have a strong view either way before he's even heard the answer, or does he genuinely wait to hear it?

[00:43:19] **Ylva Sandell:** He genuinely waits, to be fair to him. He's not trying to kill the purchase, he's trying to understand what it's actually for. I've grown to appreciate that discipline even when it slows things down. It saved us from a bad decision last year, actually. A vendor we almost signed turned out to have exactly the kind of gap Per would have caught.

[00:43:44] **Göran Wrede:** It's a fair question, honestly, even if I'm slightly tired of hearing it.

[00:43:49] **Ylva Sandell:** Whether it replaces anything.

[00:43:51] **Sofia Bergström:** That's a very CFO question, in the best sense, he's asking whether this is incremental cost or a genuine substitution.

[00:43:59] **Ylva Sandell:** He asks that about literally everything. It's actually a good discipline, I've come to appreciate it even when it's inconvenient for what I'm trying to buy.

[00:44:10] **Göran Wrede:** He's saved us from some genuinely bad purchases over the years by asking exactly that question.

[00:44:16] **Sofia Bergström:** Does it? I'd rather you actually answer that than assume the answer for you.

[00:44:22] **Ylva Sandell:** It replaces about two hundred thousand kronor of consultant time and roughly a third of my year.

[00:44:29] **Sofia Bergström:** Is the consultant time a fixed annual retainer, or does it vary year to year?

[00:44:35] **Ylva Sandell:** Fixed retainer, renewed automatically unless somebody actively cancels it, which is exactly the kind of spend that survives review after review simply because nobody questions it.

[00:44:45] **Göran Wrede:** That's worth flagging to the CFO directly, honestly, a fixed retainer nobody's actively evaluated is exactly the kind of spend he'd want surfaced.

[00:44:55] **Sofia Bergström:** Then that is your answer. If it frees up a third of your year and displaces a consultant line, that's not really a hard case to make.

[00:45:06] **Göran Wrede:** Good. Ylva, write it this week.

[00:45:08] **Sofia Bergström:** I'll send the formal proposal today so you have the exact numbers in front of you while you write it.

[00:45:16] **Ylva Sandell:** That would help a great deal, thank you. Having real numbers in front of me makes the whole thing considerably easier to argue for.

[00:45:26] **Göran Wrede:** Get it done properly rather than quickly, Ylva, this is worth doing right.

[00:45:31] **Ylva Sandell:** I will. I'd rather get it in front of him before the next board cycle than have this drag another quarter.

[00:45:40] **Göran Wrede:** Agreed. Let's not let this become another six week story.

[00:45:44] **Ylva Sandell:** I will.

[00:45:45] **Sofia Bergström:** Thank you all. Per, genuinely, thank you, that was the most useful set of questions I have had in a sales meeting.

[00:45:53] **Göran Wrede:** One last thing before we close, Sofia. Does onboarding start before or after the CFO approves the line?

[00:46:01] **Sofia Bergström:** We can start the kickoff conversation before formal sign off, informally, so there's no dead time waiting on paperwork, but nothing touching your systems until the contract is actually signed. That balance tends to work well for accounts your size.

[00:46:17] **Göran Wrede:** That's sensible, thank you. I'd rather not lose weeks to paperwork if we don't have to.

[00:46:23] **Per Brännström:** I'll take that as a compliment, though I'd remind you I'm still not recommending anyone.

[00:46:29] **Sofia Bergström:** I wouldn't expect you to, and I'd trust you less if you suddenly did.

[00:46:35] **Per Brännström:** I will send you an invoice.

[00:46:38] **Ylva Sandell:** [laughs] Of course you will. I wouldn't expect anything less from you.

[00:46:42] **Per Brännström:** Somebody has to pay for the two weeks I lost in March. I intend to bill it properly this time.

[00:46:51] [laughter]

[00:46:54] [Recording ended 00:34:05]

---

**Auto generated summary (not reviewed):**
Nordflor Brands, multi brand food group, 22 brands. Assurance provider present as observer, focused on traceability, restatement handling, locked audit logs and coverage disclosure. Prior year restatement of 14% could not be explained to the board. Four brands on separate ERP systems. Sustainability Director raised public reduction target and absence of abatement planning; agreed to treat as phase two. Quoted 42,000 EUR annually.

**Deal notes added by Sofia Bergström 2026-08-18:**
Strong call. Brännström asked five questions and Tobias answered all five without hedging, and Brännström said out loud that the locked change log is not what he usually gets. That is worth more than anything I could have said.

The thing to watch is Wrede. He asked about the target twice and he asked about the plan, and both times we ended up at phase two. Sandell saved it by saying she cannot plan on averages anyway, which is true. But he said the quiet part clearly: he is worried we will get the data right and then need another tool in eighteen months. I did not have an answer for that and I moved on quickly.

Flagging for whoever owns this account after signature: reduction planning came up in every one of the three meetings. It is not a nice to have for Wrede, it is the thing his CEO has said publicly. Phase two is a promise we have now made twice.
