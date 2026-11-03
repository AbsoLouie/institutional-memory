# Discovery Call: Halvorsen Manufacturing x Scope Creepers

- **Category:** sales-discovery
- **Date:** 2026-10-21
- **Duration:** 30 min
- **Platform:** Microsoft Teams
- **Call type:** First discovery call (prospect)

## Attendees

| Name | Company | Role |
|---|---|---|
| Maya Okafor | Scope Creepers | Partner / Account Executive |
| Brian Halvorsen-Tate | Halvorsen Manufacturing | Chief Information Officer |
| Monique Archambault | Halvorsen Manufacturing | Director, HR and Learning & Development |

---

## Transcript

**[00:00:08] Maya Okafor:** Hi Brian, hi Monique. Can you hear me?

**[00:00:14] Brian Halvorsen-Tate:** Loud and clear. Monique, you there?

**[00:00:19] Monique Archambault:** I'm here. I'm in my car, actually, parked at the Eau Claire plant, so if it cuts out, that's why.

**[00:00:29] Maya Okafor:** No problem. Brian, I have to ask, Halvorsen-Tate, are you, uh, related to the Halvorsens?

**[00:00:40] Brian Halvorsen-Tate:** Ha. Everyone asks. Yes, my grandmother was a Halvorsen. Fourth generation family business. I promise I got the job on merit. Mostly.

**[00:00:54] Monique Archambault:** He did. Mostly.

**[00:00:57] Maya Okafor:** Ha. Okay, so I know you both reached out after the webinar on enterprise rollouts. I'd love to hear what's going on and what prompted it.

**[00:01:11] Brian Halvorsen-Tate:** Sure. So, quick context. Halvorsen makes industrial pumps and valves, mostly for water treatment and food processing. Three plants, Eau Claire, Wausau, and one in Dubuque. About two thousand employees. Roughly twelve hundred are hourly production, represented by the steelworkers. Eight hundred or so salaried: engineering, sales, finance, customer service, supply chain, the usual.

**[00:01:52] Maya Okafor:** Got it.

**[00:01:53] Brian Halvorsen-Tate:** And what prompted it, honestly, is that we did a quick network scan in August and found that about three hundred and forty people had used ChatGPT or similar tools from company devices in the past month. Some on personal accounts. We have no policy, no approved tool, nothing.

**[00:02:21] Maya Okafor:** Shadow AI.

**[00:02:23] Brian Halvorsen-Tate:** Shadow AI. And then, the thing that really got leadership's attention: one of our applications engineers pasted a customer's full pump spec and a pricing sheet into a free chatbot to help write a quote. The customer is under NDA with us. Nothing happened, as far as we know. But.

**[00:02:53] Maya Okafor:** But it could have.

**[00:02:55] Brian Halvorsen-Tate:** Exactly. So we can either block everything, which, people will just use their phones, or we give them something good and safe.

**[00:03:09] Monique Archambault:** And from my side, the people who are using it are getting real value. I talked to a few of them. Our customer service team is using it to draft responses. Engineers are using it for code and calculations. Somebody in finance built, apparently, a whole variance analysis workflow. So, we don't want to take that away. We want to channel it.

**[00:03:42] Maya Okafor:** That's a really healthy framing. So you've landed on Claude Enterprise?

**[00:03:51] Brian Halvorsen-Tate:** We've landed on, we're leaning toward Claude. We also looked at Copilot, since we're a Microsoft shop. Honestly, we'll probably end up with Copilot for some people anyway because it's bundled in the E5 conversation. But the engineers and the people who did the pilot strongly preferred Claude.

**[00:04:19] Maya Okafor:** What pilot?

**[00:04:20] Brian Halvorsen-Tate:** We did an informal thing. Twenty-five people, Team plan, six weeks. Mostly engineering and some sales ops. The feedback was really positive. Like, people got mad when it ended.

**[00:04:40] Maya Okafor:** That's a great sign. Do you have any data from the pilot?

**[00:04:45] Brian Halvorsen-Tate:** A survey. Self-reported time savings averaged about four hours a week. Which I take with a grain of salt.

**[00:04:55] Maya Okafor:** Sure. Still, directionally strong. Okay, so where do you need help? Because Anthropic can sell you licenses directly.

**[00:05:08] Brian Halvorsen-Tate:** Right. We don't need help buying it. We need help making it work. I've seen what happens when you give everybody a tool and walk away. We rolled out Teams in 2020 and two years later half the company was still emailing attachments.

**[00:05:30] Monique Archambault:** Three-quarters.

**[00:05:32] Brian Halvorsen-Tate:** Three-quarters. So, it's training, it's governance, it's figuring out the use cases that actually matter, and it's, frankly, the people side.

**[00:05:48] Maya Okafor:** Let's dig in on each. How many seats are you thinking?

**[00:05:53] Brian Halvorsen-Tate:** Phase one, salaried staff. So up to eight hundred. Realistically maybe five or six hundred in the first wave, we'd start with the departments that are most ready.

**[00:06:09] Maya Okafor:** And the hourly workforce?

**[00:06:12] Monique Archambault:** That's, um. That's the sensitive part.

**[00:06:18] Brian Halvorsen-Tate:** Go ahead, Monique.

**[00:06:19] Monique Archambault:** So, we have a really good relationship with our union locals. Took a long time to build. Contract's up for renegotiation in, uh, June of '27. And the moment anyone hears "AI" on the shop floor, they hear "automation" and "layoffs." Which is not what this is. But perception is everything in a contract year.

**[00:06:53] Maya Okafor:** That's important. Is the union aware of any of this yet?

**[00:06:58] Monique Archambault:** Not formally. Some of the stewards have heard rumors because the pilot people talked. I had one steward at Wausau ask me directly last week, "are you bringing in robots to replace us." Which, we're not. We're bringing in a chatbot for the office.

**[00:07:24] Maya Okafor:** Right.

**[00:07:26] Monique Archambault:** But I need to get ahead of it. I'd like to brief the union leadership before we announce anything company-wide. And I'd like to have something credible to say about what it means for them.

**[00:07:42] Maya Okafor:** Have you thought about what it could mean for them? Positively, I mean.

**[00:07:49] Monique Archambault:** Actually, yes. Our maintenance techs and line leads deal with a lot of manuals, safety procedures, lockout tagout, and our SOPs are, honestly, a mess. Some are binders. Some are in SharePoint, half outdated. If a line lead could ask a question in plain English and get the right procedure, that's a safety win. That's the kind of thing the union would actually support.

**[00:08:24] Brian Halvorsen-Tate:** That's a phase two thing, though. That needs a whole knowledge base build, and probably tablets on the floor.

**[00:08:32] Monique Archambault:** I know. I'm just saying it's the story.

**[00:08:38] Maya Okafor:** It's a good story. And honestly, positioning the rollout as "this helps people do their jobs, starting with the office" with a visible safety use case on the roadmap is a pattern that's worked well. I'd want to be careful not to promise the floor anything we can't deliver, though.

**[00:09:02] Monique Archambault:** Agreed.

**[00:09:06] Maya Okafor:** Okay, governance. Brian, what's your current state there?

**[00:09:11] Brian Halvorsen-Tate:** Basically nothing. We have an acceptable use policy from 2018 that doesn't mention AI. We have a data classification policy, sort of. Four tiers: public, internal, confidential, restricted. But nobody follows it. Nothing is labeled.

**[00:09:37] Maya Okafor:** Is there a security team?

**[00:09:41] Brian Halvorsen-Tate:** It's me, and two people. And an MSSP for monitoring. We're not big.

**[00:09:49] Maya Okafor:** Okay. So the governance piece, practically, is: an AI acceptable use policy, a simple "what you can and can't put in" guide mapped to your data classification, the admin configuration of Enterprise, SSO, SCIM, retention settings, which connectors are allowed, and a way to monitor usage. Is that roughly what you're picturing?

**[00:10:21] Brian Halvorsen-Tate:** Yes. And I want to understand, the connectors piece. People are going to want it connected to SharePoint, email, our ERP. How do we think about that?

**[00:10:37] Maya Okafor:** That's where I'd go slow. Start with no connectors or only low-risk ones, prove the governance works, then open up. The ERP especially. Which ERP?

**[00:10:51] Brian Halvorsen-Tate:** Epicor. Old version. We're evaluating an upgrade.

**[00:10:58] Maya Okafor:** Okay. Definitely not day one for that.

**[00:11:01] Brian Halvorsen-Tate:** Fine by me.

**[00:11:05] Maya Okafor:** And data leakage, the customer-NDA situation. With Enterprise, data isn't used for training, and you get admin controls and audit logs. But honestly, the bigger risk is people continuing to use free tools on their phones. That's a training and culture problem more than a technology one.

**[00:11:31] Brian Halvorsen-Tate:** That's what I keep telling the CEO. If we give them something better, they'll stop using the free stuff.

**[00:11:40] Monique Archambault:** Mostly.

**[00:11:41] Brian Halvorsen-Tate:** Mostly.

**[00:11:43] Maya Okafor:** Who's the CEO? And how involved is he or she?

**[00:11:48] Brian Halvorsen-Tate:** Erik Halvorsen. My cousin. Ha. He's supportive but cautious. He's the one who saw the NDA incident. He'll sign off on the overall direction. And our general counsel, Patricia Wynn, has to approve the policy.

**[00:12:11] Maya Okafor:** Is Patricia supportive?

**[00:12:15] Brian Halvorsen-Tate:** Patricia is... thorough.

**[00:12:18] Monique Archambault:** Patricia is going to want to read every word of the Anthropic terms.

**[00:12:23] Maya Okafor:** Ha. That's fine. We can help prep that. Legal teams usually focus on data use, retention, and indemnification. We can give her a summary of what we've seen other GCs focus on.

**[00:12:41] Brian Halvorsen-Tate:** That would help. She's also going to ask about the IP stuff. Like, if an engineer uses Claude to help design something, who owns it.

**[00:12:53] Maya Okafor:** Good question. I'll be honest, I'm not a lawyer, and I'd want her to get that from her own read and from Anthropic. But I can point her to the relevant sections and what other clients have done.

**[00:13:11] Brian Halvorsen-Tate:** Fair.

**[00:13:12] Maya Okafor:** Monique, training. What does L&D look like at Halvorsen today?

**[00:13:19] Monique Archambault:** Small. It's me and three people. We have an LMS, it's mostly compliance training. Safety, harassment, that kind of thing. We do a leadership program. We don't really do technical training at scale.

**[00:13:40] Maya Okafor:** What's worked in the past for rollouts?

**[00:13:46] Monique Archambault:** In-person, honestly. Our people respond to in-person. Lunch-and-learns at each plant. Video modules get, like, a twelve percent completion rate if they aren't mandatory.

**[00:14:01] Maya Okafor:** That's really useful. So the training approach probably looks like: a short required basics module, but the real work happens in in-person, role-specific sessions at each plant. And a champions network. Do you have anything like that?

**[00:14:22] Monique Archambault:** We have the pilot people. Twenty-five of them. Some of them would be great champions. A few of them would be, um, too enthusiastic.

**[00:14:36] Maya Okafor:** Ha. We know that type.

**[00:14:40] Brian Halvorsen-Tate:** There's one guy in engineering, Todd, who built like nineteen projects in six weeks. He'd train the whole company if we let him.

**[00:14:52] Maya Okafor:** Todd sounds like a champion with good guardrails.

**[00:14:57] Monique Archambault:** Todd needs guardrails, yes.

**[00:15:01] Maya Okafor:** What about use-case discovery? How do you want to approach figuring out where the value is?

**[00:15:10] Brian Halvorsen-Tate:** That's the piece I care most about. I don't want eight hundred people using it to write emails. I want to find the five or ten things that actually move the business.

**[00:15:24] Maya Okafor:** Any guesses?

**[00:15:27] Brian Halvorsen-Tate:** Quoting, for sure. Our applications engineers spend days on custom pump quotes. Each quote is a mix of specs, pricing, past quotes, compliance requirements. We do about, uh, I think twenty-two hundred quotes a year, and our win rate is around twenty-eight percent. Turnaround is averaging nine business days. Customers want three.

**[00:16:00] Maya Okafor:** That's significant.

**[00:16:02] Brian Halvorsen-Tate:** The VP of Sales, Rich Kowalski, would kill for that. He's said that faster quotes is worth more than any price cut.

**[00:16:13] Maya Okafor:** And that might be something beyond chat. A more structured quoting assistant tied to your past quotes and pricing.

**[00:16:23] Brian Halvorsen-Tate:** Right. That's what I'm thinking. But first we need the foundation.

**[00:16:30] Monique Archambault:** And from HR, I'll tell you, onboarding. We hire about three hundred people a year, mostly hourly, and our onboarding documentation is a nightmare. Different by plant. Some of it's in Spanish, some of it's supposed to be in Spanish and isn't. About eighteen percent of our hourly workforce is primarily Spanish-speaking, and a growing group speaks Hmong, especially at Wausau.

**[00:17:05] Maya Okafor:** So translation and localization of training material.

**[00:17:10] Monique Archambault:** Translation, simplification. Our safety manuals are written at like a college reading level. That's a problem.

**[00:17:21] Maya Okafor:** That's a great use case, and honestly it's one the union would likely support too.

**[00:17:30] Monique Archambault:** Yes. Exactly.

**[00:17:31] Brian Halvorsen-Tate:** Also, quality. Our quality team writes, um, corrective action reports, CAPAs. They're painful. And customer complaints, warranty claims. Lots of reading.

**[00:17:49] Maya Okafor:** I'm writing all of this down.

**[00:17:52] Brian Halvorsen-Tate:** Ha. I'm sure you are.

**[00:17:56] Maya Okafor:** So what I'm hearing is you'd want the discovery to be structured. Interview each department, find the top opportunities, size them, and pick a handful to go deep on.

**[00:18:12] Brian Halvorsen-Tate:** Yes. And with numbers. Erik is going to ask what we got for the money.

**[00:18:19] Maya Okafor:** On that. What does the budget look like?

**[00:18:24] Brian Halvorsen-Tate:** So, the licenses, I've got that, that's in the IT budget. For services, I have about a hundred and fifty thousand this fiscal year. Fiscal year ends March thirty-first. I could probably find more for next year if this goes well.

**[00:18:45] Maya Okafor:** Okay. And the timeline you're working toward?

**[00:18:50] Brian Halvorsen-Tate:** I want licenses live by January. Erik wants to announce it at the all-hands in late January, the annual kickoff. That's the moment.

**[00:19:04] Monique Archambault:** And I need the union briefing before that. So early January at the latest. Ideally December.

**[00:19:13] Maya Okafor:** Okay. That's tight but very doable for a foundation phase. Governance, admin config, a champion network, and training for a first wave. The deeper use-case work would run after the launch.

**[00:19:32] Brian Halvorsen-Tate:** That sequence makes sense.

**[00:19:36] Maya Okafor:** Are you talking to anyone else for this?

**[00:19:41] Brian Halvorsen-Tate:** Our Microsoft partner, they've pitched a Copilot adoption program. It's pretty cheap, honestly, because Microsoft subsidizes it. And a big consulting firm pitched an "AI transformation" program, but it was a seven-figure number and a lot of slides.

**[00:20:05] Monique Archambault:** It was a lot of slides.

**[00:20:09] Maya Okafor:** Ha. What did you think of the Copilot pitch?

**[00:20:14] Brian Halvorsen-Tate:** It's fine. It's generic. They didn't ask a single question about the union or the plants. It was like, this is the same deck they use for a bank.

**[00:20:28] Monique Archambault:** That's what bothered me most.

**[00:20:32] Maya Okafor:** That's useful to know. I'll be honest, if you end up with both Copilot and Claude, that's fine, and we'd help you figure out who gets what. We're not religious about it.

**[00:20:46] Brian Halvorsen-Tate:** Appreciate that.

**[00:20:49] Monique Archambault:** Oh, sorry, I'm getting, the shift supervisor's waving at me. Can I have two minutes? I'm going to mute.

**[00:20:58] Maya Okafor:** Of course.

*[00:21:00 – 00:23:56, Monique Archambault muted / off camera]*

**[00:21:03] Brian Halvorsen-Tate:** While she's away. I'll say, Monique's going to be your biggest ally on this. But she's also carrying a lot. HR is short-staffed. They lost their HRIS analyst in the summer and nobody's backfilled it, so she's doing reporting by hand in Excel.

**[00:21:28] Maya Okafor:** Oof.

**[00:21:29] Brian Halvorsen-Tate:** Yeah. And honestly, the bigger picture for me. I'm looking at the next three years and IT has a lot on its plate. The Epicor upgrade, which is, that's a monster. We've got a homegrown maintenance scheduling app at Dubuque that was written by an intern in, like, 2012, and it's on a server under someone's desk. Literally. And the CEO wants a customer portal, so distributors can check order status, which we can't do today.

**[00:22:11] Maya Okafor:** The server-under-the-desk thing is, honestly, a classic.

**[00:22:17] Brian Halvorsen-Tate:** It's terrifying. If that box dies, Dubuque doesn't know which machines to service. I've been trying to get budget to rewrite it for two years.

**[00:22:29] Maya Okafor:** That's the kind of thing we do a lot of, actually. Small app modernization. Separate conversation. But I'm noting it.

**[00:22:39] Brian Halvorsen-Tate:** Note away.

**[00:22:45] Maya Okafor:** And the Epicor upgrade, who's helping with that?

**[00:22:50] Brian Halvorsen-Tate:** We haven't picked a partner. RFP's going out in Q1.

**[00:22:55] Maya Okafor:** We're not an Epicor shop, so I wouldn't want to pretend. But data migration and cleanup is often where AI helps on those, if that's ever useful.

**[00:23:07] Brian Halvorsen-Tate:** Huh. Data cleanup, yeah. Our item master is a disaster. Forty thousand SKUs, a lot of duplicates.

**[00:23:18] Maya Okafor:** Mm. Very common.

**[00:23:58] Monique Archambault:** Sorry, I'm back. Forklift issue. Nothing serious.

**[00:24:05] Maya Okafor:** No problem. We were just chatting. Monique, I wanted to ask you about measurement. How would you know if training and adoption worked?

**[00:24:17] Monique Archambault:** Um. Weekly active users, I guess. But that's not really enough.

**[00:24:24] Maya Okafor:** I'd agree. Usage is a floor. What we usually suggest is three tiers: adoption, so active users and frequency; proficiency, so are people using it for more than basic tasks, which we can see in the analytics and in short skills check-ins; and impact, which is the business metrics on the specific use cases. Like quote turnaround.

**[00:24:56] Monique Archambault:** I like that. Can you send that as a framework?

**[00:25:01] Maya Okafor:** Yes. I'll include it.

**[00:25:05] Brian Halvorsen-Tate:** And success for me, phase one: zero data incidents, sixty percent weekly active among licensed users by end of Q1, and the shadow AI traffic on our network drops by at least half.

**[00:25:24] Maya Okafor:** Those are crisp. Very measurable.

**[00:25:27] Monique Archambault:** And for me: the union hears about it from me first, not from a rumor. And no grievances filed.

**[00:25:38] Maya Okafor:** That's a real success criterion. I'd write that down too.

**[00:25:43] Monique Archambault:** Please do.

**[00:25:45] Maya Okafor:** On the union side, would it be helpful if we joined that briefing? Or helped you prepare for it?

**[00:25:55] Monique Archambault:** Help me prepare, yes. Join, probably not. They'd see consultants as a red flag. No offense.

**[00:26:06] Maya Okafor:** None taken. Totally makes sense.

**[00:26:09] Brian Halvorsen-Tate:** Okay. Next steps. What do you need from us?

**[00:26:15] Maya Okafor:** Here's what I'd suggest. I'll send a proposal for a foundation phase: governance and policy, Enterprise admin setup, a champion program built from the pilot group, in-person training at all three plants for the first wave, and support for the union briefing. Sized to fit under the hundred-fifty this fiscal year. Then a separate, optional discovery phase for the use cases, quoting, onboarding translation, CAPAs, and so on, which could land in next fiscal year.

**[00:26:57] Brian Halvorsen-Tate:** That's good. Can you get it to me by end of next week?

**[00:27:02] Maya Okafor:** Yes. By the thirtieth.

**[00:27:05] Brian Halvorsen-Tate:** And can you include a draft of the AI acceptable use policy? Even rough? Patricia will move faster with something to mark up.

**[00:27:18] Maya Okafor:** I can include a sample outline, based on what other manufacturers have done. I'd want to be careful it's not legal advice, but a starting structure, sure.

**[00:27:32] Monique Archambault:** And the measurement framework.

**[00:27:35] Maya Okafor:** And the measurement framework. One thing I want to check on my side: you mentioned Spanish and Hmong. I want to confirm how Claude handles Hmong specifically before I promise anything on the translation use case. Spanish I'm confident about. Hmong I need to look into.

**[00:28:00] Monique Archambault:** That's fair. I appreciate you not just saying yes.

**[00:28:05] Maya Okafor:** Ha. And I'll also come back to you on whether we can do the plant trainings in the timeframe. Three sites in January with a kickoff at the end of the month, I want to check staffing before I commit.

**[00:28:22] Brian Halvorsen-Tate:** Okay.

**[00:28:24] Maya Okafor:** From your side: Brian, could you share the pilot survey results, and the network scan summary, whatever you're comfortable with? And the existing data classification policy.

**[00:28:38] Brian Halvorsen-Tate:** I can do that.

**[00:28:40] Maya Okafor:** And Monique, if there's a list of the pilot participants and departments, that helps for the champion design.

**[00:28:49] Monique Archambault:** Sure. I'll send it. Todd included.

**[00:28:54] Maya Okafor:** Ha. Todd especially.

**[00:28:57] Brian Halvorsen-Tate:** And let's set up a follow-up once we have the proposal. Maybe the week of November ninth? Patricia should join that one.

**[00:29:08] Maya Okafor:** Perfect. I'll send times.

**[00:29:11] Monique Archambault:** I've got to go, the shift change is happening. Thank you, Maya.

**[00:29:17] Maya Okafor:** Thanks Monique, thanks Brian. Talk soon.

**[00:29:20] Brian Halvorsen-Tate:** Thanks.

*[Meeting ended at 00:29:24]*
