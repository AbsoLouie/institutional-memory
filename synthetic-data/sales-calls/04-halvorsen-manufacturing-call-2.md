# Discovery Call: Halvorsen Manufacturing x Scope Creepers

- **Category:** sales-discovery
- **Date:** 2026-10-07
- **Duration:** 23 min
- **Platform:** Microsoft Teams
- **Call type:** Discovery call 2 of 3 (prospect)

## Attendees

| Name | Company | Role |
|---|---|---|
| Maya Okafor | Scope Creepers | Partner / Account Executive |
| Dev Patel | Scope Creepers | Principal Solutions Engineer |
| Brian Halvorsen-Tate | Halvorsen Manufacturing | Chief Information Officer |
| Monique Archambault | Halvorsen Manufacturing | Director, HR and Learning & Development |

---

## Transcript

**[00:00:09] Maya Okafor:** Morning, Brian. Monique, are you in your car again?

**[00:00:16] Monique Archambault:** Ha. No, I'm at an actual desk today. Wausau. Very exciting.

**[00:00:26] Brian Halvorsen-Tate:** She has a window and everything.

**[00:00:30] Maya Okafor:** Ha. Okay, I want to introduce Dev Patel. Dev's our principal solutions engineer. He's set up Enterprise for a bunch of clients, SSO, SCIM, the admin side. I've filled him in on our call from mid-September.

**[00:00:54] Dev Patel:** Hi both. Thanks for having me. I read Maya's notes, so I know about the network scan, the NDA quote incident, and Todd.

**[00:01:08] Monique Archambault:** Everyone knows about Todd.

**[00:01:12] Brian Halvorsen-Tate:** Todd is becoming a brand.

**[00:01:16] Maya Okafor:** Ha. So quick recap of where we left it. Roughly two thousand people, claude.ai Enterprise, governance and training first, office before the floor, launch at the late-January all-hands. And Brian, you said you'd have a better answer on the money.

**[00:01:44] Brian Halvorsen-Tate:** I do. And I need to correct something from last time.

**[00:01:50] Maya Okafor:** Okay.

**[00:01:51] Brian Halvorsen-Tate:** Monique mentioned two-fifty. That was the number we'd floated internally, and I didn't shoot it down, which I should have. Finance went through the plan last week and cut it. For services, I have a hundred and fifty thousand this fiscal year. That's the real number.

**[00:02:21] Maya Okafor:** A hundred fifty. Got it. Thank you for telling me straight.

**[00:02:27] Monique Archambault:** Sorry, that was my fault. I repeated the whiteboard number.

**[00:02:33] Brian Halvorsen-Tate:** Not your fault. It was everybody's number until it wasn't.

**[00:02:39] Maya Okafor:** And the fiscal year ends when?

**[00:02:42] Brian Halvorsen-Tate:** March thirty-first. So it's a hundred fifty to spend between now and end of March. Licenses are separate, those come out of the IT budget. This is just services.

**[00:03:00] Maya Okafor:** Is there any chance of more next fiscal year?

**[00:03:04] Brian Halvorsen-Tate:** If this goes well, probably. Our CFO was pretty clear, though. Show results on the first chunk, then ask for more. No promises for next year.

**[00:03:21] Maya Okafor:** That's a completely reasonable stance. And honestly, it changes the shape of what I'd propose more than the size.

**[00:03:32] Brian Halvorsen-Tate:** How so?

**[00:03:34] Maya Okafor:** At two-fifty, I was picturing all three plants trained before the all-hands. At a hundred fifty, I'd rather do it really well in one place first than thinly everywhere. Phase it plant by plant.

**[00:03:56] Brian Halvorsen-Tate:** I had the same thought, actually. I just didn't want to be the one to say it.

**[00:04:03] Monique Archambault:** I'm fine with that. As long as Wausau and Dubuque don't feel like the stepchildren.

**[00:04:12] Maya Okafor:** That's the risk, right. So let's talk about which plant goes first. Where are the salaried people concentrated?

**[00:04:22] Brian Halvorsen-Tate:** Eau Claire, by a lot. It's headquarters. Engineering, sales, finance, most of customer service. Probably five hundred of the eight hundred salaried are there.

**[00:04:40] Dev Patel:** And the network scan, the three hundred forty, how does that break down by site?

**[00:04:48] Brian Halvorsen-Tate:** Mostly Eau Claire. I'd guess two-thirds. Wausau is maybe sixty or seventy, Dubuque is small.

**[00:05:02] Dev Patel:** Then Eau Claire first is almost obvious. That's where the risk is, and that's where the pilot people are.

**[00:05:10] Monique Archambault:** All twenty-five pilot people are Eau Claire, except two.

**[00:05:16] Maya Okafor:** So here's a sketch. Phase one, Eau Claire salaried, plus a small seed group of champions at Wausau and Dubuque, so those plants have someone local who's already trained. That's what goes live for the all-hands. Phase two, Wausau, spring. Phase three, Dubuque, after that. The later phases would probably land in next fiscal year.

**[00:05:54] Brian Halvorsen-Tate:** So at the all-hands, I'd announce, what, "it's live at Eau Claire, and it's coming to you"?

**[00:06:04] Maya Okafor:** "It's live for these groups, here's the schedule for everyone else, and here's your local champion." That's actually a stronger message than "everyone gets it Monday," because people know who to go to.

**[00:06:22] Monique Archambault:** I like that a lot. The local champion part especially.

**[00:06:28] Brian Halvorsen-Tate:** How many seats does that make for phase one?

**[00:06:34] Dev Patel:** If it's Eau Claire salaried plus, say, ten champions at each of the other plants, you're around five hundred twenty seats. I'd want to check that against the scan data, but that's the ballpark.

**[00:06:54] Brian Halvorsen-Tate:** Okay. That's good for my license budget too, honestly. I was nervous about licensing eight hundred up front.

**[00:07:04] Dev Patel:** Can I ask about identity? What are you on?

**[00:07:10] Brian Halvorsen-Tate:** Entra ID. Microsoft shop, all the way down.

**[00:07:16] Dev Patel:** Good. SSO and SCIM provisioning with Entra are straightforward. The question is group structure. Do you have clean groups by site and department, or is it more of a, uh, a historical situation?

**[00:07:36] Brian Halvorsen-Tate:** It's a historical situation.

**[00:07:40] Dev Patel:** Ha. Most are. The good news is the phased rollout helps. You only need clean groups for Eau Claire salaried to start, and we can provision from one group and grow it.

**[00:07:58] Brian Halvorsen-Tate:** That I can do. Department attributes are mostly right because they come from the HR system.

**[00:08:08] Monique Archambault:** Mostly.

**[00:08:10] Brian Halvorsen-Tate:** Mostly.

**[00:08:14] Monique Archambault:** I say that because the HR system data is only as good as what we put in it, and since we lost our HRIS analyst in the summer, I've been doing a lot of it by hand. In Excel. Don't tell anyone.

**[00:08:33] Maya Okafor:** Your secret's safe. Mostly.

**[00:08:38] Monique Archambault:** Ha.

**[00:08:40] Dev Patel:** Is the Excel reporting something people pull from regularly? Headcount, turnover, that kind of thing?

**[00:08:50] Monique Archambault:** Every month. Headcount by plant, turnover, overtime, open requisitions. It takes me about two days every month to build. I hate it.

**[00:09:06] Dev Patel:** Noted. That's, uh, that's a very fixable thing. Not today's problem, though.

**[00:09:14] Monique Archambault:** Not today's problem.

**[00:09:18] Maya Okafor:** Let's talk about what fits in a hundred fifty. Here's how I'd think about the buckets. Governance and policy. Enterprise admin setup and SSO. Champions program. In-person training at Eau Claire, plus champion training for the other two plants. And some support around communications for the launch.

**[00:09:50] Brian Halvorsen-Tate:** What gets cut, compared to the two-fifty version?

**[00:09:56] Maya Okafor:** Mostly two things. Full in-person training at Wausau and Dubuque before January, and the structured use-case discovery. I'd originally pictured kicking off discovery in parallel. At this budget I'd push it to after launch, maybe next fiscal year.

**[00:10:21] Brian Halvorsen-Tate:** The use-case piece is what I care about most long term.

**[00:10:27] Maya Okafor:** I know. Which is why I don't want to do it half-funded. I'd rather run one focused use case inside phase one as a proof point, and save the broader discovery.

**[00:10:44] Brian Halvorsen-Tate:** Which use case?

**[00:10:46] Maya Okafor:** You tell me. Last time you said quoting.

**[00:10:51] Brian Halvorsen-Tate:** Quoting. Nine days to three days. Rich would throw a parade.

**[00:10:58] Dev Patel:** Can I push on that a bit? A real quoting assistant, tied to past quotes and pricing, is bigger than a phase-one proof point. It touches the ERP, pricing data, customer data. That's the stuff you said you didn't want connected on day one.

**[00:11:21] Brian Halvorsen-Tate:** Fair. Yeah.

**[00:11:24] Dev Patel:** What I'd suggest instead is something narrower. Like, a set of tested prompts and a Claude project for the applications engineers, with sanitized reference material. Teaches them the safe way to do exactly what the NDA engineer was trying to do. It won't get you to three days, but it might shave real time off and it directly addresses the incident.

**[00:11:57] Brian Halvorsen-Tate:** I actually love that. Because it's also the story for leadership. "The thing that scared us, here's how we do it safely now."

**[00:12:09] Maya Okafor:** Exactly.

**[00:12:12] Brian Halvorsen-Tate:** And the bigger quoting thing is a phase-two conversation.

**[00:12:18] Maya Okafor:** Right. And speaking of the ERP, Dev, Brian mentioned Epicor last time.

**[00:12:26] Brian Halvorsen-Tate:** Oh. Yeah, so, the Epicor upgrade. We're doing it. Not sure when. RFP goes out in Q1. Honestly, the bigger issue isn't the upgrade itself, it's the data. Our item master is a disaster. Forty thousand SKUs, tons of duplicates, descriptions written by twenty different people over thirty years.

**[00:12:58] Dev Patel:** Mm. That's very common, and honestly it's one of the places where AI does well. Matching duplicates, normalizing descriptions.

**[00:13:10] Brian Halvorsen-Tate:** Is that something you'd do?

**[00:13:14] Maya Okafor:** We're not an Epicor implementation shop, I don't want to pretend. But data cleanup ahead of a migration, yes, we've done that.

**[00:13:26] Brian Halvorsen-Tate:** Huh. Okay. Separate conversation.

**[00:13:30] Maya Okafor:** Separate conversation. Monique, I owe you an answer on Hmong.

**[00:13:38] Monique Archambault:** Yes. I was hoping you'd remember.

**[00:13:42] Maya Okafor:** I looked into it, and Dev ran some tests. Short version, Claude can work in Hmong, but the quality isn't at the level of Spanish. For anything safety-related, I would not ship a translation without a native speaker reviewing it.

**[00:14:04] Dev Patel:** We took a sample lockout tagout procedure, simplified the English first, then translated. The Spanish was clean. The Hmong was understandable but a reviewer would need to fix terminology. Which honestly is what you'd do with a human translator too.

**[00:14:28] Monique Archambault:** That's actually really helpful. We have bilingual supervisors at Wausau who could review.

**[00:14:38] Maya Okafor:** That's the pattern I'd recommend. Claude drafts, a person who knows the floor reviews.

**[00:14:45] Monique Archambault:** And for onboarding. We hire about three hundred people a year, mostly hourly, and our onboarding packet is different at every plant. Some of it's supposed to be in Spanish and isn't.

**[00:15:04] Maya Okafor:** So that's a strong future use case. I'd keep it out of phase one for budget reasons, but I'd put it on the roadmap slide for the all-hands. It's the kind of thing that tells the floor this is for them too.

**[00:15:22] Monique Archambault:** Yes. That's the story I want.

**[00:15:27] Brian Halvorsen-Tate:** Okay. Let's say phase one is Eau Claire plus champions. Can you actually hit the late-January all-hands with that?

**[00:15:39] Maya Okafor:** I checked staffing after last time. With one plant instead of three, yes, comfortably. Three plants in January would have been tight. One plant in December and January is realistic.

**[00:15:57] Brian Halvorsen-Tate:** December?

**[00:16:00] Maya Okafor:** I'd want governance and admin setup done in November and December. Champion training in early January. Broader Eau Claire training the two weeks before the all-hands. So the all-hands is the announcement, but people already have it.

**[00:16:22] Dev Patel:** And the admin setup is really two weeks of work if your groups cooperate. The policy side is usually the long pole.

**[00:16:33] Brian Halvorsen-Tate:** The policy side is definitely the long pole.

**[00:16:39] Maya Okafor:** Say more?

**[00:16:42] Brian Halvorsen-Tate:** Just, there's a review process. Legal will want to read everything.

**[00:16:51] Maya Okafor:** Which brings me to the question you parked last time. Who else is involved in getting this approved? You said it was more layered than a normal IT purchase.

**[00:17:06] Brian Halvorsen-Tate:** It is. And I'm still, honestly, I'm still working it out internally. There's me, obviously. There's our CEO. Legal. And Monique has been saying, rightly, that the labor side has to be part of it.

**[00:17:28] Monique Archambault:** I've been saying it loudly.

**[00:17:33] Brian Halvorsen-Tate:** She has. I don't want to give you a half-answer on who decides what. Can we bring the right people to the next call and lay it out properly?

**[00:17:46] Maya Okafor:** Yes, that would be ideal. Who would you bring?

**[00:17:51] Monique Archambault:** I'd like to bring Gary. Gary runs labor relations. He knows the stewards better than anyone.

**[00:18:00] Maya Okafor:** Great. We'd love to meet him.

**[00:18:04] Brian Halvorsen-Tate:** I'll see about the rest.

**[00:18:09] Dev Patel:** One technical question while we're here. The shadow AI traffic. Do you want to block the consumer tools once Enterprise is live, or just monitor?

**[00:18:22] Brian Halvorsen-Tate:** I don't know yet. What do people usually do?

**[00:18:27] Dev Patel:** Most clients monitor for the first month or two, then block the most common ones once people have a good alternative. If you block on day one, people go to their phones, like you said.

**[00:18:45] Brian Halvorsen-Tate:** Then monitor first. Okay.

**[00:18:50] Dev Patel:** And with phasing, you'd only block at a site once that site has access. Otherwise Wausau gets the stick before the carrot.

**[00:19:02] Monique Archambault:** Please don't give Wausau the stick before the carrot. They'll never let me forget it.

**[00:19:09] Maya Okafor:** Ha. Noted.

**[00:19:14] Brian Halvorsen-Tate:** Oh, one more thing that came up in the finance conversation. Our CFO wanted to know how we'd show the hundred fifty was worth it. In March. Not in a year.

**[00:19:30] Maya Okafor:** That's where the measurement framework helps. Did that land okay?

**[00:19:36] Monique Archambault:** I loved it. I already put it in a slide.

**[00:19:40] Maya Okafor:** Ha. Great. So by end of March, you'd have adoption numbers for Eau Claire, proficiency check-ins on the champions, a before-and-after on the applications engineer quoting workflow, and the shadow AI traffic trend. That's a credible story for a next-year ask.

**[00:20:08] Brian Halvorsen-Tate:** That's the story I need.

**[00:20:14] Dev Patel:** And the network scan is your baseline. Can you re-run it monthly?

**[00:20:20] Brian Halvorsen-Tate:** Our MSSP can, yeah.

**[00:20:24] Dev Patel:** Then let's make that a standing report.

**[00:20:28] Maya Okafor:** Okay. Let me play it back. Budget is a hundred fifty thousand for services this fiscal year, ending March thirty-first, not two-fifty. Licenses are separate in IT. Because of that, we phase the rollout plant by plant: Eau Claire salaried plus seed champions at Wausau and Dubuque for the all-hands, Wausau and Dubuque in later phases, likely next fiscal year. One narrow proof point with the applications engineers. Translation and onboarding go on the roadmap. Did I get it?

**[00:21:15] Brian Halvorsen-Tate:** You got it.

**[00:21:18] Monique Archambault:** Yes.

**[00:21:21] Maya Okafor:** Next steps from our side. I'll put the phased plan into a short draft scope so you can react to it, with the buckets and rough sizing against the hundred fifty. Still not a formal proposal, because I want to hear from the people on the next call first.

**[00:21:46] Brian Halvorsen-Tate:** That makes sense.

**[00:21:50] Dev Patel:** And I'll send you an Entra SSO and SCIM prep checklist, so your team can start cleaning up the Eau Claire groups. That'll save us time later no matter what.

**[00:22:04] Brian Halvorsen-Tate:** Great.

**[00:22:08] Maya Okafor:** Monique, I'll also send the Spanish and Hmong samples Dev ran, so your bilingual supervisors can tell us what they think.

**[00:22:20] Monique Archambault:** Perfect. I'll get them in front of two people at Wausau.

**[00:22:26] Maya Okafor:** And on your side, Brian, the site breakdown of the network scan would help Dev confirm the seat count.

**[00:22:36] Brian Halvorsen-Tate:** I'll send it this week.

**[00:22:40] Maya Okafor:** And for the next call, Gary, and whoever else you think needs to be in the room.

**[00:22:48] Brian Halvorsen-Tate:** I'll work on it. End of October?

**[00:22:52] Maya Okafor:** I'll send times for the week of the twenty-sixth.

**[00:22:58] Monique Archambault:** Thank you both. This was really helpful. Honestly, the plant-by-plant thing makes me less nervous, not more.

**[00:23:10] Maya Okafor:** That's what we like to hear. Thanks, everyone.

**[00:23:15] Dev Patel:** Thanks, all.

**[00:23:18] Brian Halvorsen-Tate:** Thanks.

*[Meeting ended at 00:23:22]*
