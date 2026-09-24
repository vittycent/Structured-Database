# Nordolie AS / Rootline — implementation stall

**Date:** 2026-08-20
**Week:** 2026-W34
**Duration:** 36 min 22 sec
**Type:** Customer success, escalation
**Recorded in:** Conversation intelligence tool, auto transcribed, not corrected

**Rootline:** Petra Nyström (Customer Success Manager), Tobias Rahm (Solutions Engineer)
**Nordolie AS:** Anette Rud (Quality Manager), Bjarte Solstad (Production Manager, joined 00:14)

---

**Auto generated summary:** Escalation call regarding a data quality issue. The customer raised concerns about unit handling in the platform. The issue was investigated and a resolution path was agreed.

---

[00:00:11] **Petra Nyström:** Anette, thank you for staying on for this. I know we have been going back and forth by email and I would rather do this properly, live, with Tobias.

[00:00:23] **Anette Rud:** I appreciate it. I am going to be honest with you, I am at the point where I have stopped opening the account and I do not like being that person.

[00:00:36] **Petra Nyström:** You are not that person, and I would much rather you told me than kept quietly not opening it.

[00:00:43] **Anette Rud:** I nearly did not say it, actually, because it sounds worse out loud than it felt in my head.

[00:00:51] **Petra Nyström:** It does not sound worse to me. It sounds like exactly the thing I need to know, and I would rather hear it in week twelve than not hear it at all.

[00:01:04] **Anette Rud:** I appreciate that.

[00:01:05] **Petra Nyström:** I know, and I am sorry it has taken this long to get you and Tobias in the same room.

[00:01:13] **Tobias Rahm:** Right, let me start by making sure I understand the problem properly, because I have read the email thread three times and I keep getting slightly different versions of it.

[00:01:26] **Anette Rud:** That is because it keeps changing shape. Every time we think we have found the actual thing, there is another layer.

[00:01:34] **Petra Nyström:** How many times has somebody told you it was fixed?

[00:01:38] **Anette Rud:** Three. Once in May, once in June, once about ten days ago.

[00:01:43] **Petra Nyström:** And each time?

[00:01:45] **Anette Rud:** Each time it looked fixed for about a week and then a different number looked wrong. Not the same number. A different one.

[00:01:54] **Petra Nyström:** That must have been maddening.

[00:01:56] **Anette Rud:** It has been more than maddening, if I am honest, it has made me start to wonder whether the whole thing is reliable, and once you start wondering that about one part of a system you start wondering it about all of it.

[00:02:14] **Petra Nyström:** That is a completely fair reaction and I want you to know I have read every one of those threads, not just the most recent one.

[00:02:24] **Anette Rud:** I did not expect that, actually.

[00:02:27] **Petra Nyström:** It is my job to have read them. I am sorry it took this long to get the right person in the room.

[00:02:36] **Tobias Rahm:** Tell me from the beginning. When did you first notice something was wrong?

[00:02:41] **Anette Rud:** May. We loaded the Q1 purchasing data and one of the material lines looked absurd. A crude oil intake that was about four times what it should have been.

[00:02:53] **Tobias Rahm:** Four times.

[00:02:54] **Anette Rud:** Roughly. Enough that even I, who am not a numbers person, could see it was wrong just by looking at the total.

[00:03:03] **Tobias Rahm:** What made you notice it, specifically? I ask because a lot of these errors sit in a total and nobody looks at the total closely enough to catch a factor of four.

[00:03:16] **Anette Rud:** We use the intake figure to sanity check against our finance system, roughly, once a quarter. The finance number and your number should be in the same order of magnitude even though they measure slightly different things, and this one was nowhere close.

[00:03:34] **Tobias Rahm:** That is a genuinely good check and most customers do not do it. You would be surprised how many customers only find out a number is wrong when their auditor asks.

[00:03:46] **Anette Rud:** It is not sophisticated. It is just that our finance director asks me the same question every quarter, does the number make sense, and I have learned to have an answer ready.

[00:03:59] **Tobias Rahm:** It is the single most useful question anybody asks about this kind of data and almost nobody asks it. I am going to start recommending it to other accounts, with your permission.

[00:04:12] **Anette Rud:** Of course. If it helps somebody else avoid three months of this, please use it.

[00:04:19] **Tobias Rahm:** And you flagged it to us.

[00:04:21] **Anette Rud:** I flagged it in May. Somebody looked and said it was a unit mismatch, that the supplier export was in a different unit than we expected, and it would be fixed in the next data load.

[00:04:36] **Tobias Rahm:** Was it?

[00:04:37] **Anette Rud:** No. The next load fixed that line and broke a different one.

[00:04:41] **Petra Nyström:** This is the part I want on the record, because I think it matters. Which line broke the second time?

[00:04:50] **Anette Rud:** Palm kernel. Same kind of thing, a number that was obviously too high, and when I went looking it turned out to be the opposite problem, tonnes reported as kilos rather than kilos reported as tonnes.

[00:05:04] **Tobias Rahm:** So the direction of the error flipped.

[00:05:07] **Anette Rud:** The direction of the error flipped, and I want to say clearly that I do not think anybody is being careless. I think there is something genuinely confusing about our data and I would like to understand what it is rather than keep reporting symptoms.

[00:05:26] **Petra Nyström:** Can I ask, when the first one was reported fixed in May, did anybody explain what had actually been done, or did it just say resolved?

[00:05:36] **Anette Rud:** It said resolved. One line.

[00:05:38] **Petra Nyström:** [pause] That is not good enough and I want to say so directly rather than defend it.

[00:05:45] **Anette Rud:** I appreciate you saying that. I did not want to make a fuss about a one line email, it felt petty, but it genuinely made the second time worse, because I had no idea whether the new problem was related to the old one or completely separate.

[00:06:04] **Petra Nyström:** Which is exactly the thing Tobias is about to walk you through, so at least this time you will know.

[00:06:12] **Tobias Rahm:** That is exactly the right way to think about it, and I am glad you said that, because I want to walk through what I think is actually happening, and it is more interesting than a simple mistake.

[00:06:28] **Anette Rud:** Please.

[00:06:29] **Tobias Rahm:** You buy from three kinds of supplier. Large industrial refiners, who report in metric tonnes, always, without exception. Smaller regional crushers, who report in kilograms because their systems were built for a smaller scale. And then there is one supplier, and I think this is where the real problem is, who reports in a unit called a barrel equivalent, which is a volume measure converted to a notional weight using a density constant that varies by product.

[00:07:00] **Anette Rud:** [pause] That is the one.

[00:07:02] **Tobias Rahm:** That is the one, I would guess.

[00:07:05] **Anette Rud:** How did you know?

[00:07:06] **Tobias Rahm:** Because a density based conversion is the only kind of unit error that would not be consistent. A tonnes to kilos mistake is always off by a factor of a thousand, in one direction, every time. What you are describing, a number that is roughly four times too high and then a different number that is exactly a thousand times off, is two completely different bugs that happen to look similar from where you are sitting.

[00:07:37] **Anette Rud:** Can I check I am following, before you go further. You are saying the reason it kept looking fixed and then breaking again is that we were chasing one symptom at a time, from what were actually two unrelated causes.

[00:07:54] **Tobias Rahm:** Exactly that. Somebody fixed the tonnes and kilos flip in May, which was real and which was fixed properly. I have checked that fix myself today, before this call, specifically so I would not tell you something was resolved without having verified it. Then the barrel equivalent supplier's error surfaced on a different material line and looked, from your side, like the same bug coming back. It was not the same bug. It just happened to produce an equally obviously wrong total.

[00:08:27] **Anette Rud:** So there could be a third one we have not found yet.

[00:08:32] **Tobias Rahm:** There could be, and I do not want to promise you there is not, because that is exactly the kind of promise that got us here three months ago. What I can promise is that I am going to check every supplier feeding this account rather than only the two that have already surfaced. I would rather widen the check now than have you come back to me in October with a third supplier and a third version of this same conversation.

[00:09:06] **Anette Rud:** That is a better promise than the ones we have had so far.

[00:09:11] **Tobias Rahm:** It is a smaller promise and I think that is why it is better. A big promise made under pressure is how you got the one line resolved emails in the first place.

[00:09:24] **Anette Rud:** So it is not one problem.

[00:09:27] **Tobias Rahm:** It is not one problem. It is at least two, possibly three, and I think the reason it has taken three months is that everybody, including us, has been treating it as one.

[00:09:40] **Anette Rud:** That would explain a great deal, honestly.

[00:09:43] [00:14 Bjarte Solstad joined]

[00:09:45] **Bjarte Solstad:** Sorry, sorry, the line at the refinery, do not ask.

[00:09:49] **Petra Nyström:** Not a problem, Bjarte, good timing actually, we are right at the interesting part.

[00:09:55] **Bjarte Solstad:** I read the email chain on the way in, I want to say, so you do not have to catch me up from scratch.

[00:10:04] **Tobias Rahm:** That is helpful, thank you. Where did you land after reading it?

[00:10:09] **Bjarte Solstad:** Confused, honestly, in the same way Anette has been. It reads like three separate problems that somebody has been treating as one. I read it twice and made notes and I still could not tell you with confidence what the actual fix was supposed to be.

[00:10:28] **Tobias Rahm:** [pause] That is a very good summary and it is more or less exactly what I am about to say. You have saved me the introduction.

[00:10:39] **Bjarte Solstad:** Anette said you finally worked out what is wrong.

[00:10:42] **Tobias Rahm:** I have a theory. I want to test it against something you would know better than Anette, which is where the barrel equivalent supplier actually sits in your process.

[00:10:54] **Bjarte Solstad:** That will be the crude palm supplier. Old contract, we have been with them fifteen years, and their invoicing system has never changed because changing it would apparently cost more than the contract is worth.

[00:11:09] **Tobias Rahm:** And when their export comes in, does anybody convert it before it reaches us, or does it arrive as they send it?

[00:11:18] **Bjarte Solstad:** It arrives as they send it. There used to be a conversion step, somebody did it by hand in a spreadsheet, and that person left about two years ago and nobody picked it up because the file kept working, it just stopped being accurate.

[00:11:36] **Petra Nyström:** Who was that person, do you know? Just so I understand the shape of it.

[00:11:42] **Bjarte Solstad:** She was in purchasing. Ran the whole intake reconciliation, spreadsheets for everything, very thorough, and when she left we hired somebody for the role but they were never given the spreadsheet, because nobody thought to hand it over specifically, it was just one of about forty things she did.

[00:12:02] **Tobias Rahm:** Do you still have the old spreadsheet?

[00:12:05] **Bjarte Solstad:** Somewhere. On a shared drive, probably, under her name, in a folder nobody has opened in two years.

[00:12:12] **Tobias Rahm:** That would actually be useful, if you can find it, even if it is out of date, because it would tell me what the conversion logic used to be, which is a faster starting point than working it out from scratch.

[00:12:29] **Bjarte Solstad:** I will look. I cannot promise it is there.

[00:12:32] **Anette Rud:** I can ask the new purchasing person as well, in case anybody ever mentioned it to her informally, even if it was never formally handed over.

[00:12:43] **Petra Nyström:** That is worth doing, because sometimes those things get half passed on in a conversation that nobody thought was important at the time.

[00:12:52] **Bjarte Solstad:** This is starting to feel like an archaeology project rather than a data problem.

[00:12:58] **Tobias Rahm:** [laughter] It quite often is, honestly. A surprising amount of what I do is trying to reconstruct what one person used to know. Companies write down what a system does and almost never write down what a person quietly did to keep it working.

[00:13:16] **Petra Nyström:** [pause] So there was a manual step that quietly stopped happening.

[00:13:21] **Bjarte Solstad:** There was a manual step that quietly stopped happening, and none of us knew, because the file still had numbers in it, they were just the wrong numbers.

[00:13:32] **Tobias Rahm:** That is exactly the shape of bug I would expect. Can I ask, does the density constant vary by product for this supplier, or is it a fixed conversion?

[00:13:44] **Bjarte Solstad:** It varies. Crude is different from refined, and within crude it varies a bit by origin because the impurity content changes the density slightly.

[00:13:54] **Tobias Rahm:** Can you give me a rough sense of the range? I do not need exact figures now, just an order of magnitude.

[00:14:03] **Bjarte Solstad:** Crude from their main origin runs somewhere around zero point nine two to zero point nine four, from memory. If it comes from the secondary origin, which happens maybe a fifth of the time, it can be a bit lower, perhaps zero point nine.

[00:14:21] **Tobias Rahm:** [pause] So a five percent swing depending on origin, on top of whatever the reporting error already is.

[00:14:28] **Bjarte Solstad:** I suppose so, yes, though five percent has never felt like the problem we were chasing, it has felt much bigger than that.

[00:14:37] **Tobias Rahm:** It is, because the origin variation is a real physical fact, it is small and it is not your problem. Your problem is a much larger error sitting on top of it, from the conversion having stopped happening at all. Once we fix the large error, the five percent will still be there, and it is genuine, and it is not worth chasing further than a reasonable default, because five percent on one supplier is well inside what any customer template will tolerate. Chasing the last five percent would cost you more in my time than it is worth in accuracy.

[00:15:19] **Anette Rud:** That is reassuring, actually, because I had assumed we needed to solve all of it perfectly or none of it mattered.

[00:15:27] **Tobias Rahm:** That is a very common assumption and it is nearly always wrong. People assume precision everywhere is the goal, when actually the goal is knowing where the imprecision is and how big it is. Getting the big error out is what matters. The small physical variation underneath it is a rounding question, not a crisis.

[00:15:50] **Tobias Rahm:** [pause] Then this is not a simple fix, and I want to say that plainly rather than promise you something in the next data load and be wrong again.

[00:16:01] **Anette Rud:** Thank you for saying that. Genuinely.

[00:16:04] **Tobias Rahm:** What I would propose is this. We do not try to build an automatic conversion for this one supplier, because a density constant that varies by origin is exactly the kind of thing that goes quietly wrong and nobody notices for two years, which is precisely what just happened to you.

[00:16:25] **Bjarte Solstad:** So what do we do instead?

[00:16:27] **Tobias Rahm:** We ask the supplier to report in tonnes. Directly. It is a request, not a system change on our end, and it removes the conversion step entirely rather than trying to automate something that was already failing when a person was doing it.

[00:16:45] **Anette Rud:** Will they do that?

[00:16:46] **Bjarte Solstad:** [pause] I do not know. Nobody has ever asked them. We have just always taken what they send.

[00:16:54] **Petra Nyström:** That might be worth a phone call rather than an email, given the relationship is fifteen years old.

[00:17:01] **Bjarte Solstad:** I can make that call. I know their commercial director reasonably well.

[00:17:06] **Tobias Rahm:** If they cannot, or will not, there is a second option, which is slower but more defensible. We ask them for the density figures per shipment rather than a single constant, and we build the conversion properly, with the actual number rather than an assumed one, and we flag every one of those rows as converted so that if it is ever wrong again, it is visible rather than hidden inside a total.

[00:17:36] **Anette Rud:** I like that it would be visible.

[00:17:39] **Tobias Rahm:** That is the part that actually matters here, more than getting the number exactly right on the first try. The reason this took three months is that a wrong number looked identical to a right number. If we flag converted rows, the next time something drifts, you will see it in a day rather than a quarter.

[00:18:02] **Petra Nyström:** Can I ask a slightly different question, which is about how this gets reported once it is fixed. Anette, what do you actually need to see, in writing, to feel confident closing this?

[00:18:15] **Anette Rud:** Not just resolved. I need to see which suppliers were affected, what the actual error was for each one, and what changed. I do not need to understand the technical detail the way Bjarte might, but I need more than one line.

[00:18:33] **Petra Nyström:** That is completely reasonable and it is not what you got in May.

[00:18:38] **Anette Rud:** It is not what I got in May, no.

[00:18:42] **Tobias Rahm:** I will write it as a short report rather than a status update. What was wrong, why, what we did, and what changed for you going forward. I will send it to both of you and I am happy to walk through it live if that is useful once it is ready.

[00:19:03] **Bjarte Solstad:** I would want to see it before Anette signs off on it being closed, honestly, because I understand the physical side better than the reporting side.

[00:19:13] **Petra Nyström:** That seems sensible. Should the two of you review it together before it comes back to us?

[00:19:20] **Bjarte Solstad:** We can do that. Give us a day after you send it.

[00:19:25] **Tobias Rahm:** That works. I would rather it be right for both of you than fast for neither. We have already tried fast twice this quarter.

[00:19:35] **Petra Nyström:** Can I ask something about the last three months, because I want to understand what it has actually cost you, beyond the number itself.

[00:19:45] **Anette Rud:** It has cost me trust in the whole account, if I am honest. I do not say that lightly. Not just this supplier. I have started double checking everything, which defeats half the point of buying the system. I bought this specifically so I would not have to be the person checking every number by hand, and for the last three months that is exactly what I have become again.

[00:20:13] **Petra Nyström:** That is a fair and difficult thing to hear.

[00:20:17] **Anette Rud:** It is not personal. I like working with you and I like Tobias. It is that once I found two wrong numbers I stopped trusting the rest, and I do not know how to get that back except time.

[00:20:33] **Petra Nyström:** Does that affect the annual submission? The one for your customer scorecard.

[00:20:38] **Anette Rud:** [pause] It does, actually, and I have not said this to anybody yet. I sent our last submission with a note attached saying two figures had recently been corrected and might move slightly, because I did not want to be caught having sent something I already suspected was wrong.

[00:20:58] **Petra Nyström:** How did that land with the customer?

[00:21:01] **Anette Rud:** They did not reply, which I am choosing to read as fine, though I do not actually know if it is fine.

[00:21:10] **Tobias Rahm:** Once we have the corrected figures, would it help to send a clean restated version, rather than leaving the caveat sitting there?

[00:21:19] **Anette Rud:** Yes. I would like that a great deal, actually. I do not like having sent something with an asterisk on it.

[00:21:27] **Tobias Rahm:** Then that becomes part of the same piece of work. Fix it, document it properly, and give you something clean to send that replaces the caveated version. I will make sure it is dated and clearly marked as a restatement rather than a silent correction, because a silent correction is how a good faith fix starts looking like something being hidden.

[00:21:52] **Anette Rud:** Thank you. That specifically had been sitting with me and I had not raised it because it felt like a separate problem.

[00:22:01] **Petra Nyström:** It is not separate. It is the actual cost of the three months, more than the internal frustration is. The internal frustration is real and it heals. A caveated submission sitting with a customer does not heal on its own, somebody has to go back and fix it.

[00:22:21] **Petra Nyström:** What would help, even a small amount, this month? Not fixing it faster than you can, I am not asking that. I know the fix takes as long as it takes.

[00:22:34] **Anette Rud:** Honestly, exactly what just happened.[pause]  Somebody explaining why it went wrong rather than just fixing it. I do not need it to never break. I need to understand it when it does.

[00:22:47] **Tobias Rahm:** Then let me commit to something specific rather than general. I will send you a written note, this week, that lists every supplier feeding this account, what unit they report in, and whether that unit is fixed or requires a conversion. If a conversion is required, I will say so explicitly and say what assumption it relies on.

[00:23:10] **Anette Rud:** That would help enormously.

[00:23:12] **Tobias Rahm:** And going forward, any converted figure gets a flag on the row, visible to you, not buried in a footnote.

[00:23:20] **Bjarte Solstad:** Can I ask a slightly different question, because I have been sitting here thinking about it. How many of our other suppliers do this? The barrel equivalent thing, I mean, not literally that unit, but some kind of derived measure rather than a direct weight.

[00:23:39] **Tobias Rahm:** [pause] That is a very good question and I do not know the answer for your account specifically, but in my experience it is usually one or two suppliers out of a book this size, and they are almost always the oldest relationships, because the newer ones were set up against a modern export format.

[00:24:01] **Bjarte Solstad:** So it is the fifteen year contract that is the risk, not the newer ones.

[00:24:07] **Tobias Rahm:** In my experience, yes, consistently. The oldest supplier is usually the one still sending you a format from before anybody thought carefully about it.

[00:24:17] **Anette Rud:** Should we go through the rest of our suppliers now, while we have you? Or is that a separate exercise?

[00:24:25] **Tobias Rahm:** I would rather do it properly rather than quickly, because doing it quickly on a call is exactly how the original problem happened, somebody glancing at a unit column and assuming it was right. Speed is what got us here. I am not going to repeat that mistake to make you feel better in the next ten minutes.

[00:24:49] **Anette Rud:** Fair.

[00:24:50] **Tobias Rahm:** What I will do is pull every supplier feeding this account, check the unit against what we hold on file for them, and flag anything that looks like it might be a derived measure rather than a direct weight. That is the note I already promised, I am just expanding what goes in it.

[00:25:11] **Bjarte Solstad:** How long will that take you?

[00:25:14] **Tobias Rahm:** A day, maybe a day and a half, because I want to actually look at recent export files rather than trust what is documented, since what is documented for this account turned out to be wrong.

[00:25:28] **Anette Rud:** That is a better answer than I expected.

[00:25:32] **Tobias Rahm:** It is the only answer I trust after what just happened. I do not want to tell you something is fine because a document says it is fine. That is precisely the habit that cost us three months. Documents lied to us once already this quarter, in a manner of speaking.

[00:25:52] **Anette Rud:** That is slightly funny, in a bleak way. The supplier we trust most because we have known them longest is the one causing the problem.

[00:26:03] **Petra Nyström:** It is a pattern I have seen elsewhere, for what it is worth. Not at this scale, but the shape of it, yes. Trust and data quality are not the same thing and people conflate them constantly.

[00:26:18] **Anette Rud:** I certainly conflated them. I would have told you a month ago that our best supplier relationship was also our best data.

[00:26:27] **Bjarte Solstad:** I would have said the same thing, and I have been buying from them for eleven years.

[00:26:34] **Tobias Rahm:** That is not a criticism of either of you, it is close to universal. I say this on nearly every account I take on. The newer the relationship, the more recently somebody actually specified the data format, so newer often means cleaner, almost by accident rather than by design.

[00:26:54] **Anette Rud:** So the thing that should worry us is not the newest supplier, it is the next oldest one after this one.

[00:27:02] **Tobias Rahm:** That is exactly the right instinct, and it is precisely why I want to check all four rather than stop at the one that happened to surface first. Waiting for the next one to surface on its own is how this whole three months happened in the first place.

[00:27:22] **Tobias Rahm:** It is nearly always backwards. The supplier you trust most is the one nobody has audited in years, precisely because you trust them. Auditing them would feel, to most people, like an accusation, so nobody does it until something forces the question.

[00:27:39] **Anette Rud:** Does that mean we should be looking harder at our other long term suppliers? Not just this one.

[00:27:47] **Petra Nyström:** I think it is worth a light pass, yes, not a full audit, just a check of when each supplier's export format was last reviewed.

[00:27:57] **Bjarte Solstad:** We have four suppliers we have used for more than ten years. This one is the oldest, but not by much.

[00:28:06] **Tobias Rahm:** I would include all four in the note I am already writing. It is not much more work to check four exports than two, and it means you are not back here in six months with the same conversation about a different supplier.

[00:28:23] **Anette Rud:** I would genuinely rather know now than find out the way we found out this time.

[00:28:30] **Tobias Rahm:** Understood. I will treat it as five suppliers rather than one, and flag anything that looks like a derived measure across all of them. I would rather over deliver on this one, given where we are starting from. You have earned that much after three months.

[00:28:49] **Bjarte Solstad:** Thank you. That is more thorough than I expected from what was supposed to be a call about one bad number. I genuinely thought this was going to be a twenty minute apology.

[00:29:02] **Tobias Rahm:** It started as a call about one bad number and turned out to be about how the whole intake process was set up fifteen years ago and never revisited. That happens more often than customers expect.

[00:29:17] **Petra Nyström:** Anette, can I ask where this leaves you, going into the autumn. Is this the kind of thing that changes how you feel about the account generally, or is it contained to this one issue?

[00:29:31] **Anette Rud:** [pause] I want to say contained. I am not going to pretend I am not tired of it. Three months of a number that keeps being wrong in a different way each time is exhausting in a way that is hard to explain to somebody who has not lived through it.

[00:29:52] **Petra Nyström:** I believe you.

[00:29:53] **Anette Rud:** But the explanation just now, the actual mechanism, that has done more for my confidence than the fix will, honestly. I understand why it happened. I did not understand that before.

[00:30:06] **Petra Nyström:** Can I ask what would have helped earlier? Not to relitigate it, genuinely so I do it differently for the next account this happens to.

[00:30:16] **Anette Rud:** [pause] Getting Tobias on a call in May rather than in August. I do not think anybody was hiding anything from me, I think it went through two or three people before it reached somebody who could actually explain the mechanism, and each handoff lost a bit of the explanation.

[00:30:36] **Petra Nyström:** That is fair and I am going to think about that specifically, because it is a process question rather than a Tobias question.

[00:30:46] **Anette Rud:** It is not a complaint about any one person. It is that a one line resolved email is what happens when the person answering does not actually understand what was wrong, and I think that is what happened twice before today.

[00:31:02] **Tobias Rahm:** That is probably an accurate read. I was not on either of the first two threads.

[00:31:09] **Petra Nyström:** Which is exactly the gap. I am going to change how these get escalated so a data quality issue that recurs gets a technical person on it by the second occurrence rather than the third. I do not have a formal process for that today, which is itself a gap, and I am going to fix it rather than just apologise for this one instance. An apology does not stop it happening to the next customer.

[00:31:40] **Anette Rud:** I would have appreciated that a great deal.

[00:31:43] **Tobias Rahm:** I am going to send that supplier note today, and I would like a follow up in two weeks specifically on this, separate from your normal check in, just to close it out properly.

[00:31:57] **Anette Rud:** Should Bjarte be on that follow up as well, or just the two of us?

[00:32:03] **Petra Nyström:** I would include Bjarte if he is able, given how much of the technical detail lives with him rather than with you. Two of you catching an error is better than one.

[00:32:16] **Bjarte Solstad:** I can do two weeks. Put it in the calendar and I will move things around it.

[00:32:23] **Tobias Rahm:** I will send an invite alongside the supplier note, so it is not a separate thing you have to remember to ask for. Fewer things for either of you to hold in your head is the whole point at this stage.

[00:32:40] **Anette Rud:** Yes. I would like that.

[00:32:42] **Petra Nyström:** Bjarte, will you make the call to the supplier this week?

[00:32:47] **Bjarte Solstad:** I will call them Thursday. I want to think about how to ask it, because if I ask badly it sounds like an accusation and they have been good to us for fifteen years.

[00:33:01] **Petra Nyström:** Would it help if we drafted something together, rather than you writing it alone?

[00:33:06] **Bjarte Solstad:** It might. I know the relationship, you know how to ask the technical part of the question.

[00:33:13] **Tobias Rahm:** I can send you three sentences by tomorrow that explain what we need and why, in plain language, and you can wrap it in whatever context makes sense for your relationship with them.

[00:33:27] **Bjarte Solstad:** That would take the worst part off my plate. The worst part is not the ask, it is worrying about how it lands.

[00:33:36] **Tobias Rahm:** It should land fine. Most suppliers their size already report in tonnes to their other customers, this one just never got asked. I have seen this exact conversation happen at four other accounts this year alone and every one of them said yes within a week. It sounds like a bigger ask than it actually is, once somebody finally makes it.

[00:34:01] **Bjarte Solstad:** [pause] That is actually reassuring. I had assumed it would be a genuine change for them.

[00:34:08] **Tobias Rahm:** It might be a genuine change for how they report to you specifically, but it is very unlikely to be a genuine change to how they hold the data internally. Systems that size are almost never built around one customer's export preference, they are built around their own production planning, which is nearly always metric. Most systems this size already have it in tonnes somewhere, they have just been exporting it to you in whatever their old format happens to be.

[00:34:41] **Tobias Rahm:** I can help with the wording if that is useful. It is a very normal request, most of our newer accounts ask for it from day one, it is only unusual here because the relationship predates the question.

[00:34:56] **Bjarte Solstad:** That would help. Send me something and I will make it my own.

[00:35:01] **Petra Nyström:** Right. Supplier note this week, follow up in two weeks, Bjarte's call Thursday. Anette, anything else before we close?

[00:35:09] **Anette Rud:** Just one thing, and it is not about this issue specifically. I want to say that Tobias explaining the mechanism today has changed how I feel about raising things in future. I was starting to feel like reporting a problem was pointless because nothing came back that helped me understand it.

[00:35:30] **Petra Nyström:** I am glad you said that, and I am sorry it took three attempts to get here.

[00:35:37] **Anette Rud:** It got here. That is what matters now.

[00:35:40] **Bjarte Solstad:** Thank you both, genuinely. I came into this call expecting to be annoyed for half an hour and I am not.

[00:35:49] **Petra Nyström:** I will take that as a win, given where we started.

[00:35:53] **Anette Rud:** No. Thank you both. This is the first time in three months I have come off a call about this feeling better rather than worse.

[00:36:04] **Petra Nyström:** That is exactly what I wanted to hear and I am sorry it took three months to get here.

[00:36:11] **Anette Rud:** It is what it is. Thank you for taking it seriously today.

[00:36:16] [Recording ended]

---

**CSM notes, Petra Nyström, 2026-08-20:**

Nordolie. Unit conversion issue, three months old, escalated properly today for the first time with Tobias in the room rather than handled by email.

Root cause is more interesting than it looked from the outside. Not one bug, at least two: a straightforward tonnes/kilos flip on one supplier, and a genuinely hard problem on their oldest supplier, whose export uses a density based volume-to-weight conversion that used to be done by hand in a spreadsheet by somebody who left the company two years ago. The manual step quietly stopped and nobody noticed because the numbers kept arriving, they were just wrong.

Tobias proposed asking the supplier to report in tonnes directly rather than building an automatic conversion, since the density constant varies by product and origin, which is exactly the kind of thing that fails silently. Bjarte is calling the supplier's commercial director Thursday. Fallback is converting properly with real density data and flagging every converted row visibly, so a future drift is caught in a day rather than a quarter.

Anette's language is worth recording precisely. She said she has stopped opening the account, and separately that finding two wrong numbers made her stop trusting the rest, which defeats half the point of buying the system. What actually moved her in this call was not the fix, it was the explanation. Her words: I understand why it happened, I did not understand that before.

Flagging for the file because I think it generalises. She said her best supplier relationship, fifteen years, was also assumed to be her best data, and it was backwards: nobody had ever questioned that supplier's export precisely because the relationship was trusted. Tobias said this is consistent across accounts, that the oldest supplier is usually the one still on a format from before anybody thought carefully about it, and that trust and data quality get conflated constantly.

This is loud and it is one account. I do not think it is a pattern yet, I think it is a genuinely hard technical edge case that happened to a vocal customer with a fifteen year old supplier relationship. Worth watching whether it recurs elsewhere before treating it as anything more than that.

Follow up booked in two weeks, separate from her normal check in.
