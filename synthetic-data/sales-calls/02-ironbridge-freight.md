# Discovery Call: Ironbridge Freight x Scope Creepers

- **Category:** sales-discovery
- **Date:** 2026-10-08
- **Duration:** 31 min
- **Platform:** Zoom
- **Call type:** First discovery call (prospect)

## Attendees

| Name | Company | Role |
|---|---|---|
| Maya Okafor | Scope Creepers | Partner / Account Executive |
| Dev Patel | Scope Creepers | Principal Solutions Engineer |
| Marcus Delgado | Ironbridge Freight | Chief Technology Officer |
| Gary Lindqvist | Ironbridge Freight | Lead Developer, Dispatch Systems |

---

## Transcript

**[00:00:03] Marcus Delgado:** There they are. Hey! Maya, Dev, good to meet you.

**[00:00:09] Maya Okafor:** Hi Marcus, great to finally put a face to the emails. And this must be Gary.

**[00:00:16] Gary Lindqvist:** That's me. Sorry, my camera's being weird, give me a second.

**[00:00:25] Dev Patel:** No rush. Is that a, is that a truck model behind you, Marcus?

**[00:00:32] Marcus Delgado:** Ha, yes. That's a 1979 Kenworth W900. My dad drove one just like it. Ironbridge started with four of those. Now we're at about eleven hundred tractors, so, things have changed a bit.

**[00:00:51] Dev Patel:** That's great.

**[00:00:54] Gary Lindqvist:** Okay, I'm here. Video's there now?

**[00:00:57] Maya Okafor:** We see you. Welcome.

**[00:01:00] Marcus Delgado:** So, I'll be honest, I'm pretty fired up about this. I read the case study you sent about the insurance policy admin migration and I sent it to Gary at eleven at night with like four exclamation points.

**[00:01:18] Gary Lindqvist:** He did. I was asleep.

**[00:01:21] Maya Okafor:** Ha. Well, I'm glad it landed. Here's what I'd suggest for today. We'd love to understand the dispatch system, what's driving the timing, what happened in 2022, since you mentioned it in your email, and then Dev can talk a bit about how we'd approach it. Does that work?

**[00:01:44] Marcus Delgado:** Perfect.

**[00:01:47] Maya Okafor:** Okay. So, Marcus, give us the lay of the land.

**[00:01:52] Marcus Delgado:** Alright. So the core system is called DART. Dispatch And Routing Tool. Gary's predecessor named it. It runs everything. Load tendering, driver assignment, dispatch, check calls, it calculates driver pay, it does some of the billing feeds. The front end is VB6. Yes, still. Some of the newer modules are .NET Framework 3.5 WinForms, and there's a SQL Server back end with, Gary, how many stored procedures?

**[00:02:36] Gary Lindqvist:** Last time I counted, about nineteen hundred. Some of them are dead. I don't know which ones.

**[00:02:44] Marcus Delgado:** Nineteen hundred stored procedures, a lot of business logic in them, and a lot of business logic in the VB6 too. And it's about, what, six hundred thousand lines?

**[00:02:59] Gary Lindqvist:** Somewhere around there across everything. The VB6 piece is maybe two hundred and fifty thousand.

**[00:03:07] Dev Patel:** And how many people use it day to day?

**[00:03:12] Marcus Delgado:** About a hundred and forty dispatchers and planners across four terminals. Plus billing, plus safety, plus the driver managers. Call it two hundred and twenty users.

**[00:03:26] Maya Okafor:** And it's all on-prem?

**[00:03:29] Gary Lindqvist:** On-prem, Citrix for the remote terminals. Which, the Citrix part is held together with tape.

**[00:03:39] Maya Okafor:** So what's driving the timing now? Why this year?

**[00:03:44] Marcus Delgado:** A few things. One, honestly, is Gary.

**[00:03:50] Gary Lindqvist:** Here it comes.

**[00:03:52] Marcus Delgado:** Gary's been with us twenty-three years. Gary's told us he's retiring end of 2027. And Gary is, and I say this with total respect, the only human being alive who understands how driver pay is calculated in DART.

**[00:04:12] Gary Lindqvist:** That's, unfortunately, true. There's one other guy who knew some of it, Ray, and he left in 2019.

**[00:04:22] Dev Patel:** How much of it is documented?

**[00:04:25] Gary Lindqvist:** Um. There's a binder.

**[00:04:28] Dev Patel:** A binder.

**[00:04:30] Gary Lindqvist:** A physical binder. It's from 2011. It's maybe forty percent right.

**[00:04:38] Marcus Delgado:** So that's risk number one. Risk number two, we can't hire. Nobody wants to write VB6. We posted a role last year, got three applicants, two of them were over sixty-five.

**[00:04:54] Maya Okafor:** Ha. Oh no.

**[00:04:56] Marcus Delgado:** And three, the business wants things DART can't do. Customers want real-time ETAs through an API. Our biggest shipper, a big-box retailer, is requiring API-based tendering by Q3 next year or we lose preferred carrier status. That's about eighteen percent of revenue.

**[00:05:23] Maya Okafor:** That's a real deadline.

**[00:05:26] Marcus Delgado:** That's the deadline. Q3 2027. The board knows about it.

**[00:05:32] Dev Patel:** Can I ask about 2022? You mentioned a rewrite that didn't go well.

**[00:05:39] Marcus Delgado:** Yeah. So, uh, painful story. We hired a, a big systems integrator, not going to name them, to do a full rewrite. Ground up, new platform, cloud native, the whole pitch. Eighteen month plan. They spent fourteen months gathering requirements and building a new UI, and when they tried to replicate driver pay, the numbers didn't match, and they couldn't figure out why, and.

**[00:06:17] Gary Lindqvist:** And they never asked me. Well, they asked me, but they asked me in two-hour workshops where I was supposed to explain thirty years of logic from memory.

**[00:06:30] Marcus Delgado:** We pulled the plug after fourteen months. We'd spent two point one million. We got a nice UI mockup out of it.

**[00:06:41] Maya Okafor:** I'm sorry. That's a rough one.

**[00:06:44] Marcus Delgado:** It was. And I'll tell you, the CEO, Pat, still brings it up. So I have to be very careful about how I pitch this internally. If it smells like another big-bang, I'm done.

**[00:07:00] Dev Patel:** That's actually a really good segue. Can I tell you how we'd think about it differently, and then you can poke holes?

**[00:07:08] Marcus Delgado:** Please.

**[00:07:12] Dev Patel:** So, the biggest thing is we wouldn't start with the UI or the new architecture. We'd start with understanding. We'd use Claude to read the entire codebase, the VB6, the WinForms, all nineteen hundred stored procedures, and build a map. What calls what, what tables each piece touches, what's dead code. Then for the critical business logic, driver pay first, we'd generate plain-English specs of what the code actually does. Not what the binder says. What it does.

**[00:07:56] Gary Lindqvist:** Huh.

**[00:07:58] Dev Patel:** And then Gary reviews those specs. Which is very different from Gary explaining it from memory. Gary's correcting, not authoring. In our experience that's like, a tenth of the effort for him.

**[00:08:16] Gary Lindqvist:** I'd actually love that. Honestly. There's stuff in there I wrote in 2004 that I don't remember.

**[00:08:24] Dev Patel:** Right. And then the second piece. We build characterization tests from production data. Take, say, the last two years of pay calculations, run them through the old logic and the new logic, and they have to match to the penny. That's how you know you're done. Not when somebody signs off on a requirements doc.

**[00:08:52] Marcus Delgado:** That's exactly what the SI didn't do.

**[00:08:56] Dev Patel:** And then the third piece is strangler pattern. You don't replace DART. You carve off one capability at a time, put an API in front of it, and DART keeps running. So for your retailer deadline, the first thing you'd carve off is probably tendering, because that's what has the external API requirement.

**[00:09:23] Gary Lindqvist:** Tendering is actually one of the cleaner modules. That was the .NET rewrite, from like 2014.

**[00:09:31] Dev Patel:** Oh that's good news.

**[00:09:34] Marcus Delgado:** See, Gary? I told you these guys would get it.

**[00:09:39] Gary Lindqvist:** I'm cautiously optimistic.

**[00:09:42] Maya Okafor:** Gary, what would worry you about this approach?

**[00:09:47] Gary Lindqvist:** Um. Honestly? A couple things. One, the VB6 code isn't, it's not clean. There's a lot of global variables. There's stuff where the business logic lives in a button click handler. I've seen tools that claim to convert VB6 and they produce garbage.

**[00:10:12] Dev Patel:** Totally. And to be clear, we're not running a converter. The model's reading the code the way a senior engineer would, and we validate everything with the tests. Where it's wrong, the tests catch it. But yeah, the button-click logic is common. We've seen worse.

**[00:10:35] Gary Lindqvist:** And two, I still have a day job. DART breaks. Something breaks every week. If I'm reviewing specs all day, who's on call?

**[00:10:48] Marcus Delgado:** That's fair. That's a real concern.

**[00:10:51] Maya Okafor:** How much of Gary's time would you be able to free up, realistically?

**[00:10:57] Marcus Delgado:** I'd give you, I mean I'd like to say fifty percent.

**[00:11:02] Gary Lindqvist:** You'd like to say.

**[00:11:04] Marcus Delgado:** I'd like to say. Realistically twenty-five, maybe thirty, unless I backfill some of his on-call. And actually, that's something I'd want to ask you about. Could part of this include, like, an AI assistant for the support side? Like, when a dispatcher calls in with a weird error, somebody other than Gary can figure out what's going on?

**[00:11:34] Dev Patel:** Yeah, actually, that falls out of the code map pretty naturally. Once the codebase is indexed, a junior dev can ask "why is this load showing a negative mileage" and get pointed to the right procedure.

**[00:11:52] Gary Lindqvist:** Okay, that I would pay for personally.

**[00:11:56] Maya Okafor:** Ha. Who else is on your team, Marcus? Who would work with us?

**[00:12:03] Marcus Delgado:** So IT's about thirty people total. Development is eight, including Gary. Two of them are decent .NET Core developers, newer hires. The rest are mostly maintaining integrations, EDI, that kind of thing. And then infrastructure and help desk.

**[00:12:27] Dev Patel:** Is there a target stack you'd want? Cloud?

**[00:12:32] Marcus Delgado:** We're moving to Azure. We've got about thirty percent of our workloads there. And I'd want .NET 8 or whatever's current, C#, since that's what my newer folks know.

**[00:12:48] Dev Patel:** Makes sense. And the EDI piece, is that in DART too?

**[00:12:52] Gary Lindqvist:** Partially. The EDI translation is a separate product, a commercial one, but the mapping logic and the 204, 214, 210 handling flows into DART.

**[00:13:07] Marcus Delgado:** And honestly the EDI team is its own mess. We have, um, about three hundred trading partners and every onboarding takes three to six weeks because the maps are hand-built. That's a whole separate conversation.

**[00:13:26] Maya Okafor:** I'm writing it down for later.

**[00:13:29] Marcus Delgado:** Ha, I'm sure you are.

**[00:13:32] Maya Okafor:** Can I ask about budget and decision process? You mentioned the CEO is sensitive to this.

**[00:13:40] Marcus Delgado:** Yeah. So, I have a modernization budget this year that's basically what was left over after we killed the SI contract. It's about seven hundred thousand that has to be committed by end of December, or I lose it. Next year, I've asked for a lot more. Whether I get it depends on whether I can show progress.

**[00:14:11] Maya Okafor:** So there's a use-it-or-lose-it piece.

**[00:14:14] Marcus Delgado:** Yes. Which honestly is part of why I'm pushing. I can sign up to five hundred on my own. Above that, it goes to Pat and the CFO, Linda.

**[00:14:28] Maya Okafor:** And would Pat want to meet us?

**[00:14:32] Marcus Delgado:** Pat would want to meet you before anything over five hundred, yes. Pat's going to ask one question, which is "how is this different from last time." So you'll want to have that answer cold.

**[00:14:48] Dev Patel:** The characterization tests are the answer. Proof, not promises.

**[00:14:54] Marcus Delgado:** I like that. Put that on a slide.

**[00:14:57] Maya Okafor:** Are you talking to anyone else?

**[00:15:00] Marcus Delgado:** Um. Yes. Honestly, a couple. There's an offshore modernization firm that does automated VB6 conversion. Their price is super low. And our Microsoft partner has been pitching something with Copilot. I haven't really engaged with either seriously.

**[00:15:23] Gary Lindqvist:** I looked at the offshore converter output. It was bad. It was VB6 written in C# syntax.

**[00:15:32] Dev Patel:** Yeah, that's the classic problem with transpilers. You get the same mess in a new language.

**[00:15:40] Marcus Delgado:** Exactly. I don't want the same mess. I want to understand it and fix it.

**[00:15:47] Maya Okafor:** Let me ask what success looks like at the end of, say, a first phase. Not the whole migration.

**[00:15:56] Marcus Delgado:** Okay. For me, end of phase one, I want three things. I want a complete map of DART that I can show the board, so they can see I understand what we've got. I want driver pay documented and validated, so if Gary gets hit by a bus, no offense Gary.

**[00:16:20] Gary Lindqvist:** None taken. I'm careful crossing the street.

**[00:16:25] Marcus Delgado:** And I want the tendering API live, or at least in test with the retailer. That's the money one.

**[00:16:33] Dev Patel:** How fast would the retailer API need to be in test? Like what's their certification process?

**[00:16:41] Marcus Delgado:** They give you about ninety days of testing before go-live. So for Q3 next year, I'd want to be in test by, call it, April.

**[00:16:54] Dev Patel:** Okay. That's doable if we start in November, December. Tight but doable. The code map would take maybe four to six weeks, driver pay specs and tests in parallel, and tendering would be the first strangler slice.

**[00:17:13] Gary Lindqvist:** Driver pay won't be four to six weeks. Just so you know. There are union rules, there are owner-operator rules, there are, uh, detention, layover, stop pay, hazmat, team splits. There are special deals with specific drivers from 2008 that nobody remembers agreeing to.

**[00:17:39] Dev Patel:** Ha. Okay, that's helpful, I'll pad it. Honestly that's exactly the kind of thing that the production-data tests catch. The weird special deals show up as mismatches and then we go figure out why.

**[00:17:56] Gary Lindqvist:** That makes sense.

**[00:18:00] Marcus Delgado:** Oh, hang on, I'm getting pinged. Ah, it's, okay, one second.

*[00:18:06 – 00:18:59, Marcus Delgado muted]*

**[00:19:00] Marcus Delgado:** Sorry. A terminal in Gary, Indiana, the city, not our Gary, had a power blip and DART dropped for twelve dispatchers. This is what I'm talking about.

**[00:19:16] Gary Lindqvist:** Do I need to go?

**[00:19:18] Marcus Delgado:** Tony's on it. Stay.

**[00:19:21] Maya Okafor:** Does that happen often?

**[00:19:24] Marcus Delgado:** Monthly. Each outage, every dispatcher is on the phone with drivers manually. We estimate an hour of DART down costs us about forty thousand in delays and missed appointments. We had, I think, nine meaningful outages last year.

**[00:19:45] Maya Okafor:** Okay. That's a number Pat should hear.

**[00:19:50] Marcus Delgado:** Good point.

**[00:19:53] Dev Patel:** Gary, can I ask some technical stuff quickly? Can you share the source code with us early, under NDA? Even just a portion?

**[00:20:04] Gary Lindqvist:** It's in, um, it's in TFS. Team Foundation Server. The old one.

**[00:20:12] Dev Patel:** That's fine. We can work with TFS, or we'd mirror it to Git.

**[00:20:19] Marcus Delgado:** I'd want to check with legal, but yes, I want to do that. I'd love for you to do a quick assessment before we sign anything big.

**[00:20:28] Dev Patel:** We do a two-week paid assessment for exactly this. Code map of a module, a sample spec, and a plan. Fixed fee.

**[00:20:40] Marcus Delgado:** What's the fee?

**[00:20:41] Maya Okafor:** For a codebase this size, the assessment would be in the forty to sixty range. We'd firm that up once Dev sees the repo structure.

**[00:20:52] Marcus Delgado:** That's an easy yes. I can do that this month.

**[00:20:57] Gary Lindqvist:** Can I ask something?

**[00:20:59] Maya Okafor:** Please.

**[00:21:00] Gary Lindqvist:** Does the code go to an AI company? Like, does Anthropic train on our code? Because there's, the pay stuff, there's stuff about specific drivers in there. Comments with names. Some hard-coded SSNs in test procedures from like 2006 that I've been meaning to clean up.

**[00:21:26] Dev Patel:** Good question. No, on the commercial API, Anthropic doesn't train on your data. And we can run everything through your Azure tenant if you prefer. And, uh, the hard-coded SSNs, we'd want to scrub those regardless. Actually the scan would find them for you.

**[00:21:48] Marcus Delgado:** Oh. Gary, that should've been flagged.

**[00:21:53] Gary Lindqvist:** It's on my list! It's been on my list.

**[00:21:56] Marcus Delgado:** Ha. Okay. Add it to the assessment, Dev. Security scan of the codebase. I'm sure there's more in there.

**[00:22:06] Dev Patel:** Noted.

**[00:22:09] Maya Okafor:** Marcus, outside of DART, how is Ironbridge thinking about AI more broadly? Is this a one-off, or part of something bigger?

**[00:22:20] Marcus Delgado:** Oh, it's, honestly, I have a list. A long list. Once DART is unstuck, things like, our safety department reviews dash cam footage and incident reports by hand. Our billing team spends a lot of time matching proof of delivery documents to invoices, they're getting PODs as photos from drivers' phones, and it's, about twelve people do that. Customer service handles about, I think, two thousand "where's my load" calls a week.

**[00:23:02] Gary Lindqvist:** That's the one I'd do first, honestly. If the ETA API exists, the where's-my-load calls go away.

**[00:23:12] Marcus Delgado:** Right, that's the dream. Also, HR. Driver recruiting. We hire, like, four hundred drivers a year to keep eleven hundred trucks filled. Turnover in trucking is brutal. The recruiting team is drowning in applications and DOT paperwork.

**[00:23:34] Maya Okafor:** That's a lot of adjacent opportunity.

**[00:23:37] Marcus Delgado:** And I'll be honest, Pat's going to ask "what's our AI strategy" at the next board meeting in January, because one of the board members sits on the board of a logistics tech company and keeps asking. So I need a story.

**[00:23:56] Maya Okafor:** That's something we help with too. Not necessarily now, but a lightweight AI roadmap, where DART modernization is the foundation and these use cases sit on top of it.

**[00:24:11] Marcus Delgado:** Yes. That. Can you, could the assessment include something like that? Even a page?

**[00:24:19] Maya Okafor:** Let me think about how to scope that. I don't want to promise a board-ready roadmap inside a two-week technical assessment, but maybe a one-page view. Let me get back to you.

**[00:24:33] Marcus Delgado:** Okay. That's fair.

**[00:24:36] Dev Patel:** Gary, quick one. Reporting. Is there reporting off DART?

**[00:24:43] Gary Lindqvist:** Crystal Reports. About three hundred and fifty of them.

**[00:24:48] Dev Patel:** Oh boy.

**[00:24:49] Gary Lindqvist:** Yeah. Finance hates them. They export everything to Excel and redo it. Linda, the CFO, has been asking for a data warehouse for three years.

**[00:25:04] Marcus Delgado:** Which is also on my list. Okay, I'm noticing I just keep adding things.

**[00:25:10] Maya Okafor:** Ha, it's all useful. We'll keep it focused.

**[00:25:15] Marcus Delgado:** Okay, let's talk about what happens next. Because I want to move fast.

**[00:25:21] Maya Okafor:** Love it. Here's what I'd propose. One, we send over our NDA and an SOW for the two-week assessment. Two, Gary gives Dev read access to the repo, or an export. Three, Dev and Gary do a ninety-minute working session where Gary walks through the architecture. Four, at the end of the assessment, we come back with the code map for a module, a sample driver pay spec, a security scan, and a phased plan with the tendering API as phase one.

**[00:26:01] Marcus Delgado:** Yes. Yes to all of that.

**[00:26:04] Gary Lindqvist:** Which module would you map?

**[00:26:08] Dev Patel:** I'd say tendering, since it's the first slice, and a chunk of driver pay, since it's the hardest. That tells us the range.

**[00:26:19] Gary Lindqvist:** Okay. Pick the line-haul pay, not the local pay. Local pay is, uh, you'll want to save that for later.

**[00:26:28] Dev Patel:** Ha. Noted.

**[00:26:32] Maya Okafor:** And Marcus, can we plan for a session with Pat at the end of the assessment? Or before, if it helps?

**[00:26:40] Marcus Delgado:** After. I want to walk in with results. Pat responds to results.

**[00:26:48] Maya Okafor:** Perfect. Should Linda be involved?

**[00:26:51] Marcus Delgado:** Linda, um. Maybe. Let me think about whether that helps or hurts. She was the one who negotiated the SI exit, she's going to be skeptical. But if we pitch the data warehouse angle, she'll lean in.

**[00:27:08] Maya Okafor:** Okay. Your call, you know her.

**[00:27:12] Dev Patel:** Gary, one ask. Do you have any production pay data we could use for test cases? Anonymized.

**[00:27:20] Gary Lindqvist:** I can pull it. Anonymizing it will take me some time, though. That's the kind of thing that eats a week.

**[00:27:28] Dev Patel:** We could help with that. We could write the anonymization script with you.

**[00:27:34] Gary Lindqvist:** That'd help.

**[00:27:36] Marcus Delgado:** Timeline. When could you start?

**[00:27:40] Maya Okafor:** For the assessment, we could start the week of October nineteenth if the paperwork moves this week. Dev, does that work?

**[00:27:50] Dev Patel:** I think so. Let me confirm, I'm finishing something up. I'll know by Monday.

**[00:27:56] Marcus Delgado:** Great. I'll get legal moving on the NDA today.

**[00:28:01] Maya Okafor:** And I'll send the SOW by tomorrow. We'll also send a short written answer on the data handling question, Gary, so you have it in writing for your legal folks.

**[00:28:14] Gary Lindqvist:** Thanks. And if you can, the details on how the model reads VB6. Like, examples. I want to see it do something non-trivial before I get excited.

**[00:28:27] Dev Patel:** I'll put together a sample. Maybe from an open-source VB6 project, so it doesn't need your code. Should have it this week.

**[00:28:38] Gary Lindqvist:** Okay.

**[00:28:40] Marcus Delgado:** Guys, this is great. Honestly, this is the first conversation about DART in two years that didn't make me want to lie down.

**[00:28:51] Maya Okafor:** Ha. We'll take it.

**[00:28:54] Marcus Delgado:** Alright. Gary, you go deal with Indiana.

**[00:28:59] Gary Lindqvist:** Yep. Nice to meet you both.

*[Gary Lindqvist left the meeting at 00:29:04]*

**[00:29:07] Marcus Delgado:** Hey, while Gary's gone, one thing. Off the record, kind of.

**[00:29:13] Maya Okafor:** Sure.

**[00:29:15] Marcus Delgado:** Gary's great. But Gary's also, he's protective of DART. It's his baby. He was a little hurt by the SI thing, they kind of treated him like an obstacle. So, just, be good to him. If Gary's in, this works. If Gary's not, it doesn't.

**[00:29:37] Dev Patel:** Completely understood. Honestly, that's how we'd want to approach it anyway. Gary's the most valuable asset in this whole project.

**[00:29:48] Marcus Delgado:** Exactly. And, second thing. We're looking at an acquisition. Smaller carrier, about two hundred trucks, Midwest. Can't say more. But if it happens, they're on a different TMS entirely, and we'd need to fold them into whatever we build. Probably mid-next year.

**[00:30:12] Maya Okafor:** Okay. That's important for the architecture. Thanks for telling us.

**[00:30:19] Dev Patel:** That actually argues for an API-first approach even more. Their system could sit behind the same interfaces during the transition.

**[00:30:30] Marcus Delgado:** That's what I was hoping you'd say. Okay. I'll let you go. Talk soon.

**[00:30:36] Maya Okafor:** Thanks Marcus. Talk soon.

*[Meeting ended at 00:30:41]*
