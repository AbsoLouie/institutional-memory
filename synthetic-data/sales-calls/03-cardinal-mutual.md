# Discovery Call: Cardinal Mutual Insurance x Scope Creepers

- **Category:** sales-discovery
- **Date:** 2026-10-14
- **Duration:** 34 min
- **Platform:** Google Meet
- **Call type:** First discovery call (prospect)

## Attendees

| Name | Company | Role |
|---|---|---|
| Maya Okafor | Scope Creepers | Partner / Account Executive |
| Dev Patel | Scope Creepers | Principal Solutions Engineer |
| Sandra Whitlock | Cardinal Mutual Insurance | Chief Operating Officer |
| Luis Ferreira | Cardinal Mutual Insurance | Claims Operations Manager |
| Harold Brandt | Cardinal Mutual Insurance | Chief Financial Officer (joined at ~00:13) |

---

## Transcript

**[00:00:05] Sandra Whitlock:** Hi, hi. Sorry, I was in another Meet and it wouldn't let me leave.

**[00:00:12] Maya Okafor:** No worries at all. Hi Sandra. Hi Luis.

**[00:00:18] Luis Ferreira:** Hey, good afternoon.

**[00:00:20] Dev Patel:** Afternoon.

**[00:00:24] Sandra Whitlock:** Harold is going to try to join, our CFO. He's stuck in a budget review, so he'll pop in late. Fair warning, he's, uh. He's going to have opinions.

**[00:00:40] Maya Okafor:** Ha. That's fine, we like opinions. How's the week going?

**[00:00:48] Luis Ferreira:** Busy. We had hail in the northern territory two weeks ago, so we're still working through about eleven hundred claims from that one event.

**[00:01:02] Maya Okafor:** Oh wow. That's actually a perfect place to start. Sandra, can you give us the context for why we're talking?

**[00:01:14] Sandra Whitlock:** Sure. So Cardinal writes personal and commercial lines, mostly auto and homeowners, some small commercial. We're in seven states. About two hundred and eighty thousand policies in force. Claims volume in a normal year is around forty-two thousand claims. In a cat year it's much more.

**[00:01:47] Maya Okafor:** And the focus is first notice of loss.

**[00:01:52] Sandra Whitlock:** Right. Intake. FNOL. Luis, you want to describe the fun?

**[00:02:00] Luis Ferreira:** Yeah. So we get claims in, uh, five ways. Phone, the web portal, the mobile app, agents emailing us, and then direct email from policyholders. Phone's about thirty-five percent. Portal and app maybe thirty. And then email, between agents and policyholders, is about thirty-five, and that's the problem child.

**[00:02:37] Dev Patel:** What makes email the problem?

**[00:02:40] Luis Ferreira:** It's unstructured. An agent sends us an email that says "see attached," and the attachment is a scanned ACORD form, or a photo of a handwritten note, or a police report PDF, plus twelve phone photos of a bumper. Somebody on my team has to open everything, figure out the policy number, figure out who's involved, what happened, the date of loss, the location, and key it all into Guidewire. Well, our claims system. It's an older version.

**[00:03:29] Maya Okafor:** How many people do that?

**[00:03:32] Luis Ferreira:** Fourteen intake specialists. On a normal day they're handling around six hundred emails, but a lot of those are follow-ups on existing claims, which is a different flow. New FNOL by email is maybe one-forty a day. Average handling time is eighteen minutes per new claim. Longer if it's a multi-vehicle.

**[00:04:07] Dev Patel:** And the follow-ups? What happens with those?

**[00:04:13] Luis Ferreira:** They have to be matched to the claim and routed to the adjuster. That's like, three minutes each, but there's four hundred-something a day. And they get mis-routed a lot. I'd say five to eight percent end up with the wrong adjuster.

**[00:04:37] Maya Okafor:** What's the downstream cost of that? Of the delays?

**[00:04:43] Sandra Whitlock:** So this is, for me, this is the real issue. Our cycle time from FNOL to first contact by an adjuster is averaging four point one days on email claims. On phone claims it's under one. And first contact time is directly correlated with severity. The longer a claim sits, the more expensive it gets. Rental days pile up, attorneys get involved.

**[00:05:23] Luis Ferreira:** Attorney rep rate is the big one.

**[00:05:27] Sandra Whitlock:** Right. Our actuaries estimate, on the bodily injury side, every day of delay to first contact adds about two percent to average severity. I'm not going to pretend that's precise. But it's directionally the number.

**[00:05:49] Maya Okafor:** And CSAT, I'm assuming?

**[00:05:53] Sandra Whitlock:** J.D. Power score dropped last year. Claims satisfaction is our weakest category. And our independent agents complain about it constantly. Agents are our distribution. If agents are annoyed, they place business elsewhere.

**[00:06:17] Maya Okafor:** That's a growth problem, not just an ops problem.

**[00:06:22] Sandra Whitlock:** Exactly. That's how I've been framing it to the board.

**[00:06:28] Dev Patel:** Luis, during cat events, what happens?

**[00:06:34] Luis Ferreira:** We pull people from other departments. Underwriting assistants, customer service. Everybody gets a crash course on intake, and the quality goes way down. We had one person last spring key in a hundred and some claims with the wrong loss date because they misread the format.

**[00:07:03] Sandra Whitlock:** And we pay a TPA for overflow. That's expensive. Last year overflow was about six hundred and forty thousand.

**[00:07:16] Maya Okafor:** Okay, that's a hard number. Thanks.

**[00:07:20] Dev Patel:** What does the policyholder see on the email side? Do they get an acknowledgment?

**[00:07:27] Luis Ferreira:** Auto-reply. "We got your email." That's it. No claim number until someone keys it in. So they call. Which adds to phone volume.

**[00:07:42] Dev Patel:** Ah, so it's a loop.

**[00:07:44] Luis Ferreira:** It's a loop.

**[00:07:48] Maya Okafor:** Sandra, I should ask, has Cardinal tried to solve this before?

**[00:07:55] Sandra Whitlock:** Um. Yes. And this is going to come up the second Harold joins, so I'll just say it. In 2023 we did an RPA project. Bots for intake. Template-based extraction from ACORD forms and auto-routing. We spent, I think all in it was around nine hundred thousand with the vendor and licensing.

**[00:08:30] Luis Ferreira:** It worked on about twenty percent of emails.

**[00:08:36] Sandra Whitlock:** It worked on the clean ones. The problem was nothing is clean. Agents use different ACORD versions, they scan them crooked, they handwrite. And every time the bots broke, somebody on Luis's team had to fix them, and eventually it was more work than it saved.

**[00:09:02] Luis Ferreira:** We turned the last bot off in February.

**[00:09:07] Dev Patel:** That's a really common story with template-based extraction. The difference with a language model is it's not matching a template. It reads the document the way a person would. So a crooked scan of an older ACORD version, or a handwritten note, or an email that just says "my wife backed into a pole in the Kroger lot on Tuesday," it can pull the structure from any of those.

**[00:09:42] Luis Ferreira:** Including photos?

**[00:09:46] Dev Patel:** Including photos. It can describe the damage, identify the vehicle, read a license plate, flag if a photo looks like it's from a different vehicle than the one on the policy. That last one's interesting for SIU.

**[00:10:06] Luis Ferreira:** Oh, SIU would love that. They've been asking for photo screening forever.

**[00:10:16] Maya Okafor:** SIU is your special investigations unit?

**[00:10:19] Luis Ferreira:** Yeah. Fraud. They're a team of six and they basically only see what adjusters flag to them. They'd love something upstream.

**[00:10:32] Maya Okafor:** I'll note that.

**[00:10:36] Sandra Whitlock:** Let's not boil the ocean. Intake first.

**[00:10:40] Maya Okafor:** Agreed. So, if intake worked the way you wanted, what does that look like?

**[00:10:49] Sandra Whitlock:** An email comes in, within minutes the claim is created in the system with all the fields filled out, the photos are attached and tagged, the policyholder gets a real claim number back, and it's routed to the right adjuster based on line, severity, and geography. And a human only touches it if something's uncertain.

**[00:11:22] Luis Ferreira:** And my team becomes, like, the exception handlers. Not keyers.

**[00:11:30] Dev Patel:** What fraction would you be happy with going straight through?

**[00:11:35] Luis Ferreira:** Honestly? If sixty percent goes straight through with good accuracy, I'd throw a party.

**[00:11:44] Sandra Whitlock:** I'd want seventy.

**[00:11:48] Luis Ferreira:** Sandra wants seventy.

**[00:11:50] Sandra Whitlock:** I want seventy.

**[00:11:54] Dev Patel:** Ha. Both reasonable. The thing I'd add is that the accuracy bar matters more than the percent. You want the model to know when it's not sure. A confident wrong answer on a date of loss is worse than kicking it to a human.

**[00:12:16] Luis Ferreira:** Yes. That was the RPA problem. The bots didn't know they were wrong.

**[00:12:23] Maya Okafor:** Can I ask about the claims system? You mentioned it's an older version.

**[00:12:31] Luis Ferreira:** It's a few major versions behind. We're supposed to upgrade.

**[00:12:38] Sandra Whitlock:** The upgrade is scheduled for 2028. It's a big project. IT has told me not to build anything that depends on the current version's APIs too heavily.

**[00:12:53] Dev Patel:** That's good to know. We'd want a thin integration layer, so the extraction and routing logic doesn't care which version it's writing to. Then when you upgrade, you swap the connector.

**[00:13:11] Sandra Whitlock:** That'd keep IT happy.

**[00:13:15] Maya Okafor:** Who in IT should we be talking to?

**[00:13:19] Sandra Whitlock:** Kevin Marsh, he's our VP of IT. He's supportive but stretched. The upgrade is eating his team.

**[00:13:30] Maya Okafor:** Okay.

*[00:13:34 – Harold Brandt joined the meeting]*

**[00:13:37] Harold Brandt:** Afternoon. Sorry. Where are we?

**[00:13:43] Sandra Whitlock:** Hi Harold. We've gone through the current state. Luis walked through the volumes. We were just talking about what good looks like.

**[00:13:54] Harold Brandt:** Okay. Hi. Harold Brandt, CFO. I'll be direct, if that's alright.

**[00:14:01] Maya Okafor:** Please.

**[00:14:03] Harold Brandt:** We spent nine hundred thousand dollars on automation three years ago and it didn't work. I approved that. I don't intend to approve the same thing with a different name on it. So what I'd like to understand is why this is different, and what it costs, and how quickly I see the money back.

**[00:14:31] Maya Okafor:** That's completely fair, and honestly, it's the right question. Dev was just touching on the difference. Dev, do you want to give Harold the short version?

**[00:14:44] Dev Patel:** Sure. The short version is the RPA bots were matching templates. If a form didn't look exactly like the template, the bot failed, usually silently. What we'd build reads documents more like a person does, so variation doesn't break it. And critically, it reports its own confidence, so when it isn't sure, a human gets it. We'd measure it against Luis's team on real historical emails before it touches anything live.

**[00:15:26] Harold Brandt:** The RPA vendor also told us it would handle variation.

**[00:15:32] Dev Patel:** That's, yeah. I'm sure they did.

**[00:15:36] Harold Brandt:** So I'm being told the same thing again.

**[00:15:39] Sandra Whitlock:** Harold, it's genuinely different technology. I've seen the demos, Luis has seen them.

**[00:15:47] Harold Brandt:** Sandra, I've seen demos too. I saw demos in 2023.

**[00:15:52] Sandra Whitlock:** Okay, but you can't...

**[00:15:54] Harold Brandt:** I'm not saying no. I'm saying I want proof before money, not money before proof.

**[00:16:03] Maya Okafor:** I think that's actually a very reasonable position, and we'd structure it that way anyway. Before any build, we'd run a proof on your historical emails. Say, two thousand real FNOL emails from last year, with the attachments. We run them through, compare the output to what Luis's team actually keyed, and you see the accuracy number. If it's not good enough, you've spent a small amount and you walk away.

**[00:16:42] Harold Brandt:** What's a small amount?

**[00:16:44] Maya Okafor:** For a proof of that size, typically between forty and seventy-five thousand, depending on how much data prep is involved.

**[00:16:57] Harold Brandt:** And then the actual build?

**[00:17:01] Maya Okafor:** I'd want to be careful. It depends on integration, how many lines of business, how much of the routing logic. A first production phase, email FNOL for auto, is in the range of three to five hundred thousand for our services. Plus model costs, which at your volume would be, Dev?

**[00:17:30] Dev Patel:** Ballpark, low tens of thousands a year. Probably under thirty.

**[00:17:38] Harold Brandt:** Three to five hundred thousand is half to more than half of what we lost last time.

**[00:17:47] Sandra Whitlock:** And the TPA overflow alone was six-forty last year, Harold.

**[00:17:53] Harold Brandt:** The overflow is variable, Sandra. That was a bad cat year.

**[00:17:58] Sandra Whitlock:** Three of the last four have been bad cat years.

**[00:18:02] Harold Brandt:** Mm.

**[00:18:05] Luis Ferreira:** Can I say something? Um. My team is fourteen people and I've lost four of them this year. Two went to a competitor's claims department, one to a bank. I've been backfilling with temps. Temps make more mistakes. Every new hire takes three months to train on intake. That's not on any spreadsheet but it's real.

**[00:18:37] Harold Brandt:** I understand that, Luis. Truly. But turnover is an HR problem. I don't want to fix an HR problem with a half-million-dollar software project.

**[00:18:52] Sandra Whitlock:** It's not just turnover. It's severity. Four days to first contact. Two percent per day.

**[00:19:01] Harold Brandt:** And that two percent is the actuaries' estimate. I've seen how they build those.

**[00:19:08] Maya Okafor:** Harold, can I ask, what would you need to see? Not "would this work," but specifically, what numbers would make this a yes for you?

**[00:19:23] Harold Brandt:** Hm. Payback inside eighteen months. Hard savings, not soft. I don't want "time freed up." I want either headcount we don't hire, or overflow cost we don't pay, or severity we can actually measure.

**[00:19:45] Maya Okafor:** That's helpful. And clear.

**[00:19:49] Harold Brandt:** And I want the proof run on our worst data. Not a cherry-picked sample. I'll pick the emails.

**[00:19:58] Dev Patel:** Honestly, we'd prefer that. Pick the ugliest ones you've got.

**[00:20:04] Luis Ferreira:** I can find you some ugly ones. Trust me.

**[00:20:09] Harold Brandt:** Not you, Luis. Someone neutral. Internal audit.

**[00:20:15] Luis Ferreira:** Okay. Fair.

**[00:20:19] Sandra Whitlock:** That's fine. That's good, actually.

**[00:20:22] Maya Okafor:** I like that a lot. It makes the result credible for everyone.

**[00:20:28] Harold Brandt:** Who else are you talking to? Are we being compared?

**[00:20:33] Sandra Whitlock:** Our claims system vendor has an AI intake module. It's only available on the new version, which is 2028 for us. And there's an insurtech that does FNOL as a service, it's per-claim pricing.

**[00:20:56] Harold Brandt:** What's their per-claim?

**[00:20:58] Sandra Whitlock:** Around nine dollars a claim, with a minimum annual.

**[00:21:03] Harold Brandt:** That's cheaper.

**[00:21:05] Dev Patel:** Can I add some context? Per-claim services usually route the data through their platform. So you'd want to understand where the photos and PII go. And you don't own anything at the end, if you want to switch, you start over. With us, it's your system, in your environment.

**[00:21:33] Harold Brandt:** Owning software isn't always a benefit. Software needs maintenance.

**[00:21:38] Dev Patel:** That's true. It's a fair trade-off. I'd say it depends on whether you see intake as a commodity or a capability.

**[00:21:49] Sandra Whitlock:** It's a capability. It's our agent experience.

**[00:21:55] Harold Brandt:** That's your view.

**[00:21:57] Sandra Whitlock:** It's my view, yes.

**[00:22:02] Maya Okafor:** I think it's a reasonable thing to compare. If it helps, we can put the two options side by side in the proposal, three-year total cost, including maintenance. You might decide the per-claim service is right, and that's okay.

**[00:22:23] Harold Brandt:** I'd appreciate that. Honestly.

**[00:22:26] Maya Okafor:** Can I ask about the budget cycle?

**[00:22:30] Harold Brandt:** Our fiscal year is calendar. 2027 budgets get finalized at the December board meeting. December ninth.

**[00:22:41] Sandra Whitlock:** I have a placeholder in my 2027 operations budget for intake automation. Harold knows about it.

**[00:22:50] Harold Brandt:** I do. It's a placeholder.

**[00:22:54] Sandra Whitlock:** It's four hundred.

**[00:22:56] Harold Brandt:** It's a placeholder for four hundred.

**[00:23:00] Maya Okafor:** Okay. So realistically, the proof would need to happen before December ninth to inform that.

**[00:23:09] Sandra Whitlock:** Ideally, yes.

**[00:23:11] Harold Brandt:** The proof could come out of this year's operations budget. Sandra has room.

**[00:23:18] Sandra Whitlock:** I have room.

**[00:23:20] Maya Okafor:** That's doable. If we got the data by end of October, we could have results by the first week of December.

**[00:23:31] Dev Patel:** Tight but doable. The data access will be the long pole, not the analysis.

**[00:23:38] Luis Ferreira:** Getting two thousand emails with attachments out of our system, uh. Kevin's team will need to do that. And legal will need to sign off on sending PII outside.

**[00:23:55] Maya Okafor:** We can run the proof inside your cloud environment if that's simpler for legal. Are you on Azure, AWS?

**[00:24:04] Luis Ferreira:** Kevin would know. I think Azure.

**[00:24:08] Sandra Whitlock:** Azure.

**[00:24:12] Harold Brandt:** I have a question for Luis, actually, not you. Luis, if this worked, what happens to your fourteen people?

**[00:24:23] Luis Ferreira:** I'd stop backfilling. And, I mean honestly I'd move a few of them to subrogation. Subro is buried. We're leaving money on the table there. We've got a backlog of something like nineteen hundred files that nobody's looked at for recovery potential.

**[00:24:49] Harold Brandt:** Nineteen hundred?

**[00:24:51] Luis Ferreira:** Give or take.

**[00:24:52] Harold Brandt:** Why am I hearing about this now?

**[00:24:56] Luis Ferreira:** It's, it's in the monthly ops report. Page eleven.

**[00:25:02] Sandra Whitlock:** It's on page eleven, Harold.

**[00:25:05] Harold Brandt:** Hm. Okay. Well. That's a number I care about. What's the average recovery on a subro file?

**[00:25:15] Luis Ferreira:** On auto, the ones that go anywhere? A few thousand. Probably a third of those are worth pursuing.

**[00:25:24] Maya Okafor:** Interesting. Honestly, reviewing a file to identify subrogation potential is a very similar task to intake. Reading the documents, the police report, determining liability. It's not today's scope, but it might be the hard-savings story Harold's looking for.

**[00:25:50] Harold Brandt:** Don't sell me two things before you've proven one.

**[00:25:55] Maya Okafor:** Ha. Fair. Noted and parked.

**[00:25:59] Sandra Whitlock:** Harold, I'm actually going to hold you to that "number you care about."

**[00:26:05] Harold Brandt:** I'm sure you will.

**[00:26:08] Dev Patel:** Luis, a few technical questions quickly. How are emails received today? A shared mailbox?

**[00:26:18] Luis Ferreira:** Shared mailbox in Outlook. Exchange Online. claims@. And then agents also email adjusters directly, which, that's another problem. Those never get logged properly.

**[00:26:34] Dev Patel:** Okay. And do you have historical keyed data we could compare against? What your team entered for each email?

**[00:26:43] Luis Ferreira:** It's in the claims system. Linking it back to the original email is, hm. Sometimes there's a reference. Not always.

**[00:26:56] Dev Patel:** That's the data prep risk. We'd want a sample where the link is solid. Even if it's smaller.

**[00:27:06] Harold Brandt:** I want two thousand.

**[00:27:08] Dev Patel:** Okay. We'll figure out how to get to two thousand. Might take some manual matching.

**[00:27:15] Luis Ferreira:** Ugh. Okay.

**[00:27:19] Sandra Whitlock:** Underwriting has the same problem, by the way. Agents email submissions for small commercial, and our underwriting assistants key them in. Same kind of mess. Different forms.

**[00:27:35] Harold Brandt:** Sandra.

**[00:27:37] Sandra Whitlock:** I'm just noting it.

**[00:27:39] Maya Okafor:** Ha. I'm writing everything down, I promise we won't pitch it today.

**[00:27:46] Harold Brandt:** I have to drop at the half hour. What are next steps?

**[00:27:52] Maya Okafor:** Here's what I'd propose. One, we send a short proposal for the proof of value: two thousand historical FNOL emails, chosen by internal audit, run inside your Azure tenant, measured against what your team keyed. Fixed fee, results before December ninth. Two, alongside that, we put together a three-year cost comparison: build with us, versus the per-claim service, versus waiting for your claims vendor's module in 2028. Three, we need a technical session with Kevin's team on data access.

**[00:28:46] Harold Brandt:** And the payback model. Eighteen months, hard savings.

**[00:28:51] Maya Okafor:** And a payback model with only hard savings: overflow, avoided backfills, and we'll show severity separately as upside so it doesn't muddy the core number.

**[00:29:06] Harold Brandt:** Good. That's how I want it.

**[00:29:10] Sandra Whitlock:** I'll set up Kevin.

**[00:29:11] Harold Brandt:** And I'll talk to internal audit about pulling the sample. Sandra, let's talk offline.

**[00:29:19] Sandra Whitlock:** Yep.

*[00:29:23 – Harold Brandt left the meeting]*

**[00:29:28] Sandra Whitlock:** So. That was Harold.

**[00:29:32] Maya Okafor:** Honestly, that went well. He's asking the right questions.

**[00:29:37] Sandra Whitlock:** He is. He's not wrong about the RPA thing. He took the heat for it at the board. I think the subro thing actually got him, which is funny, because that wasn't even on the agenda.

**[00:29:54] Luis Ferreira:** I've been telling people about the subro backlog for a year.

**[00:30:00] Sandra Whitlock:** I know, Luis.

**[00:30:03] Maya Okafor:** Sandra, one question while we've got you. Is there anything about Harold's approval, beyond the numbers, that we should know?

**[00:30:14] Sandra Whitlock:** He'll want our CEO, Paul Ingram, in the loop before anything over two-fifty. Paul's more like me, he's pro. But Paul won't override Harold. So Harold has to get there on his own.

**[00:30:35] Maya Okafor:** Understood.

**[00:30:37] Sandra Whitlock:** And, um. One thing I didn't want to say in front of him. We're probably going to be in a merger conversation next year. Another mutual, similar size. Nothing's signed. But if it happens, claims operations get combined, and whatever intake looks like then, that's what scales. So I'd like to be the one with the working system.

**[00:31:10] Maya Okafor:** That's important. Thank you for trusting us with that.

**[00:31:15] Dev Patel:** That also argues for the thin integration layer. If the other carrier's on a different claims system, you'd want the intake piece portable.

**[00:31:28] Sandra Whitlock:** Exactly.

**[00:31:30] Luis Ferreira:** Dev, one practical thing. When you write up the proof, can you include how my team would review exceptions? Like, what the screen looks like? My people are going to be nervous.

**[00:31:47] Dev Patel:** Yes. I'll include a rough mockup of the review queue.

**[00:31:52] Maya Okafor:** And we'll want to talk to a couple of your intake specialists at some point. Not now, but before we design anything.

**[00:32:02] Luis Ferreira:** They'd like that. Nobody ever asks them.

**[00:32:05] Maya Okafor:** One open item from my side. Sandra, you mentioned agents emailing adjusters directly, which never gets logged. I don't know yet whether we'd pull adjuster mailboxes into scope for the proof or not, it complicates the data access. Let me think about it with Dev and come back to you.

**[00:32:33] Sandra Whitlock:** That's fine. My instinct is leave it out for now.

**[00:32:39] Maya Okafor:** Probably right. We'll confirm in the proposal. We'll get it over by Monday.

**[00:32:46] Sandra Whitlock:** Thank you both. Really.

**[00:32:50] Luis Ferreira:** Thanks, guys.

*[Meeting ended at 00:32:53]*
