# Discovery Call: Halvorsen Manufacturing x Scope Creepers

- **Category:** sales-discovery
- **Date:** 2026-09-15
- **Duration:** 25 min
- **Platform:** Microsoft Teams
- **Call type:** Discovery call 1 of 3 (prospect)

## Attendees

| Name | Company | Role |
|---|---|---|
| Maya Okafor | Scope Creepers | Partner / Account Executive |
| Brian Halvorsen-Tate | Halvorsen Manufacturing | Chief Information Officer |
| Monique Archambault | Halvorsen Manufacturing | Director, HR and Learning & Development |

---

## Transcript

**[00:00:10] Maya Okafor:** Hi Brian, hi Monique. Can you hear me?

**[00:00:17] Brian Halvorsen-Tate:** Loud and clear. Monique, you there?

**[00:00:23] Monique Archambault:** I'm here. I'm in my car, actually, parked at the Eau Claire plant, so if it cuts out, that's why.

**[00:00:35] Maya Okafor:** No problem. Brian, I have to ask, Halvorsen-Tate, are you, uh, related to the Halvorsens?

**[00:00:48] Brian Halvorsen-Tate:** Ha. Everyone asks. Yes, my grandmother was a Halvorsen. Fourth generation family business. I promise I got the job on merit. Mostly.

**[00:01:05] Monique Archambault:** He did. Mostly.

**[00:01:08] Maya Okafor:** Ha. Okay, so I know you both reached out after the webinar on enterprise rollouts. I'd love to hear what's going on and what prompted it.

**[00:01:25] Brian Halvorsen-Tate:** Sure. So, quick context. Halvorsen makes industrial pumps and valves, mostly for water treatment and food processing. Three plants, Eau Claire, Wausau, and one in Dubuque. About two thousand employees. Roughly twelve hundred are hourly production, represented by the steelworkers. Eight hundred or so salaried: engineering, sales, finance, customer service, supply chain, the usual.

**[00:02:14] Maya Okafor:** Got it.

**[00:02:16] Brian Halvorsen-Tate:** And what prompted it, honestly, is that we did a quick network scan in August and found that about three hundred and forty people had used ChatGPT or similar tools from company devices in the past month. Some on personal accounts. We have no policy, no approved tool, nothing.

**[00:02:49] Maya Okafor:** Shadow AI.

**[00:02:52] Brian Halvorsen-Tate:** Shadow AI. And then, the thing that really got leadership's attention: one of our applications engineers pasted a customer's full pump spec and a pricing sheet into a free chatbot to help write a quote. The customer is under NDA with us. Nothing happened, as far as we know. But.

**[00:03:28] Maya Okafor:** But it could have.

**[00:03:30] Brian Halvorsen-Tate:** Exactly. So we can either block everything, which, people will just use their phones, or we give them something good and safe.

**[00:03:47] Monique Archambault:** And from my side, the people who are using it are getting real value. I talked to a few of them. Customer service is using it to draft responses. Engineers are using it for code and calculations. Somebody in finance built, apparently, a whole variance analysis workflow. So we don't want to take that away. We want to channel it.

**[00:04:26] Maya Okafor:** That's a really healthy framing. So you've landed on Claude?

**[00:04:35] Brian Halvorsen-Tate:** We're leaning toward claude.ai Enterprise, for everybody, eventually. All two thousand. We also looked at Copilot, since we're a Microsoft shop. But the engineers and the people who did the pilot strongly preferred Claude.

**[00:04:59] Maya Okafor:** What pilot?

**[00:05:00] Brian Halvorsen-Tate:** We did an informal thing. Twenty-five people, Team plan, six weeks. Mostly engineering and some sales ops. People got mad when it ended.

**[00:05:17] Maya Okafor:** That's a great sign. Any data from it?

**[00:05:22] Brian Halvorsen-Tate:** A survey. Self-reported time savings averaged about four hours a week. Which I take with a grain of salt.

**[00:05:32] Maya Okafor:** Sure. Still, directionally strong. So where do you need help? Because Anthropic can sell you licenses directly.

**[00:05:44] Brian Halvorsen-Tate:** Right. We don't need help buying it. We need help making it work. We rolled out Teams in 2020 and two years later half the company was still emailing attachments.

**[00:06:01] Monique Archambault:** Three-quarters.

**[00:06:04] Brian Halvorsen-Tate:** Three-quarters. So it's training, it's governance, it's the people side.

**[00:06:13] Maya Okafor:** Let's take those in turn. When you say all two thousand, does that include the hourly workforce from day one?

**[00:06:23] Monique Archambault:** That's, um. That's the sensitive part.

**[00:06:29] Brian Halvorsen-Tate:** Go ahead, Monique.

**[00:06:31] Monique Archambault:** We have a really good relationship with our union locals. Took a long time to build. Contract's up in June of '27. And the moment anyone hears "AI" on the shop floor, they hear "automation" and "layoffs." Which is not what this is. But perception is everything heading into a contract year.

**[00:07:06] Maya Okafor:** That's important. Has anything reached the floor yet?

**[00:07:11] Monique Archambault:** Rumors. The pilot people talked. A steward at Wausau asked me last month, "are you bringing in robots to replace us." Which, we're not. We're bringing in a chatbot for the office.

**[00:07:32] Maya Okafor:** Right. Have you thought about what it could mean for them? Positively, I mean.

**[00:07:40] Monique Archambault:** Honestly, yes. Our maintenance techs and line leads deal with manuals, lockout tagout, SOPs, and those are a mess. Binders. SharePoint, half outdated. If a line lead could ask a question in plain English and get the right procedure, that's a safety win.

**[00:08:11] Brian Halvorsen-Tate:** That's a later thing, though. Knowledge base, probably tablets on the floor.

**[00:08:18] Monique Archambault:** I know. I'm just saying it's the story.

**[00:08:23] Maya Okafor:** It's a good story. "This helps people do their jobs, starting with the office," with a visible safety use case on the roadmap, is a pattern that's worked well. I'd be careful not to promise the floor anything we can't deliver, though.

**[00:08:44] Monique Archambault:** Agreed.

**[00:08:48] Maya Okafor:** Okay, governance. Brian, current state?

**[00:08:53] Brian Halvorsen-Tate:** Basically nothing. An acceptable use policy from 2018 that doesn't mention AI. A data classification policy, sort of. Four tiers: public, internal, confidential, restricted. Nobody follows it. Nothing is labeled.

**[00:09:17] Maya Okafor:** Security team?

**[00:09:19] Brian Halvorsen-Tate:** Me, two people, and an MSSP for monitoring. We're not big.

**[00:09:28] Maya Okafor:** Okay. So governance, practically, is: an AI acceptable use policy, a simple "what you can and can't put in" guide mapped to your classification tiers, the Enterprise admin setup, SSO, SCIM, retention, which connectors are allowed, and usage monitoring. Roughly what you're picturing?

**[00:09:58] Brian Halvorsen-Tate:** Yes. And I already know people are going to want it connected to SharePoint, email, our ERP.

**[00:10:07] Maya Okafor:** That's where I'd go slow. Start with no connectors or only low-risk ones, prove the governance works, then open up. Which ERP?

**[00:10:19] Brian Halvorsen-Tate:** Epicor. Old version.

**[00:10:23] Maya Okafor:** Definitely not day one for that.

**[00:10:26] Brian Halvorsen-Tate:** Fine by me.

**[00:10:30] Maya Okafor:** And on the NDA situation. With Enterprise, your data isn't used for training, and you get admin controls and audit logs. But honestly, the bigger risk is people continuing to use free tools on their phones. That's a training and culture problem more than a technology one.

**[00:10:55] Brian Halvorsen-Tate:** That's my whole argument. Give them something better and they'll stop using the free stuff.

**[00:11:02] Monique Archambault:** Mostly.

**[00:11:04] Brian Halvorsen-Tate:** Mostly.

**[00:11:07] Maya Okafor:** Monique, training. What does L&D look like today?

**[00:11:13] Monique Archambault:** Small. Me and three people. An LMS that's mostly compliance training. Safety, harassment. A leadership program. We don't do technical training at scale.

**[00:11:31] Maya Okafor:** What's worked for past rollouts?

**[00:11:35] Monique Archambault:** In-person. Lunch-and-learns at each plant. Video modules get, like, a twelve percent completion rate if they aren't mandatory.

**[00:11:48] Maya Okafor:** Really useful. So probably a short required basics module, but the real work happens in in-person, role-specific sessions at each plant. Plus a champions network.

**[00:12:05] Monique Archambault:** We have the pilot people. Some would be great champions. A few would be, um, too enthusiastic.

**[00:12:16] Brian Halvorsen-Tate:** There's one guy in engineering, Todd, who built like nineteen projects in six weeks. He'd train the whole company if we let him.

**[00:12:28] Maya Okafor:** Todd sounds like a champion who needs guardrails.

**[00:12:32] Monique Archambault:** Todd needs guardrails, yes.

**[00:12:37] Maya Okafor:** Ha. Okay. Brian, what's the business case look like to you? Beyond stopping the leaks.

**[00:12:46] Brian Halvorsen-Tate:** I don't want two thousand people using it to write emails. I want to find the handful of things that actually move the business. Quoting, for sure. Our applications engineers spend days on custom pump quotes. Specs, pricing, past quotes, compliance requirements. Turnaround is averaging nine business days. Customers want three.

**[00:13:17] Maya Okafor:** That's a big gap.

**[00:13:19] Brian Halvorsen-Tate:** Rich Kowalski, our VP of Sales, says faster quotes are worth more than any price cut. And that's literally where the NDA thing came from. The engineer was trying to go faster.

**[00:13:35] Maya Okafor:** Which tells you the demand is real. That might eventually be something beyond chat, a structured quoting assistant. But foundation first.

**[00:13:48] Brian Halvorsen-Tate:** Foundation first. Agreed.

**[00:13:53] Maya Okafor:** So let's talk timing. What are you working toward?

**[00:13:58] Brian Halvorsen-Tate:** We have a company all-hands in late January. The annual kickoff, all three plants dial in. That's the moment. I want to stand up there and say "here's the tool, here are the rules, here's how you get trained."

**[00:14:19] Maya Okafor:** So licenses live by then.

**[00:14:22] Brian Halvorsen-Tate:** At least for the first group, yes. Live, policy published, champions in place.

**[00:14:30] Monique Archambault:** And realistically I need the floor to hear about it from us before that. Not at the all-hands for the first time.

**[00:14:40] Maya Okafor:** Understood. Late January is tight but workable for a foundation phase. Governance, admin config, champions, training for a first wave. Deeper use-case work would come after launch.

**[00:14:58] Brian Halvorsen-Tate:** That sequence makes sense.

**[00:15:01] Maya Okafor:** Is the late-January date fixed, or is there flexibility?

**[00:15:07] Brian Halvorsen-Tate:** The all-hands date is fixed. What we announce at it is flexible, I guess. But I really don't want to announce "we're thinking about AI." We've been thinking about it for a year.

**[00:15:23] Maya Okafor:** Ha. Fair. And on the investment side, have you scoped a number for services?

**[00:15:30] Brian Halvorsen-Tate:** Not really. The licenses we'd handle out of IT. Services, I don't, uh, I don't have a firm number for you yet.

**[00:15:42] Monique Archambault:** Weren't we thinking something in the two-fifty range? That's what I heard in the planning meeting.

**[00:15:49] Brian Halvorsen-Tate:** That was, yeah, that number came up. Two-fifty-ish. But that was a whiteboard number. Don't hold me to it.

**[00:15:59] Maya Okafor:** No problem. I won't write it in stone. I'll write it in pencil.

**[00:16:04] Brian Halvorsen-Tate:** Ha. Pencil's good.

**[00:16:07] Maya Okafor:** And beyond the two of you, who else would be involved in getting this over the line?

**[00:16:14] Brian Halvorsen-Tate:** A few people. It's, uh, it's a little more layered than a normal IT purchase, given the plants. Can I come back to you on that? I want to make sure I give you the right picture, not the org chart picture.

**[00:16:31] Maya Okafor:** Totally fine. We can cover it next time.

**[00:16:35] Monique Archambault:** Oh, sorry, the shift supervisor's waving at me. Two minutes? I'm going to mute.

**[00:16:43] Maya Okafor:** Of course.

*[00:16:46 – 00:19:49, Monique Archambault muted / off camera]*

**[00:16:50] Brian Halvorsen-Tate:** While she's away. Monique's going to be your biggest ally on this. But she's carrying a lot. HR is short-staffed.

**[00:17:04] Maya Okafor:** Noted. We'll try not to add to her pile.

**[00:17:08] Brian Halvorsen-Tate:** Appreciate that. And honestly, IT has a lot on its plate in general. We've got a homegrown maintenance scheduling app at Dubuque that an intern wrote in, like, 2012, and it's on a server under someone's desk. Literally under a desk.

**[00:17:31] Maya Okafor:** The server under the desk. A classic.

**[00:17:36] Brian Halvorsen-Tate:** It's terrifying. If that box dies, Dubuque doesn't know which machines to service. Anyway. Different problem.

**[00:17:47] Maya Okafor:** Different problem. But I'm noting it.

**[00:17:50] Brian Halvorsen-Tate:** Note away.

**[00:17:54] Maya Okafor:** Who else are you talking to on the rollout?

**[00:17:59] Brian Halvorsen-Tate:** Our Microsoft partner pitched a Copilot adoption program. Cheap, because Microsoft subsidizes it. And a big consulting firm pitched an "AI transformation" program. Seven figures and a lot of slides.

**[00:18:19] Maya Okafor:** What did you think of the Copilot pitch?

**[00:18:24] Brian Halvorsen-Tate:** Generic. They didn't ask a single question about the union or the plants. Same deck they use for a bank.

**[00:18:36] Maya Okafor:** That's useful. And if you end up with both Copilot and Claude for different groups, that's fine. We're not religious about it.

**[00:18:48] Brian Halvorsen-Tate:** Good to hear.

**[00:19:52] Monique Archambault:** Sorry, I'm back. Forklift issue. Nothing serious.

**[00:19:59] Maya Okafor:** No problem. Monique, measurement. How would you know if training and adoption worked?

**[00:20:07] Monique Archambault:** Weekly active users, I guess. But that's not really enough.

**[00:20:14] Maya Okafor:** Agreed. Usage is a floor. We usually suggest three tiers: adoption, so active users and frequency; proficiency, so are people doing more than basic tasks; and impact, the business metrics on specific use cases. Like quote turnaround.

**[00:20:41] Monique Archambault:** I like that. Can you send it as a framework?

**[00:20:44] Maya Okafor:** Yes.

**[00:20:47] Brian Halvorsen-Tate:** And success for me, phase one: zero data incidents, sixty percent weekly active among licensed users by end of Q1, and shadow AI traffic on our network drops by at least half.

**[00:21:06] Maya Okafor:** Those are crisp.

**[00:21:08] Monique Archambault:** And for me: no grievances filed. And nobody on the floor hears about this from a rumor.

**[00:21:18] Maya Okafor:** That's a real success criterion. I'm writing it down.

**[00:21:23] Brian Halvorsen-Tate:** She means it.

**[00:21:25] Monique Archambault:** I mean it.

**[00:21:29] Maya Okafor:** One more on need. The two thousand. Is the goal everyone gets a seat, or everyone gets access to something?

**[00:21:38] Brian Halvorsen-Tate:** Long term, everyone has an approved tool. Whether every hourly operator needs a full seat, I don't know. Some might just need a kiosk or a shared tablet in the break room.

**[00:21:54] Monique Archambault:** And I'd want that to be a choice we make carefully, not a default.

**[00:22:00] Maya Okafor:** Makes sense. We'd want the first wave to be the people with the most shadow usage and the most to gain, which sounds like engineering, sales, customer service, and finance.

**[00:22:13] Brian Halvorsen-Tate:** That's exactly the network scan list, yeah.

**[00:22:18] Maya Okafor:** Okay. Let me play back what I've heard. You need a safe, approved AI tool for roughly two thousand people because three hundred and forty are already using unapproved ones and you had a near-miss with customer NDA data. You want claude.ai Enterprise, with governance, training, and a champions network built from the pilot group. The office goes first, the floor later and carefully, because of the contract year. And the target is a launch announcement at the late-January all-hands.

**[00:22:58] Brian Halvorsen-Tate:** That's it. That's exactly it.

**[00:23:01] Monique Archambault:** Yes.

**[00:23:04] Maya Okafor:** Great. So for next steps. I'd like to bring Dev Patel, our principal solutions engineer, to the next conversation. He's done the Enterprise admin setup and SSO side many times and he'll have sharper questions for you on the network scan and the identity setup.

**[00:23:26] Brian Halvorsen-Tate:** Good. I'd like that.

**[00:23:30] Maya Okafor:** Before then, I'll send a short recap of today, the measurement framework, and a rough outline of what a foundation phase usually includes, so you can react to it. Not a proposal yet. I want to understand the investment picture and who's involved before I put numbers on paper.

**[00:23:54] Brian Halvorsen-Tate:** That's fair. I'll have a better answer on the money by then.

**[00:24:01] Maya Okafor:** And one thing I'll check on my side. Monique mentioned in the webinar Q&A that some of your workforce speaks Spanish and Hmong. I want to look into how Claude handles Hmong before we promise anything there.

**[00:24:19] Monique Archambault:** You remembered that. Thank you.

**[00:24:23] Maya Okafor:** I'll also look at what a January training schedule across three plants would take on our side, so I'm not overpromising.

**[00:24:34] Brian Halvorsen-Tate:** Okay.

**[00:24:36] Maya Okafor:** From your side, Brian, could you share the pilot survey results and the network scan summary? Whatever you're comfortable with.

**[00:24:47] Brian Halvorsen-Tate:** I can do that.

**[00:24:49] Maya Okafor:** And Monique, a list of the pilot participants and departments helps for the champion design.

**[00:24:58] Monique Archambault:** Sure. Todd included.

**[00:25:01] Maya Okafor:** Ha. Todd especially.

**[00:25:05] Brian Halvorsen-Tate:** Let's do the follow-up in about three weeks. First week of October?

**[00:25:12] Maya Okafor:** Perfect. I'll send times for the week of October fifth.

**[00:25:18] Monique Archambault:** I've got to go, shift change. Thank you, Maya.

**[00:25:23] Maya Okafor:** Thanks Monique, thanks Brian. Talk soon.

**[00:25:26] Brian Halvorsen-Tate:** Thanks.

*[Meeting ended at 00:25:30]*
