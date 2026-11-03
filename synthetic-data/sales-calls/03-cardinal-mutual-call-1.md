# Discovery Call: Cardinal Mutual Insurance x Scope Creepers

- **Category:** sales-discovery
- **Date:** 2026-09-09
- **Duration:** 25 min
- **Platform:** Google Meet
- **Call type:** Discovery call 1 of 3 (prospect)

## Attendees

| Name | Company | Role |
|---|---|---|
| Maya Okafor | Scope Creepers | Partner / Account Executive |
| Dev Patel | Scope Creepers | Principal Solutions Engineer |
| Sandra Whitlock | Cardinal Mutual Insurance | Chief Operating Officer |
| Luis Ferreira | Cardinal Mutual Insurance | Claims Operations Manager |

---

## Transcript

**[00:00:05] Sandra Whitlock:** Hi, hi. Sorry, I was in another Meet and it wouldn't let me leave.

**[00:00:14] Maya Okafor:** No worries at all. Hi Sandra. Hi Luis.

**[00:00:20] Luis Ferreira:** Hey, good afternoon.

**[00:00:22] Dev Patel:** Afternoon.

**[00:00:28] Maya Okafor:** Thanks for making time. How's the week going?

**[00:00:34] Luis Ferreira:** Busy. We had a wind event down south over Labor Day weekend, so we're still working through about seven hundred claims from that.

**[00:00:49] Maya Okafor:** Oh wow. That's actually a good place to start. Sandra, can you give us the context for why we're talking?

**[00:01:01] Sandra Whitlock:** Sure. So Cardinal writes personal and commercial lines, mostly auto and homeowners, some small commercial. We're in seven states. About two hundred and eighty thousand policies in force. Claims volume in a normal year is around forty-two thousand claims. In a cat year it's much more.

**[00:01:38] Maya Okafor:** And the focus is first notice of loss.

**[00:01:42] Sandra Whitlock:** Right. Intake. FNOL. Luis, you want to describe the fun?

**[00:01:51] Luis Ferreira:** Yeah. So we get claims in, uh, five ways. Phone, the web portal, the mobile app, agents emailing us, and then direct email from policyholders. Phone's about thirty-five percent. Portal and app maybe thirty. And then email, between agents and policyholders, is about thirty-five, and that's the problem child.

**[00:02:32] Dev Patel:** What makes email the problem?

**[00:02:36] Luis Ferreira:** It's unstructured. An agent sends us an email that says "see attached," and the attachment is a scanned ACORD form, or a photo of a handwritten note, or a police report PDF, plus twelve phone photos of a bumper. Somebody on my team has to open everything, figure out the policy number, who's involved, what happened, the date of loss, the location, and key it all into the claims system. It's an older version.

**[00:03:30] Maya Okafor:** How many people do that?

**[00:03:34] Luis Ferreira:** Fourteen intake specialists. On a normal day they're handling around six hundred emails, but a lot of those are follow-ups on existing claims, which is a different flow. New FNOL by email is maybe one-forty a day. Average handling time is eighteen minutes per new claim. Longer if it's a multi-vehicle.

**[00:04:12] Dev Patel:** And the follow-ups? What happens with those?

**[00:04:19] Luis Ferreira:** They have to be matched to the claim and routed to the adjuster. That's like, three minutes each, but there's four hundred-something a day. And they get mis-routed a lot. I'd say five to eight percent end up with the wrong adjuster.

**[00:04:45] Maya Okafor:** What's the downstream cost of the delays?

**[00:04:51] Sandra Whitlock:** So this is, for me, this is the real issue. Our cycle time from FNOL to first contact by an adjuster is averaging four point one days on email claims. On phone claims it's under one. And first contact time is directly correlated with severity. The longer a claim sits, the more expensive it gets. Rental days pile up, attorneys get involved.

**[00:05:36] Luis Ferreira:** Attorney rep rate is the big one.

**[00:05:41] Sandra Whitlock:** Right. Our actuaries estimate, on the bodily injury side, every day of delay to first contact adds about two percent to average severity. I'm not going to pretend that's precise. But it's directionally the number.

**[00:06:05] Maya Okafor:** And customer satisfaction, I'm assuming?

**[00:06:10] Sandra Whitlock:** J.D. Power score dropped last year. Claims satisfaction is our weakest category. And our independent agents complain about it constantly. Agents are our distribution. If agents are annoyed, they place business elsewhere.

**[00:06:35] Maya Okafor:** So that's a growth problem, not just an ops problem.

**[00:06:40] Sandra Whitlock:** Exactly. That's how I've been framing it to the board.

**[00:06:46] Dev Patel:** Luis, during cat events, like the one you're in now, what happens?

**[00:06:54] Luis Ferreira:** We pull people from other departments. Underwriting assistants, customer service. Everybody gets a crash course on intake, and the quality goes way down. We had one person last spring key in a hundred and some claims with the wrong loss date because they misread the format.

**[00:07:25] Sandra Whitlock:** And we pay a TPA for overflow. That's not cheap either. Last year overflow was, I want to say a little over four hundred thousand. Something like that.

**[00:07:42] Luis Ferreira:** Somewhere around there. Finance has the exact number.

**[00:07:48] Maya Okafor:** Okay. Even roughly, that's helpful. Thanks.

**[00:07:52] Dev Patel:** What does the policyholder see on the email side? Do they get an acknowledgment?

**[00:08:00] Luis Ferreira:** Auto-reply. "We got your email." That's it. No claim number until someone keys it in. So they call. Which adds to phone volume.

**[00:08:16] Dev Patel:** Ah, so it's a loop.

**[00:08:19] Luis Ferreira:** It's a loop.

**[00:08:24] Maya Okafor:** Sandra, I should ask. Has Cardinal tried to solve this before?

**[00:08:31] Sandra Whitlock:** Um. Yes. A few years back we did an RPA project. Bots for intake. Template-based extraction from ACORD forms and auto-routing. It was, let's say, a meaningful investment. And it didn't go well.

**[00:08:58] Luis Ferreira:** It worked on about twenty percent of emails.

**[00:09:04] Sandra Whitlock:** It worked on the clean ones. The problem was nothing is clean. Agents use different ACORD versions, they scan them crooked, they handwrite. And every time the bots broke, somebody on Luis's team had to fix them, and eventually it was more work than it saved.

**[00:09:34] Luis Ferreira:** We turned the last bot off in February.

**[00:09:39] Maya Okafor:** Is there scar tissue from that internally?

**[00:09:44] Sandra Whitlock:** Some. People remember it. I'd rather not talk about it more than we have to, but you should know it happened, because it'll come up.

**[00:09:58] Dev Patel:** That's a really common story with template-based extraction. The difference with a language model is it's not matching a template. It reads the document the way a person would. So a crooked scan of an older ACORD version, or a handwritten note, or an email that just says "my wife backed into a pole in the Kroger lot on Tuesday," it can pull the structure from any of those.

**[00:10:38] Luis Ferreira:** Including photos?

**[00:10:41] Dev Patel:** Including photos. It can describe the damage, identify the vehicle, read a license plate, flag if a photo looks like it's from a different vehicle than the one on the policy. That last one's interesting for fraud.

**[00:11:04] Luis Ferreira:** Oh, SIU would love that. They've been asking for photo screening forever.

**[00:11:12] Maya Okafor:** SIU is your special investigations unit?

**[00:11:16] Luis Ferreira:** Yeah. Fraud. They're a team of six and they basically only see what adjusters flag to them. They'd love something upstream.

**[00:11:30] Maya Okafor:** I'll note that.

**[00:11:34] Sandra Whitlock:** Let's not boil the ocean. Intake first.

**[00:11:39] Maya Okafor:** Agreed. So, if intake worked the way you wanted, what does that look like?

**[00:11:48] Sandra Whitlock:** An email comes in, within minutes the claim is created in the system with all the fields filled out, the photos are attached and tagged, the policyholder gets a real claim number back, and it's routed to the right adjuster based on line, severity, and geography. And a human only touches it if something's uncertain.

**[00:12:24] Luis Ferreira:** And my team becomes, like, the exception handlers. Not keyers.

**[00:12:31] Dev Patel:** What fraction would you be happy with going straight through?

**[00:12:36] Luis Ferreira:** Honestly? If sixty percent goes straight through with good accuracy, I'd throw a party.

**[00:12:45] Sandra Whitlock:** I'd want seventy.

**[00:12:49] Luis Ferreira:** Sandra wants seventy.

**[00:12:51] Sandra Whitlock:** I want seventy.

**[00:12:55] Dev Patel:** Ha. Both reasonable. The thing I'd add is that the accuracy bar matters more than the percent. You want the model to know when it's not sure. A confident wrong answer on a date of loss is worse than kicking it to a human.

**[00:13:19] Luis Ferreira:** Yes. That was the RPA problem. The bots didn't know they were wrong.

**[00:13:28] Maya Okafor:** Luis, can I ask about your team? Beyond the volumes. How are they holding up?

**[00:13:35] Luis Ferreira:** Honestly? Not great. I've lost four of the fourteen this year. Two went to a competitor's claims department, one to a bank. I've been backfilling with temps. Temps make more mistakes. Every new hire takes three months to train on intake. That's not on any spreadsheet but it's real.

**[00:14:08] Sandra Whitlock:** It's a miserable job, keying. I'd leave too.

**[00:14:12] Luis Ferreira:** Thanks, Sandra.

**[00:14:15] Sandra Whitlock:** You know what I mean.

**[00:14:19] Maya Okafor:** Can I ask about the claims system? You mentioned it's an older version.

**[00:14:26] Luis Ferreira:** It's a few major versions behind. We're supposed to upgrade.

**[00:14:32] Sandra Whitlock:** The upgrade is scheduled for 2028. It's a big project. IT has told me not to build anything that depends on the current version's APIs too heavily.

**[00:14:48] Dev Patel:** That's good to know. We'd want a thin integration layer, so the extraction and routing logic doesn't care which version it's writing to. Then when you upgrade, you swap the connector.

**[00:15:06] Sandra Whitlock:** That'd keep IT happy.

**[00:15:10] Maya Okafor:** Who in IT should we be talking to?

**[00:15:14] Sandra Whitlock:** Kevin Marsh, he's our VP of IT. He's supportive but stretched. The upgrade is eating his team.

**[00:15:25] Dev Patel:** Luis, a few technical questions quickly. How are emails received today? A shared mailbox?

**[00:15:34] Luis Ferreira:** Shared mailbox in Outlook. Exchange Online. claims@. And then agents also email adjusters directly, which, that's another problem. Those never get logged properly.

**[00:15:51] Dev Patel:** Okay. And do you have historical keyed data? What your team entered for each email?

**[00:16:00] Luis Ferreira:** It's in the claims system. Linking it back to the original email is, hm. Sometimes there's a reference. Not always.

**[00:16:14] Dev Patel:** That's useful to know early. If we ever measured accuracy, we'd want a set where the link between email and keyed claim is solid.

**[00:16:26] Luis Ferreira:** We could probably find some. It'd be manual.

**[00:16:32] Maya Okafor:** Let me zoom back out for a second. Sandra, if nothing changes, what does the next couple of years look like?

**[00:16:42] Sandra Whitlock:** Honestly? Email share keeps growing. Agents prefer it. Younger policyholders prefer it. So the problem gets bigger every year whether we do anything or not. And I keep hiring keyers who leave.

**[00:17:05] Luis Ferreira:** And the four-point-one goes up.

**[00:17:09] Sandra Whitlock:** And the four-point-one goes up.

**[00:17:12] Maya Okafor:** Is anything else in the business competing for attention right now? I want to understand where this sits.

**[00:17:21] Sandra Whitlock:** The upgrade, obviously. And, um. Underwriting has a version of the same problem, by the way. Agents email submissions for small commercial, and our underwriting assistants key them in. Same kind of mess. Different forms.

**[00:17:45] Maya Okafor:** Interesting.

**[00:17:48] Sandra Whitlock:** I'm just noting it. Not today.

**[00:17:51] Maya Okafor:** Ha. Noted and parked. I promise we won't pitch it.

**[00:17:58] Dev Patel:** What happens to the photos today, once they're in? Are they tagged at all?

**[00:18:05] Luis Ferreira:** They get dumped into the claim file as attachments. Named whatever the phone named them. IMG underscore four thousand and something. The adjuster opens them one by one.

**[00:18:22] Dev Patel:** So even a basic "front bumper, driver side, moderate damage" tag would save the adjuster time.

**[00:18:31] Luis Ferreira:** Oh, they'd love that. They complain about the photos all the time.

**[00:18:38] Maya Okafor:** Okay. Sandra, I want to ask a couple of process questions, if that's alright. When it comes to a project like this, who else needs to be involved on your side? Who weighs in?

**[00:18:52] Sandra Whitlock:** Kevin, for the technical side. Legal, if data leaves the building. Luis, obviously, because it's his team.

**[00:19:04] Maya Okafor:** And in terms of the decision itself?

**[00:19:08] Sandra Whitlock:** That's me. Claims operations reports to me. Intake is my house. This is my call.

**[00:19:18] Maya Okafor:** Okay. Good to know.

**[00:19:21] Luis Ferreira:** She's not wrong. It's her house.

**[00:19:25] Maya Okafor:** And have you thought at all about what an investment like this would look like? Or is it too early?

**[00:19:32] Sandra Whitlock:** Too early. Honestly. I want to understand whether this is real before I start talking about money. I've been burned once. If the case is there, I'll find a way.

**[00:19:49] Maya Okafor:** That's fair. And timing? Is there a date driving this?

**[00:19:55] Sandra Whitlock:** Not a hard one. I'd like it yesterday, but I'm not going to pretend there's a deadline. I'd rather get it right.

**[00:20:06] Maya Okafor:** Understood. Then let's focus on getting you something concrete enough to evaluate.

**[00:20:14] Dev Patel:** Can I ask one more thing about the RPA project? Not the money, the mechanics. What made the bots break? Was it the input, or the downstream system?

**[00:20:26] Luis Ferreira:** Both. Mostly input. But also, every time the claims system had a patch, a screen moved and the bot clicked in the wrong place.

**[00:20:39] Dev Patel:** Right, screen-scraping. We wouldn't do that. We'd write through an API or a supported import, never through the UI.

**[00:20:49] Luis Ferreira:** Thank God.

**[00:20:52] Sandra Whitlock:** That alone would make Kevin happy.

**[00:20:56] Dev Patel:** And on the input side, the way we'd approach it is to measure before anything goes live. Take a batch of real historical emails, run them through, compare against what your team actually keyed, and see the accuracy number per field. So nobody has to take our word for it.

**[00:21:21] Sandra Whitlock:** I like that. That's what we should have done last time.

**[00:21:28] Luis Ferreira:** When you write that up, can you include how my team would review exceptions? Like, what the screen looks like? My people are going to be nervous.

**[00:21:40] Dev Patel:** Yes. I'll include a rough mockup of a review queue.

**[00:21:45] Maya Okafor:** And we'll want to talk to a couple of your intake specialists at some point. Not now, but before we design anything.

**[00:21:54] Luis Ferreira:** They'd like that. Nobody ever asks them.

**[00:21:59] Maya Okafor:** Sandra, the follow-up emails. Four hundred a day, five to eight percent misrouted. Is that in scope in your head, or is it just new claims?

**[00:22:10] Sandra Whitlock:** My head says new claims first. But if the same thing can read a follow-up and attach it to the right claim, I'm not going to say no.

**[00:22:21] Dev Patel:** It's the same capability. Read it, figure out which claim it belongs to, route it. Honestly the follow-ups might be the easier win.

**[00:22:42] Maya Okafor:** One open item from my side. You mentioned agents emailing adjusters directly, which never gets logged. I don't know yet whether that belongs in scope. It complicates data access. Let me think about it with Dev and come back to you.

**[00:23:04] Sandra Whitlock:** That's fine. My instinct is leave it out for now.

**[00:23:09] Maya Okafor:** Probably right. Okay, here's what I'd propose for next steps. One, we write up a short summary of what we heard today, the problem in your numbers, so you can tell us where we got it wrong. Two, Dev puts together a rough outline of how we'd measure accuracy on your historical emails, plus the review queue mockup for Luis. Three, we'd like a technical conversation with Kevin about how the mailbox and the claims system are set up.

**[00:23:51] Sandra Whitlock:** I can set up Kevin.

**[00:23:55] Maya Okafor:** And then a second conversation in a few weeks to walk through all of it.

**[00:24:01] Sandra Whitlock:** Works for me. Luis?

**[00:24:04] Luis Ferreira:** Yeah. I'll pull together a few examples of ugly emails so you can see what we're dealing with. Redacted.

**[00:24:12] Dev Patel:** That'd be great. The uglier the better.

**[00:24:18] Luis Ferreira:** Oh, I have ugly. Trust me.

**[00:24:22] Maya Okafor:** We'll get the summary over by early next week.

**[00:24:28] Sandra Whitlock:** Thank you both. Really. This is the first conversation about this in a while that didn't make me tired.

**[00:24:36] Luis Ferreira:** Thanks, guys.

*[Meeting ended at 00:24:40]*
