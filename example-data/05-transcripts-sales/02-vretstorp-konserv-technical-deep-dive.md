# Vretstorp Konserv / Rootline — technical deep dive

**Date:** 2026-08-31
**Week:** 2026-W36
**Duration:** 34 min 12 sec
**Type:** Sales call, second meeting
**Recorded in:** Conversation intelligence tool, auto transcribed, not corrected

**Rootline:** Erik Lindqvist (Account Executive), Tobias Rahm (Solutions Engineer)
**Vretstorp Konserv:** Ann-Sofie Berg (Sustainability Coordinator), Krister Malm (Sourcing Manager, joined 00:09), Torsten Blom (Operations Director, joined 00:21, left 00:31), Cecilia Rung (joined at start, role not stated)

---

[00:00:11] **Erik Lindqvist:** ...there we go. Can you hear me now?

[00:00:11] **Erik Lindqvist:** Cecilia, good morning, thanks for joining as well.

[00:00:11] **Cecilia Rung:** Morning.

[00:00:14] **Ann-Sofie Berg:** Yes, now it is fine. Something with the headset.

[00:00:18] **Erik Lindqvist:** Happens to everyone. Good morning Ann-Sofie. How is Karlshamn?

[00:00:21] **Ann-Sofie Berg:** Wet. Very wet. We had water in the loading area on Saturday which is not, you know, not what you want.

[00:00:30] **Erik Lindqvist:** Water in the loading area, that is a bad Monday. Was it the rain or was it something of yours?

[00:00:38] **Ann-Sofie Berg:** The rain. It comes off the field behind us and there is a drain that has never been big enough, and every four or five years it reminds us. Torsten has been asking for that drain since before I started.

[00:00:54] **Erik Lindqvist:** Did you lose anything?

[00:00:55] **Ann-Sofie Berg:** No. Two hours and some very unhappy drivers. But it is the third thing this year, and it puts everyone in a mood where a new system is not what they want to hear about.

[00:01:09] **Erik Lindqvist:** Should we have moved this?

[00:01:11] **Ann-Sofie Berg:** No, no. Honestly it is easier for me to get people into a call than into a room, and Krister is never in the building anyway.

[00:01:22] **Erik Lindqvist:** Where is he?

[00:01:23] **Ann-Sofie Berg:** This week? Poland, I think, or he was. He buys, so he travels, and I get him for twenty minutes at a time between things.

[00:01:33] **Erik Lindqvist:** That is worth knowing for how we run this. If he is a twenty minute person then we should never plan anything that needs him for an hour.

[00:01:44] **Ann-Sofie Berg:** Nothing has ever needed him for an hour. He would not come.

[00:01:49] **Erik Lindqvist:** No. Not ideal. Okay so, Tobias is here with me, he is our solutions engineer, he is the one who actually knows how the thing works. I mostly talk.

[00:02:01] **Tobias Rahm:** Hi Ann-Sofie.

[00:02:02] **Ann-Sofie Berg:** Hi. Good. So Krister said he would join, he has something running until quarter past, and Torsten wanted to come in for a bit at the end if that is okay.

[00:02:14] **Erik Lindqvist:** That is more than okay. Torsten is operations?

[00:02:17] **Ann-Sofie Berg:** Operations director, yes. He is the one who has to say yes to anything with a number on it, so.

[00:02:25] **Erik Lindqvist:** Understood. Then let me suggest we do this. Thirty minutes, I want to spend maybe five recapping what you told us last time so Tobias has it from you and not from my notes, then Tobias shows you the actual product on your kind of data, and then we leave time at the end for Torsten and for what happens next. Does that work?

[00:02:51] **Ann-Sofie Berg:** That works.

[00:02:52] **Erik Lindqvist:** Great. So. Last time you said the thing that started all of this was the deforestation regulation, the EUDR, and specifically the palm and the soy you bring in for the blends. Is that still the pressure or has something else come on top?

[00:03:09] **Ann-Sofie Berg:** No, that is still it. But it has, how do I say, it has grown. Because when we started looking at what we would need for EUDR we realised we do not really have anything for the rest either. So it started as palm and soy and now it is, okay, what about everything.

[00:03:31] **Erik Lindqvist:** Right.

[00:03:32] **Ann-Sofie Berg:** And then in June we got a request from one of the big groups, one of our customers, they want product level numbers for four of our products. In their template. Which is a spreadsheet with about two hundred rows and I do not understand half of it.

[00:03:50] **Tobias Rahm:** Do you know which framework their template follows?

[00:03:53] **Ann-Sofie Berg:** I do not. It says something at the top, I can send it to you.

[00:03:59] **Tobias Rahm:** Please do, that would help. Nine times out of ten it is one of three formats and we already export to all three.

[00:04:09] **Ann-Sofie Berg:** Okay. Good. Because right now what happens is, I take our purchase data, I have an Excel where I have built, I don't know, it is quite big now, and I multiply the spend by factors I found in a public database, and then I fill in the gaps with assumptions.

[00:04:29] **Erik Lindqvist:** And how do you feel about the number that comes out of that?

[00:04:34] **Ann-Sofie Berg:** [laughs] How do I feel about it.

[00:04:37] **Erik Lindqvist:** Honest answer.

[00:04:38] **Ann-Sofie Berg:** I don't know if the number I sent them last year was right. That is the honest answer. I sent it. Nobody came back and asked anything. But if someone had asked me to show where a number came from I would have had a problem, because it came from an average of everything in that category across, I think, Europe. And we are not the average of everything in Europe.

[00:05:06] **Erik Lindqvist:** That is the thing we hear most often, for what it is worth.

[00:05:11] **Ann-Sofie Berg:** It does not make me feel better.

[00:05:14] **Erik Lindqvist:** No, fair. Tobias, do you want to pick up on the data side, because Ann-Sofie, the other thing you mentioned last time was the co op.

[00:05:24] **Ann-Sofie Berg:** Yes. So for the rapeseed, most of it comes through a cooperative. And the cooperative gives me an average across their whole membership. So I get one number for rapeseed and that is it. It does not matter which farm, which practice, whether they use cover crops, whether it is drained peat or not, I get one number.

[00:05:48] **Tobias Rahm:** And your customer is asking you to differentiate.

[00:05:51] **Ann-Sofie Berg:** My customer is asking me to tell them why our oil is better than someone else's oil, which I believe it is, but I cannot show it. So we look the same as everyone.

[00:06:04] **Tobias Rahm:** Can I ask about the cooperative, because it is going to come back later and I would rather understand it now. When they give you the average, is it an average of the whole membership or of the volume they sold you?

[00:06:21] **Ann-Sofie Berg:** The whole membership. I asked that once. It is the same figure they give everybody.

[00:06:27] **Tobias Rahm:** So two competitors buying from the same co op publish the same rapeseed number.

[00:06:33] **Ann-Sofie Berg:** Yes. Which is either fair or completely useless depending on which day you ask me.

[00:06:39] **Tobias Rahm:** And do they tell you which farms your volume came from?

[00:06:43] **Ann-Sofie Berg:** No. And I do not think they know, in the sense that it goes into a silo.

[00:06:50] **Erik Lindqvist:** Does the co op have any appetite to change that?

[00:06:54] **Ann-Sofie Berg:** There is a project. There has been a project for two years. Somebody presents it at the annual meeting and then nothing happens until the next annual meeting.

[00:07:05] **Tobias Rahm:** That is very common and it usually moves when one of their big buyers makes it a condition rather than a request.

[00:07:14] **Ann-Sofie Berg:** We are not big enough to make it a condition.

[00:07:18] **Erik Lindqvist:** Your customer might be.

[00:07:20] **Ann-Sofie Berg:** [pause] That is an interesting thought and I do not know what to do with it.

[00:07:26] **Ann-Sofie Berg:** Can I ask something else about the co op, because there is a thing in the customer's letter I have not understood. They want us to have a target eventually. And the letter says the agricultural part has to be handled separately, as its own commitment, with its own coverage.

[00:07:46] **Tobias Rahm:** That is right, and for you it is most of the footprint.

[00:07:51] **Ann-Sofie Berg:** So if my rapeseed is one number from a co op that covers four hundred farms, and I cannot say which of those farms grew what I bought, what is my coverage?

[00:08:04] [pause]

[00:08:07] **Tobias Rahm:** That is a very good question and the honest answer is that a co op average is not primary data for this purpose, it is a supplier specific average, and depending on how it is derived it may not count towards the coverage you need.

[00:08:25] **Ann-Sofie Berg:** May not.

[00:08:26] **Tobias Rahm:** I would want to check rather than tell you yes or no on a call. But you should assume it is a problem rather than assume it is fine.

[00:08:37] **Ann-Sofie Berg:** So the thing I have been treating as solved, because I get a number every year without asking, is actually the thing that is not solved.

[00:08:48] **Erik Lindqvist:** That is often how it goes. The line nobody worries about is the line with no evidence behind it, precisely because it arrives on time.

[00:08:58] **Ann-Sofie Berg:** [pause] I am going to need to write that down and then decide whether to tell anybody.

[00:09:04] **Erik Lindqvist:** Okay, that is, I think that is the whole thing right there. Tobias, can you share?

[00:09:11] **Tobias Rahm:** Yes, one second. Can you see the screen?

[00:09:14] **Ann-Sofie Berg:** I see a login page.

[00:09:16] **Tobias Rahm:** Yes, hold on. There we go. Okay. So this is a demo environment, it is built on a company we made up that looks a bit like you, oils and fats, three sites, about the same import profile you described. So the numbers are not yours but the shape is yours.

[00:09:36] **Ann-Sofie Berg:** Okay.

[00:09:37] **Tobias Rahm:** So the first screen is the corporate footprint. Scope one, two, three. This is the part every tool does, I am not going to spend long here, but the difference is what sits underneath scope three. If I click into purchased goods and services...

[00:09:54] **Ann-Sofie Berg:** That is the big one for us.

[00:09:57] **Tobias Rahm:** It is the big one for everyone in food. It is usually somewhere between eighty and ninety five percent of the total. So, if I click in, you see it is broken down by material, not by supplier spend. Rapeseed oil, palm, soy, sunflower, packaging, energy.

[00:10:16] **Ann-Sofie Berg:** Mm.

[00:10:17] **Tobias Rahm:** And each of those, if I open rapeseed, is broken down again by origin and by production practice.

[00:10:23] **Ann-Sofie Berg:** Where does that come from?

[00:10:25] **Tobias Rahm:** Two places. Public LCA databases for the baseline, and then licensed agricultural data from partners for the granularity. The partner data is the part you cannot get yourself. It is what lets us say a rapeseed grown in Skåne under one set of practices and a rapeseed grown in northern France under another are not the same number.

[00:10:48] **Ann-Sofie Berg:** And if I do not know the practice?

[00:10:52] **Tobias Rahm:** Then you get the regional default, and the interface tells you that is what you are looking at. It is flagged. Which matters, because when your auditor asks, you can say this line is primary, this line is regional default, this line is a global average, and here is why.

[00:11:12] **Ann-Sofie Berg:** Okay. That is, yes. That would be, that is useful.

[00:11:16] **Erik Lindqvist:** Sorry, Krister has joined I think.

[00:11:18] **Krister Malm:** Hello. Sorry. I am here. I have maybe twenty minutes.

[00:11:22] **Erik Lindqvist:** No problem at all Krister, good to meet you. Very short version, we are looking at how Vretstorp Konserv would produce emissions numbers that hold up, and Tobias is showing the product. Ann-Sofie, do you want to say why Krister is here?

[00:11:38] **Ann-Sofie Berg:** Because everything I need comes from Krister's suppliers.

[00:11:42] **Krister Malm:** [laughs] Yes. And I will say now, before we go further, I am not sending my suppliers another survey.

[00:11:49] **Erik Lindqvist:** Okay.

[00:11:50] **Krister Malm:** I am serious. We did this two years ago. Someone in the group sent out a questionnaire, forty suppliers, and I think three answered. Three. And then I spent the next month on the phone apologising to people I have worked with for fifteen years, explaining that no, this does not affect their contract, no, we are not auditing them.

[00:12:14] **Erik Lindqvist:** That is a completely reasonable position.

[00:12:16] **Krister Malm:** These are relationships, not accounts. I know their kids' names. I am not turning that into a compliance exercise because someone in Stockholm wants a spreadsheet filled in.

[00:12:27] **Tobias Rahm:** Can I ask what the questionnaire actually asked for?

[00:12:31] **Krister Malm:** I do not remember exactly. Emissions data. It was long.

[00:12:35] **Tobias Rahm:** Right. So, two things and then I will drop it. First, the reason response rates are that low is almost always that the supplier has no idea what is being asked and no way to answer it, so they ignore it. Second, when we do this the request goes out with the specific fields, in their language, with a deadline that is realistic, and it goes out under your name, not ours, unless you want it the other way.

[00:13:06] **Krister Malm:** Under our name.

[00:13:07] **Tobias Rahm:** Under your name. And they get something back, which is the part that changes the number. They get their own footprint for what they sell you, which most of them have never had, and which their other customers are also going to start asking for.

[00:13:25] **Krister Malm:** Hm.

[00:13:26] **Erik Lindqvist:** Krister, honestly, if you tell us no on that module we will still do everything else. It is not a condition.

[00:13:34] **Krister Malm:** No, I hear you. I am not saying no. I am saying I have been burned. Let me see what it looks like.

[00:13:43] **Tobias Rahm:** Let me actually show you something else first, because I think it is more relevant to you than the supplier piece. Ann-Sofie, can I use the product view?

[00:13:55] **Ann-Sofie Berg:** Go ahead.

[00:13:56] **Tobias Rahm:** So this is a product footprint. One SKU. In this case a blended cooking oil, because that is close to something you make. And what you get is the recipe, ingredient by ingredient, with the contribution of each one to the total.

[00:14:12] **Ann-Sofie Berg:** So the packaging is, what is that, eleven percent?

[00:14:16] **Tobias Rahm:** Eleven point four. And everyone always guesses packaging is the problem and it almost never is. The problem is nearly always the agricultural input. Here it is seventy eight percent, all of it in the oils.

[00:14:30] **Ann-Sofie Berg:** Right.

[00:14:31] **Ann-Sofie Berg:** While the packaging line is on the screen. Is any of this connected to the new packaging rules?

[00:14:38] **Tobias Rahm:** Connected how?

[00:14:39] **Ann-Sofie Berg:** There is something starting in October about what is allowed in food packaging. Our bottle supplier has sent us two letters about it and our technical manager forwarded both to me, and I do not know why they came to me.

[00:14:55] **Tobias Rahm:** They came to you because you are the sustainability person and it has the word packaging in it.

[00:15:02] **Ann-Sofie Berg:** [laughs] Yes. That is exactly why.

[00:15:05] **Tobias Rahm:** To be straight with you, no. What is on this screen is the carbon of your packaging materials. It will not tell you whether a bottle or a closure is compliant with a chemical restriction, and I would not want you to leave this call thinking it will.

[00:15:24] **Ann-Sofie Berg:** So who does that?

[00:15:25] **Erik Lindqvist:** Your supplier, mostly, and then somebody at your end has to keep the declarations. It is a quality job rather than a carbon job.

[00:15:35] **Ann-Sofie Berg:** It is going to end up being my job.

[00:15:39] **Krister Malm:** It is going to end up being your job.

[00:15:42] **Ann-Sofie Berg:** Thank you Krister.

[00:15:43] **Tobias Rahm:** Now. This is the part I actually wanted to show you. This SKU uses palm oil, and we have two suppliers for it in this demo, both of them supplying the same specification, same grade. If I split the line by supplier...

[00:16:00] [pause]

[00:16:03] **Tobias Rahm:** Supplier A, and supplier B. Same ingredient. Same spec. One is roughly two point one times the other.

[00:16:11] [pause]

[00:16:14] **Krister Malm:** Say that again.

[00:16:15] **Tobias Rahm:** Same ingredient, same specification, two suppliers, and one carries roughly double the footprint of the other. Because of where it is grown and what was there before it was grown.

[00:16:27] **Krister Malm:** Explain the double to me properly. Because if I take that to a supplier I need to be able to say why, and "your oil is worse" is not something I can say to a man I have bought from for nine years.

[00:16:44] **Tobias Rahm:** Then do not say the oil is worse, because that is not what it says. Most of that gap is not how the crop was farmed. It is the land.

[00:16:56] **Krister Malm:** Meaning what.

[00:16:57] **Tobias Rahm:** Meaning that if the plantation sits on land that was converted from forest inside the accounting window, the carbon released by that conversion is attributed to what grows there afterwards, spread across twenty years.

[00:17:11] **Krister Malm:** Twenty years.

[00:17:12] **Tobias Rahm:** Twenty years. So a decision made in 2012 is still in a 2026 number, and neither you nor your supplier made it.

[00:17:20] **Krister Malm:** [pause] So supplier B is not doing anything wrong.

[00:17:24] **Tobias Rahm:** Supplier B may be doing everything right and still carry twice the number, yes. That is the uncomfortable part and I would rather you heard it from me than found it out in a meeting with him.

[00:17:39] **Krister Malm:** Then what am I actually buying when I pick supplier A?

[00:17:43] **Tobias Rahm:** You are buying a supply chain with less land conversion history in it. Which is a real thing, and it is worth real money to your customer, and it is not a compliment to supplier A's farming.

[00:17:58] **Ann-Sofie Berg:** Does it ever go the other way? Does a number get worse without anybody doing anything?

[00:18:04] **Tobias Rahm:** Yes. Three ways. The window moves as years pass. The mapping data improves and reclassifies a parcel. Or the convention itself gets revised, which has happened twice in the time I have been doing this.

[00:18:18] **Ann-Sofie Berg:** So I could publish a number this year and have it be different next year with nothing changed at our end.

[00:18:27] **Tobias Rahm:** You could, and you should expect to, and the only protection is being able to show what moved and why.

[00:18:35] **Ann-Sofie Berg:** [pause] That happened to us. Two years ago, with the palm. The number changed and I could not explain it and I told Torsten it was a database update, which was true and sounded like an excuse.

[00:18:49] **Erik Lindqvist:** Did he accept it?

[00:18:51] **Ann-Sofie Berg:** He accepted it. He has not entirely forgotten it.

[00:18:55] **Krister Malm:** I remember that. I remember because you were quite upset about it and I did not understand why at the time.

[00:19:03] **Krister Malm:** And you can do that for anything?

[00:19:06] **Tobias Rahm:** For anything where we can resolve the origin, yes. Which for oils is very good coverage.

[00:19:12] **Krister Malm:** Can you do it for the whole book?

[00:19:15] **Tobias Rahm:** What do you mean by the whole book?

[00:19:19] **Krister Malm:** I mean everything I buy. I have, what, Ann-Sofie, ninety, ninety five active suppliers?

[00:19:24] **Ann-Sofie Berg:** About that.

[00:19:25] **Krister Malm:** Because I am sitting in a tender in November. And if I could go into that tender and say, these two offers are eleven öre apart on price and one of them is half the carbon, that is a conversation I have never been able to have. Nobody has ever given me that.

[00:19:46] **Erik Lindqvist:** Krister, that is exactly what it does.

[00:19:49] **Krister Malm:** Because right now the only thing I have is price and reliability. Sustainability is something Ann-Sofie does after I have already bought.

[00:19:58] **Ann-Sofie Berg:** That is true, actually.

[00:19:59] **Krister Malm:** It is completely true. I buy, and then six months later she asks me what I bought.

[00:20:06] **Tobias Rahm:** Yes. So, to answer properly, the whole book is a bigger exercise than four products. For the top suppliers by volume we can get you there quickly because it is mostly origin data you already have in your ERP. The long tail takes longer and some of it you will never get below a regional average, and that is fine as long as it is labelled.

[00:20:33] **Krister Malm:** Before November?

[00:20:34] **Tobias Rahm:** For your top, I would guess, twenty suppliers by spend? Yes. Comfortably.

[00:20:38] **Krister Malm:** Okay. That is interesting. That is more interesting than I expected, I will be honest.

[00:20:44] **Erik Lindqvist:** [laughs] I will take that.

[00:20:46] **Ann-Sofie Berg:** Can I ask something about the comparison. If our supplier says their number is X and your database says it is Y, who wins?

[00:20:56] **Tobias Rahm:** Primary data from the supplier wins, if it is documented and if the method is one we can check. If they just send a number with nothing behind it, we will show it next to ours and flag the difference. We do not silently overwrite. That would be the worst possible thing to do to you in an audit.

[00:21:19] **Ann-Sofie Berg:** Okay. Good.

[00:21:20] [00:21:23 Torsten Blom joined]

[00:21:23] **Torsten Blom:** Hello, sorry, is this the carbon thing?

[00:21:25] **Ann-Sofie Berg:** This is the carbon thing.

[00:21:27] **Erik Lindqvist:** Hi Torsten, Erik from Rootline. We are about twenty minutes in, Tobias has been showing the product. Do you want the short version of where we are?

[00:21:38] **Torsten Blom:** Please.

[00:21:39] **Erik Lindqvist:** Vretstorp Konserv has a deforestation regulation obligation on palm and soy, a customer asking for product level numbers on four products, and a corporate footprint that is currently built in a spreadsheet from spend data. We would replace all three of those with one system, and the differentiator for you specifically is that we can tell two suppliers of the same input apart, which Krister just said would change how he runs a tender.

[00:22:08] **Torsten Blom:** Krister said that?

[00:22:09] **Krister Malm:** I said it was interesting.

[00:22:11] **Torsten Blom:** [laughs] From him that is a standing ovation. Okay. My question is a boring one. We looked at another one of these, I forget the name, Ann-Sofie?

[00:22:22] **Ann-Sofie Berg:** Verdanta.

[00:22:23] **Torsten Blom:** Verdanta, yes. Why not them.

[00:22:24] **Erik Lindqvist:** Straight answer? They are a good product and they cover every industry. If you were a company with a big office estate and a vehicle fleet and food was a third of your footprint, I would tell you to look hard at them. For you, ninety percent of your emissions are in agricultural inputs, and generalist tools model agriculture as a category average. They will tell you rapeseed oil is rapeseed oil. We will not.

[00:22:54] **Torsten Blom:** And on the software itself? Because Ann-Sofie showed me a screenshot from them and it was, I mean, it looked nice.

[00:23:02] **Erik Lindqvist:** It does look nice. Ours looks like it was designed by people who care more about the model than the interface, which is accurate, because it was. We have a rebuild in progress. I am not going to pretend the interface is our strength.

[00:23:20] **Torsten Blom:** Okay. Appreciated. That is a better answer than I usually get.

[00:23:24] **Ann-Sofie Berg:** Torsten, honestly, I do not care what it looks like if the numbers survive.

[00:23:30] **Torsten Blom:** No, agreed. Next question then. We get the numbers. Then what? Because the board is going to ask what we are doing about it, not what it is.

[00:23:41] **Erik Lindqvist:** So there is a reduction planning piece in the platform where you can model scenarios, switch a supplier, change a practice, see what happens to the number.

[00:23:52] **Torsten Blom:** But is that the same standard as the measurement?

[00:23:56] **Erik Lindqvist:** It is earlier. It is on the roadmap to go deeper. What I would say is that in food, the reduction levers are almost entirely in sourcing, and the thing that unlocks them is knowing which supplier is which. So the measurement is not separate from the reduction, it is the precondition for it.

[00:24:17] **Torsten Blom:** Mm. Okay. I will take that for now.

[00:24:20] **Ann-Sofie Berg:** [inaudible] the tender though.

[00:24:22] **Torsten Blom:** Sorry?

[00:24:23] **Ann-Sofie Berg:** I said, the tender though. If Krister can use it in November that is a reduction, right there, and it is this year.

[00:24:32] **Torsten Blom:** That is a fair point.

[00:24:34] **Torsten Blom:** One more and then I will stop being difficult. If we buy this, who at Vretstorp Konserv runs it? Because Ann-Sofie is one person and she already does the audits.

[00:24:45] **Ann-Sofie Berg:** I run it.

[00:24:46] **Torsten Blom:** That is what I thought you would say and it is what worries me.

[00:24:52] **Erik Lindqvist:** It is a fair worry and I will not pretend it away. What I would say is that the shape of the work changes rather than the amount. Ann-Sofie stops building a spreadsheet from scratch every spring, which by her own account is weeks, and starts reviewing something that is already built, which is days.

[00:25:14] **Ann-Sofie Berg:** It is three weeks. It was three weeks last year and it was four the year before because of the palm thing.

[00:25:23] **Torsten Blom:** I did not know it was three weeks.

[00:25:26] **Ann-Sofie Berg:** You did not ask. It happens in July and you are always somewhere else in July.

[00:25:32] **Torsten Blom:** [laughs] That is true.

[00:25:34] **Erik Lindqvist:** The other thing, and this is the part people underestimate, is that the questions currently come to Ann-Sofie because she is the only place they can go. Once there is a system with published figures in it, some of those questions get answered by somebody else looking them up.

[00:25:54] **Torsten Blom:** Would Krister use it?

[00:25:55] **Krister Malm:** If it tells me which of two offers is cheaper on carbon, I will use it in November and I will use it in every tender after that. If it asks me to fill anything in, I will not.

[00:26:11] **Tobias Rahm:** That is a completely reasonable deal and it is the deal.

[00:26:15] **Torsten Blom:** Right. And the board question. You said reduction is earlier than measurement. Give me the version I would say to them.

[00:26:24] **Erik Lindqvist:** The version I would say is that in oils and fats you cannot reduce what you cannot see, and nobody in this market can currently see below the category. The first year buys you sight. The second year buys you decisions, and the first of those decisions is the November tender, which is this year and not next.

[00:26:47] **Torsten Blom:** That is a better sentence than the one you gave me two minutes ago.

[00:26:52] **Erik Lindqvist:** It is, and Ann-Sofie wrote it, I just repeated it.

[00:26:56] **Ann-Sofie Berg:** I did write it.

[00:26:58] **Torsten Blom:** Then Ann-Sofie should come to the board meeting.

[00:27:01] **Ann-Sofie Berg:** [pause] I would like that.

[00:27:03] **Erik Lindqvist:** Should we talk about what it costs and what happens next, while Torsten is here?

[00:27:09] **Torsten Blom:** Yes, that is mostly why I came.

[00:27:12] **Erik Lindqvist:** So for a company your size, corporate footprint, product footprints, and the supplier module, you are looking at somewhere in the mid twenties in euros per year. I will send an exact figure this week once I know how many products you want modelled, because that is the variable.

[00:27:32] **Torsten Blom:** Per year.

[00:27:33] **Erik Lindqvist:** Per year, annual contract.

[00:27:34] **Torsten Blom:** And implementation?

[00:27:35] **Erik Lindqvist:** Included. Six to eight weeks typically. Faster if your ERP export is clean, and I have no idea yet whether it is.

[00:27:44] **Ann-Sofie Berg:** It is not.

[00:27:45] **Tobias Rahm:** It never is.

[00:27:46] **Torsten Blom:** [laughs] Okay. I need to go, I have a thing. Ann-Sofie, you decide, come to me with a number. Nice to meet you both.

[00:27:56] **Erik Lindqvist:** Thanks Torsten.

[00:27:57] [00:28:00 Torsten Blom left]

[00:27:59] **Tobias Rahm:** Ann-Sofie, one thing I want to check before we talk about next steps, because it changes the estimate. The four products your customer asked for. Are they four recipes or four article numbers?

[00:28:12] **Ann-Sofie Berg:** Four article numbers. Two of them are the same blend in different bottles.

[00:28:17] **Tobias Rahm:** Then it is three recipes and a packaging variant, and the variant is an afternoon rather than a week.

[00:28:25] **Ann-Sofie Berg:** That is useful. I have been quoting four to Torsten.

[00:28:29] **Tobias Rahm:** Quote him four and deliver four. I am telling you so you know what it costs us, not so you can promise less.

[00:28:38] **Ann-Sofie Berg:** [laughs] Understood.

[00:28:39] **Erik Lindqvist:** And the two hundred row template. Ann-Sofie, when you send it, can you send it as it arrived rather than the version you have started filling in?

[00:28:50] **Ann-Sofie Berg:** Why the original?

[00:28:51] **Erik Lindqvist:** Because the parts you have left blank tell us more than the parts you have completed. The blanks are where their template does not fit a company like yours, and that is what we need to see.

[00:29:06] **Ann-Sofie Berg:** [pause] There are a lot of blanks.

[00:29:08] **Erik Lindqvist:** Good.

[00:29:09] **Ann-Sofie Berg:** There is a whole section on land that I have not touched at all, because I did not know what to put and the guidance note is in English and it is nine pages.

[00:29:22] **Tobias Rahm:** Send that section first, then.

[00:29:24] **Ann-Sofie Berg:** It is the section I have been avoiding since June.

[00:29:28] **Tobias Rahm:** It is the section that matters and it is almost certainly why they picked those four products, because three of them are blends with imported oil in them.

[00:29:40] **Ann-Sofie Berg:** [pause] I had not connected those two things.

[00:29:43] **Krister Malm:** Which three?

[00:29:44] **Ann-Sofie Berg:** The two blends and the frying oil.

[00:29:46] **Krister Malm:** All palm.

[00:29:47] **Ann-Sofie Berg:** All palm.

[00:29:48] **Krister Malm:** Then it is not a carbon request, it is a palm request wearing a carbon coat.

[00:29:54] **Erik Lindqvist:** That is a very good instinct and it is worth testing before you answer it, because it changes what a good answer looks like.

[00:30:04] **Ann-Sofie Berg:** How would I test it?

[00:30:06] **Erik Lindqvist:** Ask her which of the four she needs first. If the answer is the three blends, you have your answer.

[00:30:14] **Erik Lindqvist:** Okay. Ann-Sofie, Krister, what do you need from us to move this forward?

[00:30:19] **Ann-Sofie Berg:** I need to see it with our data. Not a demo company. Ours.

[00:30:24] **Erik Lindqvist:** We can do that. What we would need is a spend export from the ERP for one year, and the recipe or specification for two or three products. Not all four, two or three is enough to show you.

[00:30:40] **Ann-Sofie Berg:** The specs are in a different system and I do not have access.

[00:30:45] **Krister Malm:** R and D has them.

[00:30:47] **Ann-Sofie Berg:** R and D has them and R and D is, you know. Busy.

[00:30:52] **Erik Lindqvist:** How long does it usually take to get something out of them?

[00:30:57] **Ann-Sofie Berg:** If I ask nicely and it is not a busy week, maybe two weeks. If I ask in November, no chance, the whole department is inside the tender.

[00:31:08] **Erik Lindqvist:** Then let us ask this week. And Krister, would it help if we did the supplier comparison on your actual top twenty rather than the demo? Because then you have something real before the tender.

[00:31:22] **Krister Malm:** That would help, yes. I can get you the supplier list and the origins. The origins are in the system for most of them. Some of them, we buy through traders, and then I know the trader and not the farm.

[00:31:39] **Tobias Rahm:** That is normal. We can work with the trader and flag it as lower resolution.

[00:31:45] **Krister Malm:** Fine. I can do that by, let us say, end of next week.

[00:31:50] **Krister Malm:** One thing on the supplier list before I go. When I send you the top twenty, some of those origins are going to be wrong.

[00:32:00] **Tobias Rahm:** Wrong how?

[00:32:01] **Krister Malm:** Wrong in the sense that the field says Malaysia because the contract says Malaysia, and the trader may have sourced it somewhere else that season. It is not fraud, it is how the market works.

[00:32:15] **Tobias Rahm:** That is genuinely useful to know before we start rather than after. We will treat trader supplied origins as declared rather than verified and mark them differently.

[00:32:25] **Krister Malm:** How many of mine will end up in that box?

[00:32:29] **Ann-Sofie Berg:** Half?

[00:32:30] **Krister Malm:** Not half. A third. The direct ones I know.

[00:32:33] **Tobias Rahm:** A third declared is a normal starting point and it improves every year, because once you start asking, the traders who can answer start answering.

[00:32:43] **Krister Malm:** And the ones who cannot?

[00:32:45] **Tobias Rahm:** Tell you a story about commercial sensitivity.

[00:32:48] **Krister Malm:** [laughs] Yes. I have heard that story.

[00:32:51] **Erik Lindqvist:** Perfect. So, actions. Ann-Sofie sends us the customer template. Ann-Sofie chases R and D for two or three product specs. Krister sends the top twenty supplier list with origins. We come back with your data in the product, and I send a firm price this week. Sound right?

[00:33:10] **Ann-Sofie Berg:** Sounds right.

[00:33:11] **Krister Malm:** Yes. I have to run.

[00:33:13] **Erik Lindqvist:** Thanks Krister, genuinely useful to have you on.

[00:33:16] **Krister Malm:** Mm. Bye.

[00:33:17] [00:33:20 Krister Malm left]

[00:33:19] **Ann-Sofie Berg:** He liked it.

[00:33:21] **Erik Lindqvist:** I could not tell at all.

[00:33:23] **Ann-Sofie Berg:** No, he did. He asked a second question. He does not do that.

[00:33:28] **Erik Lindqvist:** [laughs] Good to know. Ann-Sofie, one last thing while I have you. When you take this internally, who else needs to be comfortable?

[00:33:37] **Ann-Sofie Berg:** Torsten, who you met. And finance will want to know it is not a five year thing. And IT will send a form.

[00:33:47] **Erik Lindqvist:** There is always a form. We have a completed one, I will send it with the price so you can hand it straight over.

[00:33:52] **Cecilia Rung:** Is the agreement per entity, or could a second company be added later at a rate rather than as a new contract?

[00:33:59] **Erik Lindqvist:** [pause] Per entity as it stands, though we can usually add an entity to an existing agreement at an incremental rate if the structure makes sense. Is that something relevant here?

[00:34:08] **Cecilia Rung:** Just understanding the structure. Thank you.

[00:33:56] **Ann-Sofie Berg:** That would save me a week.

[00:33:59] **Erik Lindqvist:** Then that is what we will do. Thank you both, this was a good call.

[00:34:05] **Ann-Sofie Berg:** Thank you. Bye.

[00:34:06] [Recording ended 00:34:12]

---

**Auto generated summary (not reviewed):**
Vretstorp Konserv evaluating carbon accounting driven by EUDR obligations on palm and soy plus a customer request for product level data. Currently spreadsheet based on spend. Key discussion around supplier level granularity. Competitor Verdanta mentioned. Next steps agreed on data exchange and pricing.

**Deal notes added by Erik Lindqvist 2026-08-31:**
The supplier comparison is what did it. Nobody asked for it, it was not in discovery, it was not in the deck. Tobias put two lines on the screen and Malm stopped the call. Ten seconds of silence and then he asked if we could do it for ninety five suppliers before a tender in November. That is the whole deal. Also note Blom asked "then what" about reduction and I gave the roadmap answer. It landed okay because Ann-Sofie saved me with the tender point, but I would not want that question from a bigger account. One more thing, a person called Cecilia Rung was on from the start, introduced by nobody, said almost nothing the whole call, and asked a contract question near the end about whether a second entity could be added to this agreement at a rate rather than as a new contract. Not a consultant's question. I do not know who she is.
