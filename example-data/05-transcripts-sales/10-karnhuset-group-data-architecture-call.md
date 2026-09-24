# Kärnhuset Group / Rootline — data architecture call

**Date:** 2026-08-21
**Week:** 2026-W34
**Duration:** 31 min 44 sec
**Type:** Sales call, fourth meeting
**Recorded in:** Conversation intelligence tool, auto transcribed, not corrected

**Rootline:** Sofia Bergström (Account Executive), Tobias Rahm (Solutions Engineer)
**Kärnhuset Group:** Madeleine Vinge (Head of Sustainability), Joakim Sten (Group Data and Integration)

---

[00:00:19] **Madeleine Vinge:** Hi both. Joakim is here, he is the one who will tell you this is impossible.

[00:00:38] **Joakim Sten:** [laughs] I will tell you it is possible and expensive.

[00:00:54] **Sofia Bergström:** That is a better starting position than I usually get.

[00:01:07] **Madeleine Vinge:** So, to set the frame. I have run a process like this before at my last company, so I know roughly what I am doing and I know what usually goes wrong.

[00:01:42] **Sofia Bergström:** What usually goes wrong?

[00:01:48] **Madeleine Vinge:** The vendor demos on clean data, we sign, and then five months later we are still arguing about a file format and nobody has produced a number. I have watched that happen twice.

[00:02:29] **Sofia Bergström:** Then let us spend today on the file formats and not on the demo.

[00:02:45] **Madeleine Vinge:** That is why Joakim is here.

[00:02:55] **Joakim Sten:** Okay. So. Kärnhuset is four legal entities and, depending on how you count, four and a half systems.

[00:03:24] **Tobias Rahm:** Tell me the half.

[00:03:30] **Joakim Sten:** The half is a company we bought in 2021 that runs its own instance of the same ERP as the parent but with a different chart of accounts and different material master data. So it is the same product and it may as well be a different system.

[00:04:24] **Tobias Rahm:** That is worse than a different system, honestly, because people assume it will just work.

[00:04:43] **Joakim Sten:** That is exactly what happened. Finance assumed it would just work and we spent a year on it.

[00:05:05] **Tobias Rahm:** What are the other three?

[00:05:12] **Joakim Sten:** The parent runs the main ERP. One entity runs an older Danish system that we are supposed to migrate next year and which we have been supposed to migrate for three years. And the fourth is a small brand with about forty people that runs on a cloud accounting package and a lot of manual work.

[00:06:18] **Tobias Rahm:** And material master data. Is there any group level harmonisation?

[00:06:37] **Joakim Sten:** None. That is the actual problem.

[00:06:50] **Madeleine Vinge:** Explain that properly Joakim, because this is the thing I could not explain to the last vendor.

[00:07:09] **Joakim Sten:** So. If you buy rapeseed oil, the parent has it in the material master as one code with a description in Swedish. The Danish entity has three codes for what is functionally the same thing, in Danish, split by supplier. And the small one does not have a material master at all, they have a supplier invoice with a line that says oil.

[00:08:26] **Tobias Rahm:** And in the group consolidation?

[00:08:35] **Joakim Sten:** In the group consolidation it all lands in a cost account called raw materials and there is no way back.

[00:09:01] **Tobias Rahm:** Right. So you cannot go top down, you have to go entity by entity at the material level.

[00:09:23] **Joakim Sten:** Yes. And that is what everyone gets wrong. They connect to the consolidation because it is the tidy one, and then all you have is money by cost account, and you are back to spend based.

[00:10:07] **Tobias Rahm:** Agreed completely. We would never connect to the consolidation. We connect at entity level, to the purchase ledger and the material master, and we do the mapping in our layer, not in yours.

[00:10:52] **Joakim Sten:** Say that again.

[00:10:58] **Tobias Rahm:** We do not require you to harmonise your material master. We build the mapping on our side, so the three Danish codes and the one Swedish code point to the same underlying material in our model, and your systems stay as they are.

[00:11:52] **Joakim Sten:** Who maintains that mapping?

[00:12:02] **Tobias Rahm:** We build it during implementation and it is visible to you. New materials appear in a review queue and someone maps them, which takes a few minutes a month once it is running.

[00:12:40] **Joakim Sten:** A few minutes a month. That is not what it takes.

[00:12:53] **Tobias Rahm:** For a group your size, with your volume of new materials, I would say fifteen to thirty minutes a month after the first quarter. In the first quarter it is a few hours a week because everything is new.

[00:13:37] **Joakim Sten:** That is a more believable answer.

[00:13:47] **Madeleine Vinge:** Joakim, is this workable?

[00:13:56] **Joakim Sten:** If they genuinely do the mapping on their side, yes. That was the thing that killed the last evaluation. They wanted us to clean our master data first, which is a two year project that nobody will fund.

[00:14:44] **Sofia Bergström:** We would not ask for that and I would be suspicious of anyone who does, because it is not a real requirement, it is a way of moving the hard part onto the customer.

[00:15:22] **Joakim Sten:** [laughs] Yes.

[00:15:29] **Tobias Rahm:** One thing I do need from you though, and it is the one genuine dependency. Quantities. We need volume or weight, not only value. If a purchase line has no quantity, we cannot do anything except spend based for that line.

[00:16:23] **Joakim Sten:** The parent has quantities. Denmark has quantities. The 2021 acquisition has quantities on maybe seventy percent of lines. The small one has almost none.

[00:17:04] **Tobias Rahm:** Then the small one is spend based until it is not, and it is flagged as such.

[00:17:23] **Madeleine Vinge:** How big is the small one in the footprint?

[00:17:33] **Joakim Sten:** Four percent of group revenue. Probably similar in volume.

[00:17:48] **Madeleine Vinge:** Then I can live with that.

[00:17:55] **Tobias Rahm:** And it gives you an argument for fixing it, which you did not have before.

[00:18:14] **Madeleine Vinge:** Can I ask about the acquisition entity specifically, because that is where I expect the fight.

[00:18:36] **Tobias Rahm:** Go ahead.

[00:18:42] **Madeleine Vinge:** They have a sustainability person of their own. She has been doing her own footprint for four years with a consultant, and she is proud of it, and it does not match anything we produce at group.

[00:19:27] **Tobias Rahm:** How far off is it?

[00:19:33] **Madeleine Vinge:** Her number for that entity is about eighteen percent below what our group calculation gives for the same entity.

[00:19:59] **Tobias Rahm:** Do you know why?

[00:20:05] **Madeleine Vinge:** No. And she does not either, she says her method is more accurate because it is bottom up and ours is spend based, which, to be fair, is true.

[00:20:40] **Tobias Rahm:** It may well be true and eighteen percent is still a big gap. My guess, and it is only a guess, is boundary. Either she is excluding a category you include, or she is excluding upstream transport, or there is a co product allocation in there.

[00:21:37] **Madeleine Vinge:** Can you find out?

[00:21:44] **Tobias Rahm:** During implementation, yes, and I would want to. That kind of reconciliation is usually two hours of work and it settles an argument that otherwise runs for years.

[00:22:22] **Madeleine Vinge:** If you settle that argument you will have earned the fee on your own.

[00:22:38] **Tobias Rahm:** [laughs] I will note that down.

[00:22:47] **Madeleine Vinge:** I am half serious. It is a political problem, not a technical one. She thinks group is going to overwrite her work.

[00:23:16] **Sofia Bergström:** Is she going to be part of the implementation?

[00:23:29] **Madeleine Vinge:** She has to be. She is the only person in that entity who understands their materials.

[00:23:48] **Sofia Bergström:** Then I would suggest something. Rather than presenting this as group rolling out a system, we start the implementation with her entity and we treat her as the expert, because she is. If her number and ours reconcile, she becomes the internal proof for everyone else.

[00:24:51] **Madeleine Vinge:** And if they do not reconcile?

[00:25:01] **Sofia Bergström:** Then we find out why in week two rather than in month eight.

[00:25:17] **Madeleine Vinge:** Hm. That is not how I was planning to sequence it. I was going to do the parent first because it is easiest.

[00:25:45] **Sofia Bergström:** The parent will be fine whenever you do it. The risk is not the parent.

[00:26:04] **Madeleine Vinge:** No. The risk is her. Okay, I will think about that. It is a good instinct.

[00:26:27] **Madeleine Vinge:** Sofia, can we talk about what happens after implementation.

[00:18:30] **Sofia Bergström:** Yes.

[00:18:36] **Madeleine Vinge:** Because here is my honest position. Everything Joakim and Tobias have just discussed is plumbing, and plumbing is necessary and I have done it before and I know it takes twice as long as anyone says. What I actually care about is the year after.

[00:19:33] **Sofia Bergström:** Go on.

[00:19:40] **Madeleine Vinge:** Our owners have asked for a reduction pathway. Not a footprint, a pathway. And I have told them they cannot have a pathway until we have a footprint we believe, which bought me about a year, and that year is nearly over.

[00:20:34] **Sofia Bergström:** How specific is the ask?

[00:20:43] **Madeleine Vinge:** Very. They want to see, by 2030, what we intend to do, what it costs, and what it saves. In a table.

[00:21:15] **Sofia Bergström:** Then I have to be direct with you about where we are. We can model scenarios. Change a supplier, change a specification, change a mix, and see the effect on the number. What we do not produce today is a costed abatement plan with a pathway curve. That is on our roadmap and I will not give you a date.

[00:22:28] **Madeleine Vinge:** Okay.

[00:22:35] **Sofia Bergström:** Is that disqualifying?

[00:22:41] **Madeleine Vinge:** No. It is annoying. It is not disqualifying because I have looked at the ones that do produce that table, and the table is built on averages, and I know what that table is worth.

[00:23:25] **Sofia Bergström:** Which is?

[00:23:32] **Madeleine Vinge:** It is worth a nice slide and a conversation in two years about why none of it happened.

[00:23:54] **Sofia Bergström:** [laughs]

[00:24:00] **Madeleine Vinge:** I am serious though. I would rather be able to say to the owners, here are the nine suppliers who account for forty percent of our footprint, here is how they differ, and here is what happens if we move volume between them. That is a plan even if it is not a curve.

[00:25:04] **Sofia Bergström:** That we can do, and we can do it in your first year.

[00:25:17] **Madeleine Vinge:** Then that is what I will present. But Sofia, I want to say this clearly so it is on the record and not a surprise later. I am buying measurement now because I need it. I will be asking you about reduction planning at every review, and if in two years you still do not have it, I will look at whoever does.

[00:26:30] **Sofia Bergström:** That is completely fair and I would rather have it said now.

[00:26:46] **Madeleine Vinge:** Good.

[00:26:52] **Joakim Sten:** Can I ask a security thing before I drop off?

[00:27:05] **Tobias Rahm:** Please.

[00:27:11] **Joakim Sten:** Where is the data hosted and does it leave the EU.

[00:27:24] **Tobias Rahm:** EU region, and no. Sub processors are listed in the DPA and there is one outside the EU for support tooling, which is documented and which you can opt out of.

[00:28:05] **Joakim Sten:** Send me the DPA and the sub processor list and I will run it past our security review. That takes three weeks, so start it now if you want this signed in September.

[00:28:43] **Sofia Bergström:** It goes to you today.

[00:28:50] **Joakim Sten:** Good. Then I am done. Madeleine, from my side it is workable.

[00:29:09] **Madeleine Vinge:** Thank you Joakim.

[00:29:15] [00:29:15 Joakim Sten left]

[00:29:25] **Madeleine Vinge:** That is the first time he has said workable about anything in two years.

[00:29:41] **Sofia Bergström:** [laughs] I will take it. What is left on your side?

[00:29:57] **Madeleine Vinge:** Security review, which Joakim just started. A reference call, ideally with someone who has more than one ERP. And the commercial terms, which I will negotiate, and I will be annoying about it, fair warning.

[00:30:44] **Sofia Bergström:** I would be disappointed otherwise.

[00:30:54] **Madeleine Vinge:** Send me the reference and the paperwork. And Sofia, one small thing. Do not send me a case study PDF. I will not read it. Give me a person and thirty minutes.

[00:31:32] **Sofia Bergström:** Person and thirty minutes. Understood.

[00:09:58] [Recording ended 00:31:44]

---

**Auto generated summary (not reviewed):**
Kärnhuset Group, multi brand group, four entities across four and a half systems with no harmonised material master. Prior evaluation failed because a vendor required master data cleansing as a precondition. Mapping handled in Rootline layer rather than customer systems. One entity lacks purchase quantities, approximately 4% of group. Reduction pathway requested by owners; Rootline does not currently produce costed abatement planning, stated explicitly. Security review initiated.

**Deal notes added by Sofia Bergström 2026-08-21:**
Vinge has done this before and it shows. She ran the meeting, she knew which question killed the last vendor, and she asked for a person rather than a case study.

Two things to record. First, Sten said workable, and Vinge says that is unprecedented, so the integration objection is dead. Second, and this is the important one, Vinge said on the record that she is buying measurement now, will ask about reduction planning at every review, and will go elsewhere in two years if we do not have it. She was not threatening, she was being professional. But it is the second multi brand account this quarter to say the same thing and I want it written down somewhere product will see it.
