# Discovery Call: Cardinal Mutual Insurance x Scope Creepers

- **Category:** sales-discovery
- **Date:** 2026-10-06
- **Duration:** 26 min
- **Platform:** Google Meet
- **Call type:** Discovery call 2 of 3 (prospect)

## Attendees

| Name | Company | Role |
|---|---|---|
| Maya Okafor | Scope Creepers | Partner / Account Executive |
| Dev Patel | Scope Creepers | Principal Solutions Engineer |
| Sandra Whitlock | Cardinal Mutual Insurance | Chief Operating Officer |
| Luis Ferreira | Cardinal Mutual Insurance | Claims Operations Manager |
| Harold Brandt | Cardinal Mutual Insurance | Chief Financial Officer |

---

## Transcript

**[00:00:09] Maya Okafor:** Hi everyone. Sandra, Luis, good to see you again.

**[00:00:16] Luis Ferreira:** Hey.

**[00:00:18] Sandra Whitlock:** Hi. So, I've brought a guest. Harold, do you want to introduce yourself?

**[00:00:27] Harold Brandt:** Harold Brandt, CFO. Sandra forwarded me your summary from last month's call. I read it. I have questions.

**[00:00:40] Maya Okafor:** Great, welcome. Questions are why we're here. Dev's with me again.

**[00:00:46] Dev Patel:** Hi Harold.

**[00:00:50] Maya Okafor:** Quick recap so we're all on the same page. Last time Sandra and Luis walked us through email FNOL: about thirty-five percent of claims come in by email, one-forty new claims a day, eighteen minutes each to key, four point one days to first adjuster contact on email versus under a day on phone. Fourteen intake specialists, four lost this year. A TPA for overflow in cat events. And an RPA project a few years ago that didn't work out. Since then Luis sent us a set of redacted sample emails, which were, as promised, ugly.

**[00:01:51] Luis Ferreira:** Told you.

**[00:01:54] Dev Patel:** One of them was a photo of a napkin. I respect it.

**[00:02:00] Maya Okafor:** And Dev put together the outline for measuring accuracy and the review queue mockup. Did that land okay, Luis?

**[00:02:10] Luis Ferreira:** Yeah. I showed two of my people. They liked that they can see why the model picked something. The little highlight on the source document.

**[00:02:26] Harold Brandt:** Can I jump in?

**[00:02:28] Maya Okafor:** Please.

**[00:02:32] Harold Brandt:** I'll be direct, if that's alright. The RPA project. Sandra's summary calls it "a meaningful investment." I approved that investment. It was a lot of money, and I took it on the chin at the board when it didn't work. So I'm going to need you to tell me why this isn't the same thing with a different name on it.

**[00:03:06] Maya Okafor:** That's completely fair, and honestly, it's the right question. Dev, do you want to give Harold the short version?

**[00:03:16] Dev Patel:** Sure. The RPA bots were matching templates. If a form didn't look exactly like the template, the bot failed, usually silently. And Luis told us they also clicked through the claims system's screens, so every patch broke them. What we'd build reads documents more like a person does, so variation doesn't break it. It writes through an API, not the screen. And critically, it reports its own confidence, so when it isn't sure, a human gets it.

**[00:04:12] Harold Brandt:** The RPA vendor also told us it would handle variation.

**[00:04:20] Dev Patel:** That's, yeah. I'm sure they did.

**[00:04:24] Harold Brandt:** So I'm being told the same thing again.

**[00:04:28] Sandra Whitlock:** Harold, it's genuinely different technology. I've seen the demos, Luis has seen them.

**[00:04:38] Harold Brandt:** Sandra, I've seen demos too. I saw demos in 2023.

**[00:04:45] Sandra Whitlock:** Okay, but you can't...

**[00:04:48] Harold Brandt:** I'm not saying no. I'm saying I want proof before money, not money before proof.

**[00:04:58] Maya Okafor:** I think that's a very reasonable position, and it's how we'd structure it anyway. Before any build, a proof on your historical emails. Real FNOL emails, with attachments, run through, compared field by field to what Luis's team actually keyed. You see the accuracy number. If it's not good enough, you walk away.

**[00:05:34] Harold Brandt:** How many emails?

**[00:05:38] Dev Patel:** We'd suggested a few hundred in the outline, because the email-to-claim link is patchy.

**[00:05:46] Harold Brandt:** No. Two thousand. A few hundred tells me nothing about variance.

**[00:05:54] Dev Patel:** Okay. Two thousand. We'll figure out how to get there. Might take some manual matching.

**[00:06:03] Luis Ferreira:** Ugh. Okay.

**[00:06:06] Harold Brandt:** And I want the proof run on our worst data. Not a cherry-picked sample. Not the clean ACORD forms.

**[00:06:16] Dev Patel:** Honestly, we'd prefer that. Pick the ugliest ones you've got.

**[00:06:24] Luis Ferreira:** I can find you some ugly ones. I already did.

**[00:06:30] Harold Brandt:** Not you, Luis. No offense. Someone neutral. Internal audit picks them.

**[00:06:39] Luis Ferreira:** Okay. Fair.

**[00:06:42] Sandra Whitlock:** That's fine. That's good, actually.

**[00:06:46] Maya Okafor:** I like that a lot. It makes the result credible for everyone, including us.

**[00:06:56] Harold Brandt:** Good. Now. The other thing. I'm not interested in "time freed up." I've read a lot of business cases that free up a lot of time and somehow nobody's budget goes down. If this goes anywhere, I want hard savings. Headcount we don't hire. Overflow cost we don't pay. Severity we can actually measure.

**[00:07:32] Maya Okafor:** That's clear. We'd build the ROI on hard savings only, and show anything soft separately so it doesn't muddy the core number.

**[00:07:45] Harold Brandt:** Good. That's how I want it.

**[00:07:50] Sandra Whitlock:** And the severity piece is real, Harold. Four days to first contact. Two percent per day.

**[00:07:58] Harold Brandt:** And that two percent is the actuaries' estimate. I've seen how they build those.

**[00:08:06] Sandra Whitlock:** It's directional.

**[00:08:09] Harold Brandt:** Directional doesn't go in a business case.

**[00:08:15] Maya Okafor:** We can keep severity as upside, clearly labeled. If it's real, it shows up later.

**[00:08:24] Harold Brandt:** Fine.

**[00:08:28] Maya Okafor:** Can I ask a process question? I want to make sure we understand how a decision like this gets made at Cardinal. Last time, Sandra, you mentioned intake is your house.

**[00:08:45] Sandra Whitlock:** It is my house.

**[00:08:48] Harold Brandt:** The operations are your house. The money isn't.

**[00:08:54] Sandra Whitlock:** Harold.

**[00:08:56] Harold Brandt:** I'm just being accurate. Maya asked how it gets made. Anything over two hundred and fifty thousand goes to the budget committee. I chair it. Paul Ingram, our CEO, sits on it, and two board members from the finance committee. Sandra presents, I recommend, the committee decides.

**[00:09:30] Sandra Whitlock:** And Paul is supportive.

**[00:09:34] Harold Brandt:** Paul is supportive. Paul also doesn't override my recommendation. He hasn't in six years.

**[00:09:45] Sandra Whitlock:** That's not, okay, that's fair.

**[00:09:51] Maya Okafor:** That's really helpful, thank you. So if I've got it right: Sandra owns the operational case and sponsors it, and the decision sits with the budget committee, on Harold's recommendation.

**[00:10:09] Harold Brandt:** That's right.

**[00:10:12] Sandra Whitlock:** I'd say I'm the one who brings it, and if I don't bring it, it doesn't happen.

**[00:10:21] Harold Brandt:** That's also right.

**[00:10:24] Maya Okafor:** Understood. Is there anything under that threshold that Sandra can approve on her own? Like a proof?

**[00:10:34] Harold Brandt:** A proof, depending on size, could come out of operations. We'd talk about it.

**[00:10:44] Maya Okafor:** Okay.

**[00:10:46] Sandra Whitlock:** Sorry, Maya. I may have oversold myself last time.

**[00:10:52] Maya Okafor:** Not at all. It's better to know now.

**[00:10:57] Maya Okafor:** Harold, let me ask the question directly, then. What would you need to see? Not "would this work," but specifically, what would make this a yes for you?

**[00:11:12] Harold Brandt:** Hm. The accuracy on the audit sample, first. If that's not good, nothing else matters. Then a business case on hard savings that I believe. And I want to see it compared to the alternatives. I'm sure there are other ways to do this.

**[00:11:39] Sandra Whitlock:** There are. We've had a couple of conversations.

**[00:11:45] Harold Brandt:** Then I want them side by side.

**[00:11:50] Maya Okafor:** That's fine with us. We'll put total cost comparisons in the proposal. You might decide another option is right, and that's okay.

**[00:12:03] Harold Brandt:** I'd appreciate that. Honestly.

**[00:12:08] Maya Okafor:** And in terms of timing, is there a point where this needs to be decided by?

**[00:12:15] Harold Brandt:** Let's talk about timing when I believe the accuracy. Not before.

**[00:12:22] Maya Okafor:** Fair enough. And investment range, same answer?

**[00:12:28] Harold Brandt:** Same answer.

**[00:12:32] Sandra Whitlock:** He means yes, same answer.

**[00:12:36] Maya Okafor:** Ha. Understood.

**[00:12:40] Harold Brandt:** I have a question for Luis, actually, not you. Luis, if this worked, what happens to your fourteen people?

**[00:12:52] Luis Ferreira:** Well, ten now. Plus temps. I'd stop backfilling. And, I mean, honestly I'd move a few of them to subrogation. Subro is buried. We're leaving money on the table there. We've got a backlog of something like nineteen hundred files that nobody's looked at for recovery potential.

**[00:13:27] Harold Brandt:** Nineteen hundred?

**[00:13:30] Luis Ferreira:** Give or take.

**[00:13:32] Harold Brandt:** Why am I hearing about this now?

**[00:13:36] Luis Ferreira:** It's, it's in the monthly ops report. Page eleven.

**[00:13:44] Sandra Whitlock:** It's on page eleven, Harold.

**[00:13:48] Harold Brandt:** Hm. Okay. Well. That's a number I care about. What's the average recovery on a subro file?

**[00:13:58] Luis Ferreira:** On auto, the ones that go anywhere? A few thousand. Probably a third of those are worth pursuing.

**[00:14:10] Maya Okafor:** Interesting. Reviewing a file for subrogation potential is a pretty similar task to intake. Reading the documents, the police report, working out liability. It's not today's scope, but it might be part of the hard-savings story.

**[00:14:36] Harold Brandt:** Don't sell me two things before you've proven one.

**[00:14:42] Maya Okafor:** Ha. Fair. Noted and parked.

**[00:14:46] Sandra Whitlock:** Harold, I'm going to hold you to that "number you care about."

**[00:14:52] Harold Brandt:** I'm sure you will.

**[00:14:57] Dev Patel:** Can I get into the proof logistics for a few minutes? Data is going to be the long pole, not the analysis.

**[00:15:08] Harold Brandt:** Go ahead.

**[00:15:10] Dev Patel:** Three things. Getting two thousand emails with attachments out of Exchange. Linking each one to the claim record so we know what the right answer was. And where the data lives while we work on it.

**[00:15:30] Luis Ferreira:** Getting the emails out, Kevin's team will need to do that. And legal will need to sign off on sending PII outside.

**[00:15:42] Maya Okafor:** We can run the proof inside your cloud environment if that's simpler for legal. Nothing leaves your tenant. Sandra, last time you weren't sure if you're on Azure or AWS.

**[00:15:57] Sandra Whitlock:** Azure. I checked with Kevin.

**[00:16:02] Dev Patel:** Great. That makes it easier. We'd stand up a small environment in your Azure subscription, Kevin's team controls access, and we never take a copy.

**[00:16:16] Harold Brandt:** I like that better.

**[00:16:20] Dev Patel:** On the linking, how does internal audit want to select? Random, or stratified?

**[00:16:28] Harold Brandt:** That's their call. I'd guess they'll want a mix of lines and some cat-event emails.

**[00:16:38] Dev Patel:** Perfect. If they pick from the claims side, starting from claim records and finding the email, the link is solid by construction. That solves most of my problem.

**[00:16:54] Luis Ferreira:** Oh. That's smarter than what I was going to do.

**[00:17:00] Dev Patel:** You'd have done it the hard way and hated me.

**[00:17:04] Luis Ferreira:** Probably.

**[00:17:08] Harold Brandt:** And what do I get at the end? What does the output look like?

**[00:17:14] Dev Patel:** Accuracy per field. Policy number, date of loss, loss location, parties, vehicle, cause of loss, and so on. Straight-through rate at a given confidence threshold. And the error cases, every one, so you can look at what it got wrong and why. Plus a comparison to your team's own error rate, where we can measure it.

**[00:17:46] Harold Brandt:** My team's error rate?

**[00:17:50] Dev Patel:** If a keyer got the date of loss wrong and the model got it right, we'll see it. It cuts both ways.

**[00:17:58] Luis Ferreira:** Oh boy.

**[00:18:02] Sandra Whitlock:** Luis, it's fine.

**[00:18:04] Luis Ferreira:** I know about the hundred and some with the wrong loss date. That's going to be in there, isn't it?

**[00:18:12] Dev Patel:** Only if audit picks them.

**[00:18:16] Harold Brandt:** I'll tell them to pick them.

**[00:18:20] Luis Ferreira:** Great.

**[00:18:24] Maya Okafor:** Luis, one thing from your sample emails I wanted to ask about. A few of them weren't FNOL at all. There was one from a law firm.

**[00:18:36] Luis Ferreira:** Oh, yeah. Attorney letters. Letters of representation, demand letters. They come into claims@ too, and right now they sit in the same queue as everything else. Legal wants them within a day. They don't get them within a day.

**[00:18:58] Maya Okafor:** Okay. Good to know they're mixed in.

**[00:19:03] Luis Ferreira:** Legal complains about it a lot. Nobody's ever asked them what they'd want.

**[00:19:10] Harold Brandt:** Let's keep this about intake.

**[00:19:14] Maya Okafor:** Agreed. For the proof, we'd just recognize them and flag them, not process them.

**[00:19:22] Dev Patel:** Which is useful anyway. If one of those sits in the FNOL queue for four days, that's a cost too.

**[00:19:32] Harold Brandt:** Mm.

**[00:21:06] Maya Okafor:** Harold, last question from me on the decision side. The budget committee. When it looks at something like this, what usually kills a proposal?

**[00:21:20] Harold Brandt:** Soft numbers. A payback period nobody believes. And surprises. If the committee hears about a risk for the first time in the meeting, it's dead.

**[00:21:36] Maya Okafor:** So risks named up front, including the RPA history.

**[00:21:42] Harold Brandt:** Especially the RPA history. Paul will raise it if I don't.

**[00:21:50] Sandra Whitlock:** I'd rather we raise it.

**[00:21:52] Harold Brandt:** On that we agree.

**[00:21:57] Maya Okafor:** Okay. Let me propose next steps. One, we send a short proposal for the proof of value: two thousand historical FNOL emails, selected by internal audit, run inside your Azure tenant, measured field by field against what your team keyed, with the error cases shown in full. Two, a draft ROI framework built only on hard savings, overflow, avoided backfills, with severity shown separately as upside. Three, a technical session with Kevin's team on data access. And four, a side-by-side of the alternatives you're looking at.

**[00:23:00] Harold Brandt:** Good. Send it to Sandra and me both.

**[00:23:06] Sandra Whitlock:** I'll set up Kevin. I'll also talk to legal about the Azure setup.

**[00:23:14] Harold Brandt:** And I'll talk to internal audit about pulling the sample.

**[00:23:20] Maya Okafor:** We'll get the proposal over by the end of next week. Dev, the ROI framework is going to need the real overflow numbers. Sandra, would finance be able to share those?

**[00:23:34] Harold Brandt:** Finance is me. I'll get you the actuals.

**[00:23:40] Maya Okafor:** Perfect. Thank you.

**[00:23:45] Harold Brandt:** I have to drop. Thank you both. That was more useful than I expected.

**[00:23:52] Maya Okafor:** We'll take it.

*[00:23:57 – Harold Brandt left the meeting]*

**[00:24:04] Sandra Whitlock:** So. That was Harold.

**[00:24:09] Maya Okafor:** Honestly, that went well. He's asking the right questions.

**[00:24:15] Sandra Whitlock:** He is. And, okay, I'll own it. I told you last time it was my call. It's my project. It's not my call. Not at that size.

**[00:24:30] Maya Okafor:** That's genuinely helpful. It changes how we write the proposal, in a good way. We'll write it for the committee, not just for you.

**[00:24:42] Sandra Whitlock:** Write it for Harold. If Harold's there, the committee's there.

**[00:24:50] Luis Ferreira:** I think the subro thing actually got him.

**[00:24:54] Sandra Whitlock:** It did. Which is funny, because it wasn't even on the agenda.

**[00:25:02] Luis Ferreira:** I've been telling people about the subro backlog for a year.

**[00:25:08] Sandra Whitlock:** I know, Luis.

**[00:25:12] Dev Patel:** Luis, one practical thing. When audit picks the sample, can you ask them to include some of the follow-up emails too, not just new claims? Even a couple hundred. I'd like to see how routing does.

**[00:25:30] Luis Ferreira:** I'll ask. They might say no.

**[00:25:34] Dev Patel:** That's fine. Worth asking.

**[00:25:39] Maya Okafor:** And Luis, we still want to sit with a couple of your intake specialists before we design anything. I'll send you a few times.

**[00:25:50] Luis Ferreira:** They'd like that.

**[00:25:54] Sandra Whitlock:** Thank you both. Really.

**[00:25:57] Luis Ferreira:** Thanks, guys.

*[Meeting ended at 00:26:02]*
