# Discovery Call: Lakeshore Health Partners x Scope Creepers

- **Category:** sales-discovery
- **Date:** 2026-10-02
- **Duration:** 29 min
- **Platform:** Microsoft Teams
- **Call type:** First discovery call (prospect)

## Attendees

| Name | Company | Role |
|---|---|---|
| Maya Okafor | Scope Creepers | Partner / Account Executive |
| Denise Kowalczyk | Lakeshore Health Partners | VP, Revenue Cycle |
| Arturo Benavides | Lakeshore Health Partners | Director of IT Security |

---

## Transcript

**[00:00:06] Maya Okafor:** Hi, good morning. Can you hear me okay?

**[00:00:10] Denise Kowalczyk:** Morning, yes, we can hear you. Arturo's here with me in the conference room, we're just on one camera.

**[00:00:18] Arturo Benavides:** Hello.

**[00:00:19] Maya Okafor:** Great, hi Arturo. Thanks to you both for making time. I know Fridays get eaten up. How's the weather up there? I saw you had that storm come through earlier this week.

**[00:00:31] Denise Kowalczyk:** Oh, it was bad Tuesday. We had a generator test at Northshore that turned into an actual generator event, so. That was a fun day. It's fine now.

**[00:00:45] Maya Okafor:** Glad everything held up. Okay, so I have us for thirty minutes. My goal today is mostly to listen. I'd love to understand what's going on with prior auth, what you've tried, and then whether it even makes sense for us to keep talking. Does that work?

**[00:01:06] Denise Kowalczyk:** Works for me.

**[00:01:07] Arturo Benavides:** Before we get into it, I want to be upfront. I'm here mostly to ask about data handling. So if I'm quiet for a while, that's why. But I will have questions.

**[00:01:19] Maya Okafor:** That's totally fair, and honestly I'd rather hear them early than late. We can save some time at the end specifically for you, or just jump in whenever.

**[00:01:31] Arturo Benavides:** Jumping in is fine.

**[00:01:34] Maya Okafor:** Okay. Denise, maybe start with the big picture. What does prior authorization look like at Lakeshore today?

**[00:01:45] Denise Kowalczyk:** Sure. So, six hospitals, plus we have, um, around forty ambulatory clinics that roll up under us. Prior auth is centralized. We have a central authorization team, it's twenty-two FTEs right now, and then there's a handful of people embedded at the two biggest sites, Lakeshore Main and St. Brendan's, because the surgical volume there is just much higher.

**[00:02:21] Maya Okafor:** And roughly what volume does that team handle?

**[00:02:25] Denise Kowalczyk:** We're running about thirty-eight hundred auth requests a week across the system. Imaging is the biggest chunk, then surgical, then specialty drugs. Specialty pharmacy is the one growing fastest, that's up maybe thirty percent year over year.

**[00:02:48] Maya Okafor:** And when you say the work is the paperwork, what specifically is eating the time?

**[00:02:55] Denise Kowalczyk:** It's the clinical documentation part. The request itself isn't hard. It's that each payer wants the clinical justification in their own format, and somebody has to go into the chart, find the relevant notes, the imaging history, the conservative therapy that was tried, the labs, and then summarize it into whatever the payer portal wants. We timed it last spring. Average was twenty-six minutes per request on the clinical summary piece alone. For the complex ones, oncology, spine, it's over an hour.

**[00:03:42] Maya Okafor:** Twenty-six minutes times thirty-eight hundred a week is... a lot.

**[00:03:46] Denise Kowalczyk:** It's about sixteen hundred hours a week. And that's before the denials.

**[00:03:52] Maya Okafor:** Tell me about the denials.

**[00:03:55] Denise Kowalczyk:** Our initial denial rate on prior auth is around eleven percent. A big share of that is "insufficient documentation," which is maddening because the documentation usually exists, it's in the chart, it just didn't make it into the submission. And then a denial means a peer-to-peer or an appeal, and that's physician time, which is the most expensive time we have.

**[00:04:27] Maya Okafor:** Do you know what the denials are costing you? Even roughly.

**[00:04:33] Denise Kowalczyk:** Our finance team put the write-offs tied to auth denials at about four point two million last fiscal year. That's the number that got the board's attention, frankly.

**[00:04:48] Maya Okafor:** Okay. That's helpful context. And has the board attention turned into a specific initiative, or is it more of a "fix this" mandate?

**[00:05:00] Denise Kowalczyk:** Um, both? There's a revenue integrity initiative that our CFO, Tom Hadley, is sponsoring for fiscal '27. Prior auth is one of the three pillars. The other two are coding accuracy and, uh, underpayment recovery. So I own the auth piece.

**[00:05:25] Maya Okafor:** Got it. And fiscal '27 starts when for you?

**[00:05:30] Denise Kowalczyk:** July first. So budgets are getting built right now, basically between now and February.

**[00:05:39] Maya Okafor:** That's useful. So if something were going to happen, the money would need to be identified in the next few months.

**[00:05:48] Denise Kowalczyk:** Right. Or, I have some discretionary in this year's budget for a pilot. Not a lot. But enough for a proof of concept if it's scoped tightly.

**[00:06:01] Maya Okafor:** Okay. I won't ask you for a number yet. What have you tried so far?

**[00:06:09] Denise Kowalczyk:** We brought in templates, which helped a little. We tried outsourcing a portion to an offshore vendor two years ago, for imaging only. That was a disaster on quality, the denial rate on that batch went up, not down. We pulled it back in-house after eight months.

**[00:06:33] Arturo Benavides:** And that vendor is part of why I'm on this call.

**[00:06:37] Maya Okafor:** Say more?

**[00:06:39] Arturo Benavides:** We had a, it wasn't a breach, technically. But we found out during an audit that they had PHI sitting on a shared drive that wasn't covered by what they'd told us in the security questionnaire. So, everybody who touches our data now gets a much closer look.

**[00:07:01] Maya Okafor:** That's completely understandable. I'd want the same thing. Can I ask what your review process looks like now? Like, what does a vendor have to clear?

**[00:07:13] Arturo Benavides:** BAA, obviously, before anything. Our third-party risk questionnaire, it's about two hundred and forty questions. SOC 2 Type II. And then for anything AI, we've added a section in the last year. Where does the data go, is it used for training, retention, who has access, what's the subprocessor list. And honestly the question I'm going to ask you right now is: would PHI go to Anthropic, or OpenAI, or whoever, and under what terms.

**[00:07:54] Maya Okafor:** Yeah. So, the short version, and I want to be careful not to over-promise here. When we build on Claude for healthcare clients, we route through a deployment that's covered under a BAA. That can be Anthropic directly, or through a cloud provider like AWS Bedrock, where a lot of health systems already have a BAA in place. Zero data retention configurations are available, and the model provider doesn't train on that data. Scope Creepers ourselves would also sign a BAA with you, because during build our engineers may see PHI in test cases.

**[00:08:42] Arturo Benavides:** Do you have a SOC 2?

**[00:08:45] Maya Okafor:** We have a SOC 2 Type I. Type II, the audit window closes in, um, I believe January. I'll confirm that date, I don't want to give you the wrong month.

**[00:08:58] Arturo Benavides:** Okay. That's going to come up.

**[00:09:01] Maya Okafor:** Understood. And for what it's worth, a lot of our health clients have had us operate entirely inside their cloud tenant, so we don't hold data on our side at all. Is Lakeshore on AWS, Azure?

**[00:09:18] Arturo Benavides:** Azure, mostly. Some AWS from an acquisition.

**[00:09:22] Maya Okafor:** Okay. That's workable either way. I'll make a note.

**[00:09:28] Denise Kowalczyk:** Can I go back to something? Because I want to make sure we talk about the elephant in the room, which is Epic.

**[00:09:37] Maya Okafor:** Please.

**[00:09:39] Denise Kowalczyk:** So, we're on our EHR, it's, the vendor has an AI add-on for prior auth that they've been pitching hard. It's in their roadmap, some of it's live. And there's a camp internally, mostly in IT, that says just wait for that, it's integrated, it's under our existing contract.

**[00:10:03] Arturo Benavides:** I'm in that camp, for the record. Partially.

**[00:10:07] Maya Okafor:** That's a really reasonable position. What would make you not want to wait?

**[00:10:15] Denise Kowalczyk:** Timing, mostly. The pieces that are live only cover a subset of payers. Our two biggest commercial payers, plus Medicaid managed care, which is like forty percent of our volume, aren't in the first release. And the pricing, we got a quote. It's per-transaction and it's, um, it's not cheap. I'd rather not say the number on this call.

**[00:10:46] Maya Okafor:** No problem.

**[00:10:48] Arturo Benavides:** The counterpoint is that anything you build sits outside the EHR, so now I've got another integration, another place PHI flows, another thing to monitor.

**[00:11:01] Maya Okafor:** That's fair. And honestly, I'd push back gently on framing it as either/or. In a couple of our engagements, the work we did was the layer that fills the gaps, the payers or service lines the vendor doesn't cover, and then it gets retired or reduced as the vendor catches up. Or it's the pieces upstream of the portal, pulling the clinical evidence out of the chart into a summary, which the vendor tool doesn't do especially well yet. I don't want to talk you out of your EHR vendor. I'd want to understand where the gap actually is.

**[00:11:46] Denise Kowalczyk:** That's, yeah. That's how I've been thinking about it too.

**[00:11:51] Arturo Benavides:** Hm.

**[00:11:54] Maya Okafor:** Can I ask about integration? How does your team get the clinical notes today? Are they in the EHR directly, or is there an extract?

**[00:12:04] Denise Kowalczyk:** They're in the EHR, they work right out of the work queues. Some stuff comes from outside, like outside imaging reports come in as scanned PDFs or faxes. Which is its own nightmare.

**[00:12:21] Maya Okafor:** Faxes still?

**[00:12:22] Denise Kowalczyk:** Oh, faxes are alive and well in healthcare. Our HIM department, health information management, they get something like, gosh, I think nine thousand inbound fax pages a day across the system. Records requests, outside results, referrals. They index all of that by hand. That team is drowning too, honestly, but that's not my department.

**[00:12:52] Maya Okafor:** Who owns that?

**[00:12:54] Denise Kowalczyk:** Rachel Osei, she's the director of HIM. She'd probably love to talk to you, but let's not get ahead of ourselves.

**[00:13:03] Maya Okafor:** Ha, fair. I'll just note it.

**[00:13:07] Arturo Benavides:** Interfaces. We have FHIR APIs available, and an integration engine. Anything new goes through the integration team, and they have a queue. A long one.

**[00:13:21] Maya Okafor:** How long is long?

**[00:13:24] Arturo Benavides:** For a new interface? Realistically, three to five months to get on the schedule. Unless it's tied to something the CFO cares about.

**[00:13:34] Denise Kowalczyk:** Which this is.

**[00:13:36] Arturo Benavides:** Which this is, yes.

**[00:13:39] Maya Okafor:** Okay, so that's a real constraint for any timeline. For a pilot, would read-only access be easier? Like, we'd pull notes for a defined set of auth requests, generate the clinical summary, and a human on Denise's team reviews it before it goes anywhere. Nothing writes back to the chart.

**[00:14:03] Arturo Benavides:** Read-only is easier. It's still PHI. It's still a full review.

**[00:14:09] Maya Okafor:** Understood.

**[00:14:12] Denise Kowalczyk:** And human review is non-negotiable for me anyway. I'm not having a model submit to a payer by itself. Not in year one.

**[00:14:22] Maya Okafor:** Agreed. I wouldn't recommend that either. Let me ask about success. If we did a pilot, say twelve weeks, what would you need to see to call it a win?

**[00:14:36] Denise Kowalczyk:** Um. Time per request down meaningfully. I'd say if we get the twenty-six minutes to under ten on the targeted service line, that's a win. And documentation-related denials down. I'd want to see the denial rate on the pilot batch compared to a control.

**[00:15:01] Maya Okafor:** Which service line would you pick?

**[00:15:04] Denise Kowalczyk:** Advanced imaging. MRI and CT. It's the highest volume, it's the most templated, and the payers are pretty consistent about what they want. If it can't work there, it can't work anywhere.

**[00:15:21] Maya Okafor:** That makes sense. Arturo, what does success look like for you?

**[00:15:25] Arturo Benavides:** Success for me is I don't find out about anything after the fact. Full audit logging. Every prompt, every output, retained on our side. I want to know who reviewed what. And I want a kill switch.

**[00:15:43] Maya Okafor:** All doable. The audit logging is actually something we'd build in regardless, because Denise is going to need it for the denial comparison anyway.

**[00:15:54] Arturo Benavides:** Also. I want to understand hallucination risk. If the model says the patient had six weeks of physical therapy and they had two, that's, that's potentially a false claim. That's compliance, not just a denial.

**[00:16:12] Maya Okafor:** Yes. That's the most important design question in this whole thing, honestly. The way we handle it is that every statement in the summary is cited back to a specific source document and date in the chart, and the reviewer sees the citation next to the claim. If the model can't find support, it says "not found," it doesn't fill the gap. And we'd measure accuracy during the pilot, not just speed.

**[00:16:45] Arturo Benavides:** Has that been tested? Like with real numbers?

**[00:16:49] Maya Okafor:** In a different context, a specialty pharmacy client, we measured it on, I think around fifteen hundred summaries. I'd have to pull the exact numbers and I'd want to check what I'm allowed to share. Let me take that as a follow-up.

**[00:17:07] Arturo Benavides:** Okay.

**[00:17:10] Denise Kowalczyk:** Sorry, can I also mention, our compliance officer is going to want to be involved. Gloria Pham. She sits on the AI governance committee.

**[00:17:21] Maya Okafor:** You have an AI governance committee? That's great, actually.

**[00:17:25] Arturo Benavides:** Formed in March. It meets monthly. Anything AI touching patients or PHI goes through it.

**[00:17:33] Maya Okafor:** When's the next one?

**[00:17:34] Arturo Benavides:** Third Thursday of the month. So, October twenty-second? No. Fifteenth. The fifteenth.

**[00:17:42] Denise Kowalczyk:** It's the fifteenth.

**[00:17:43] Maya Okafor:** Okay. And then November would be the nineteenth. Is there a way to get on the agenda, or is it too early?

**[00:17:52] Arturo Benavides:** It's too early for October. November maybe, if there's a written proposal with the data flow.

**[00:18:00] Maya Okafor:** Got it. Out of curiosity, what else is in front of that committee right now? Just to understand what you're comparing things to.

**[00:18:10] Arturo Benavides:** Ambient scribing is the big one. The physicians want it badly. There's a pilot with eleven docs in primary care. And there's a patient-facing chatbot proposal from marketing that I'm, uh, not excited about.

**[00:18:28] Denise Kowalczyk:** And I think nursing has something about shift handoff notes? I saw it on the agenda.

**[00:18:34] Arturo Benavides:** That's early. It's an idea, not a proposal.

**[00:18:39] Maya Okafor:** Interesting. Okay. Let me ask about the decision. Assuming a pilot made sense and cleared security and governance, who signs?

**[00:18:51] Denise Kowalczyk:** Under a certain threshold, me. Above it, Tom, the CFO. And honestly if it's going to scale past a pilot, Tom will want to see it regardless, because it's in his revenue integrity program.

**[00:19:07] Maya Okafor:** Is there a procurement team that gets involved?

**[00:19:10] Denise Kowalczyk:** Supply chain does contracts, yeah. They're slow but they're not the bottleneck. Arturo's review is the bottleneck.

**[00:19:19] Arturo Benavides:** Thank you, Denise.

**[00:19:22] Denise Kowalczyk:** I say it with love.

**[00:19:24] Maya Okafor:** Ha. How long does the security review usually take?

**[00:19:28] Arturo Benavides:** If the questionnaire comes back complete and clean, six weeks. If it doesn't, longer. Most vendors take two or three rounds.

**[00:19:39] Maya Okafor:** Okay. One thing that could help is if we did the questionnaire in parallel with scoping, rather than waiting until the end. Would you be open to sending it over early?

**[00:19:51] Arturo Benavides:** I can send it. I'll need an NDA first.

**[00:19:55] Maya Okafor:** Totally. We'll send our mutual NDA today, or we can sign yours if that's easier.

**[00:20:03] Arturo Benavides:** Ours. Legal prefers ours.

**[00:20:06] Maya Okafor:** Works for us.

**[00:20:09] Denise Kowalczyk:** Let me ask you something. What would this cost, ballpark? I know you can't really say yet.

**[00:20:16] Maya Okafor:** I can give you a range with a lot of caveats. A tightly scoped pilot like the imaging one, twelve weeks, with integration through read-only FHIR and a reviewer interface, usually lands somewhere in the low-to-mid six figures for our services. Model costs on top, but at your volume those are small relative to labor. If the integration has to go through your integration team's queue, that affects timing more than cost.

**[00:20:52] Denise Kowalczyk:** Okay. That's... in the range I was hoping, on the low end. Mid six figures would need Tom.

**[00:21:01] Maya Okafor:** Understood. We can scope to fit. And honestly, a pilot sized for your discretionary budget, that then makes the case for the fiscal '27 money, is a pattern we see a lot.

**[00:21:16] Denise Kowalczyk:** That's exactly the play I'd want to run.

**[00:21:21] Maya Okafor:** Can I ask about the team itself? Twenty-two FTEs. Is the goal to reduce headcount, or redeploy?

**[00:21:30] Denise Kowalczyk:** Redeploy. I have nine open reqs I can't fill. Turnover on the auth team is over thirty percent. These are hard jobs, and they're boring jobs, and people leave. If I could stop backfilling and move people to denials and appeals work, that's the win.

**[00:21:52] Maya Okafor:** That's a really different story than headcount reduction, and probably an easier one internally.

**[00:21:58] Denise Kowalczyk:** Much easier. We have an employee engagement problem in revenue cycle generally. Patient financial services, the billing office, they're losing people too. Same problem, tons of reading and summarizing. Appeals letters, for example. My appeals team writes, gosh, maybe four hundred appeal letters a month, all by hand.

**[00:22:25] Maya Okafor:** Appeal letters are a really natural extension, actually, if the summary layer exists. Same evidence, different output.

**[00:22:34] Denise Kowalczyk:** That's what I was thinking. But one thing at a time.

**[00:22:39] Maya Okafor:** One thing at a time. Arturo, what am I not asking that I should be?

**[00:22:45] Arturo Benavides:** Where are your engineers located?

**[00:22:48] Maya Okafor:** All US-based for healthcare engagements. We have some contractors in Canada, but they don't touch PHI projects.

**[00:22:57] Arturo Benavides:** Okay. And what happens to the prompts and the code at the end of the engagement? Who owns it?

**[00:23:04] Maya Okafor:** You do. Standard in our MSA, all work product transfers to the client. We'd hand over the repo, the prompts, the evaluation sets, the documentation.

**[00:23:16] Arturo Benavides:** And if you're gone, can my team run it?

**[00:23:21] Maya Okafor:** That's the intent. We'd want someone on your side shadowing from the start. Do you have an internal team who'd own it?

**[00:23:30] Arturo Benavides:** Not really. That's a gap. We have an applications team that's all EHR analysts. Nobody's doing this kind of development.

**[00:23:40] Denise Kowalczyk:** There's been talk about standing up a data and AI team under the CIO. It's in the strategic plan. Nothing funded yet.

**[00:23:51] Maya Okafor:** That's good to know. We've helped a couple of systems stand up that kind of center-of-excellence function, so, something to come back to later.

**[00:24:01] Arturo Benavides:** Let's see if this works first.

**[00:24:04] Maya Okafor:** Totally fair.

**[00:24:07] Denise Kowalczyk:** Oh, shoot. I have a hard stop in about five, I have to go to Northshore for a site visit. Can we talk next steps?

**[00:24:16] Maya Okafor:** Yes. Let me play back what I heard and you tell me what I got wrong. Thirty-eight hundred auth requests a week, about twenty-six minutes each on the clinical summary, eleven percent initial denial rate, four point two million in write-offs tied to auth denials. Advanced imaging is the pilot candidate. Success is under ten minutes per request and fewer documentation denials versus a control. Human review always. Arturo needs a BAA, full audit logging on your side, a kill switch, and a clean questionnaire. Governance committee in November if we have a written proposal with the data flow. And the EHR vendor's add-on is the alternative, so we should be specific about where we fill the gap rather than compete.

**[00:25:19] Denise Kowalczyk:** That's right. I'd add, Tom needs to hear the number four point two million in whatever you write. That's what he'll anchor on.

**[00:25:30] Maya Okafor:** Noted. Next steps from my side: I'll send over a short proposal for a twelve-week imaging pilot, including a data flow diagram that Arturo can take to governance. I'll confirm our SOC 2 Type II date. And I'll check what I can share about the accuracy results from the specialty pharmacy work.

**[00:25:55] Arturo Benavides:** And the NDA.

**[00:25:57] Maya Okafor:** And sign your NDA. If you can send it over, we'll turn it in a day.

**[00:26:03] Arturo Benavides:** I'll have legal send it. Then the questionnaire.

**[00:26:07] Denise Kowalczyk:** And I'll pull together a sample of de-identified auth requests so you can see what we're dealing with. Maybe twenty or thirty. Arturo, is de-identified okay before the BAA?

**[00:26:22] Arturo Benavides:** De-identified to safe harbor standard, yes. I'll want to look at them before they go out.

**[00:26:30] Denise Kowalczyk:** Fine.

**[00:26:31] Maya Okafor:** When would be a good time for a follow-up? I'm thinking two weeks, after you've seen the proposal.

**[00:26:39] Denise Kowalczyk:** Week of the nineteenth works. After governance meets, actually, so I can hear what else is in the pipeline.

**[00:26:48] Maya Okafor:** Perfect. I'll send a couple of times.

**[00:26:51] Arturo Benavides:** One more. Your proposal should say what happens if the model provider has an outage. Our auth team can't stop working.

**[00:27:01] Maya Okafor:** Good point. The fallback is just the current manual process, but I'll write it up explicitly. And we'd want to talk about whether you'd want a second model provider as backup. I'll think about how we'd handle that, I don't have a crisp answer for you right now.

**[00:27:21] Arturo Benavides:** Okay.

**[00:27:22] Denise Kowalczyk:** Alright, I have to run. Maya, thank you, this was really helpful.

**[00:27:28] Maya Okafor:** Thank you, Denise. Good luck at Northshore.

*[Denise Kowalczyk left the meeting at 00:27:33]*

**[00:27:36] Maya Okafor:** Arturo, anything else while I have you?

**[00:27:40] Arturo Benavides:** Hm. Not really. I'll just say, I'm not against this. I've seen the auth team. I know it's bad. I just don't want to be the guy explaining a breach to the board.

**[00:27:54] Maya Okafor:** I completely get that. And honestly, I'd rather work with a security team that's careful. It makes the project better.

**[00:28:03] Arturo Benavides:** We'll see. The questionnaire is long.

**[00:28:07] Maya Okafor:** Ha. We've done a few. Can I ask, offhand, the AWS environment from the acquisition, is that something you're planning to consolidate?

**[00:28:18] Arturo Benavides:** Eventually. It's the old Bayview Medical Group stuff. There's a bunch of legacy apps over there nobody wants to touch. Some old patient scheduling thing, a custom referral tracker written in, I don't even know. It's on my list of risks.

**[00:28:37] Maya Okafor:** That kind of thing is actually a big part of what we do, legacy app modernization. Not today's conversation. But if it's ever useful.

**[00:28:48] Arturo Benavides:** Noted. Okay. I have to go too.

**[00:28:52] Maya Okafor:** Thanks, Arturo. I'll look for the NDA.

**[00:28:55] Arturo Benavides:** Bye.

*[Meeting ended at 00:28:58.]*
