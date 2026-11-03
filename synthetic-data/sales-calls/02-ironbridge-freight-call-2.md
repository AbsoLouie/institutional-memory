# Discovery Call: Ironbridge Freight x Scope Creepers

- **Category:** sales-discovery
- **Date:** 2026-10-01
- **Duration:** 24 min
- **Platform:** Zoom
- **Call type:** Discovery call 2 of 3 (prospect)

## Attendees

| Name | Company | Role |
|---|---|---|
| Maya Okafor | Scope Creepers | Partner / Account Executive |
| Dev Patel | Scope Creepers | Principal Solutions Engineer |
| Marcus Delgado | Ironbridge Freight | Chief Technology Officer |
| Gary Lindqvist | Ironbridge Freight | Lead Developer, Dispatch Systems |

---

## Transcript

**[00:00:04] Marcus Delgado:** Hey, hi. Okay, we're both here. Gary's in my office, so we're sharing a camera.

**[00:00:13] Maya Okafor:** Hi Marcus. And hi Gary, nice to finally meet you. This is Dev.

**[00:00:20] Dev Patel:** Hey both. Good to meet you, Gary. I've heard a lot about DART.

**[00:00:26] Gary Lindqvist:** Uh oh. All bad, I assume.

**[00:00:30] Dev Patel:** Mostly that you're the only one who understands it.

**[00:00:36] Gary Lindqvist:** That part's true.

**[00:00:38] Marcus Delgado:** So, Maya, I forwarded that insurance case study to Gary at like eleven at night with four exclamation points.

**[00:00:48] Gary Lindqvist:** He did. I was asleep.

**[00:00:51] Maya Okafor:** Ha. I'm glad it landed. Okay, so last time, Marcus and I kept it high level. Old system, one person who really knows it, it breaks, and there's some money for modernization. And we left a couple of things open. Timing, and some of the customer pressure you mentioned. So today I'd love for Dev to get a real picture of DART from Gary, and then come back to the why-now. Sound good?

**[00:01:26] Marcus Delgado:** Perfect. And I did my homework, so I have answers this time.

**[00:01:32] Maya Okafor:** Love that. Dev, take it away.

**[00:01:36] Dev Patel:** Gary, give me the tour. Whatever level makes sense.

**[00:01:42] Gary Lindqvist:** Okay. So DART does load tendering, driver assignment, dispatch, check calls. It calculates driver pay. It does some of the billing feeds. The front end is VB6. Yes, still. Some of the newer modules are .NET Framework 3.5 WinForms. SQL Server back end. About nineteen hundred stored procedures. Some of them are dead. I don't know which ones.

**[00:02:20] Dev Patel:** How much code, roughly?

**[00:02:24] Gary Lindqvist:** Somewhere around six hundred thousand lines across everything. The VB6 piece is maybe two hundred and fifty thousand.

**[00:02:34] Dev Patel:** And where does the business logic live? Stored procs, or the VB6?

**[00:02:40] Gary Lindqvist:** Yes.

**[00:02:42] Dev Patel:** Ha. Both. Okay.

**[00:02:45] Gary Lindqvist:** Both. And some of it lives in button click handlers. There's a lot of global variables. I'll be honest, I've seen tools that claim to convert VB6, and they produce garbage.

**[00:03:01] Dev Patel:** Totally fair. We don't run a converter. The model reads the code the way a senior engineer would and writes up what it actually does, in plain English. You'd review that, rather than explain it from memory. And everything gets validated with tests from production data. Where it's wrong, the tests catch it.

**[00:03:31] Gary Lindqvist:** Huh. Okay. That's different from the last group. They put me in two-hour workshops and asked me to explain thirty years of logic out loud.

**[00:03:44] Dev Patel:** Yeah, that doesn't work. Nobody can do that. Where's the source? What's it in?

**[00:03:51] Gary Lindqvist:** TFS. Team Foundation Server. The old one.

**[00:03:56] Dev Patel:** That's fine. We can work with that or mirror it to Git.

**[00:04:02] Maya Okafor:** Marcus, how many people are in DART day to day? Last time you said a couple hundred.

**[00:04:08] Marcus Delgado:** I got the real number. About a hundred and forty dispatchers and planners across the four terminals, plus billing, safety, driver managers. Call it two hundred and twenty users. On-prem, Citrix for the remote terminals.

**[00:04:29] Gary Lindqvist:** The Citrix part is held together with tape.

**[00:04:33] Maya Okafor:** And you said you'd pull outage numbers.

**[00:04:37] Marcus Delgado:** I did. We had nine meaningful outages last year. Ops estimates an hour of DART down costs us about forty thousand in delays and missed appointments. Some of those were three or four hours.

**[00:04:57] Dev Patel:** So, call it several hundred thousand a year just in downtime.

**[00:05:02] Marcus Delgado:** Easily. And that doesn't count the stuff we can't do.

**[00:05:08] Maya Okafor:** And hiring? Can you get people who know this stack?

**[00:05:13] Marcus Delgado:** No. Nobody wants to write VB6. We posted a role last year. Three applicants. Two of them were over sixty-five.

**[00:05:25] Maya Okafor:** Oh no.

**[00:05:26] Gary Lindqvist:** One of them I actually knew. He's older than me.

**[00:05:31] Dev Patel:** Gary, how much of your week goes to keeping it running versus new work?

**[00:05:38] Gary Lindqvist:** Something breaks every week. Last week a driver's pay came out negative because of a layover rule. The week before, a load wouldn't save because somebody typed an apostrophe in a city name.

**[00:05:56] Dev Patel:** Oh, the classic.

**[00:05:59] Gary Lindqvist:** I'd say seventy percent keeping it running. Maybe more.

**[00:06:04] Dev Patel:** And driver pay, how complicated is that?

**[00:06:10] Gary Lindqvist:** Very. There are union rules, owner-operator rules, detention, layover, stop pay, hazmat, team splits. There are special deals with specific drivers from 2008 that nobody remembers agreeing to.

**[00:06:31] Dev Patel:** Ha. Okay. Honestly, that's exactly what production-data tests catch. The weird special deals show up as mismatches and then we go figure out why.

**[00:06:44] Gary Lindqvist:** That makes sense. Actually, detention's a whole thing on the billing side too. Half of what billing does is arguing with shippers about detention. Was the truck really there four hours. The timestamps in DART are, let's say, aspirational.

**[00:07:05] Maya Okafor:** Ha. Aspirational.

**[00:07:08] Marcus Delgado:** That's generous.

**[00:07:10] Gary Lindqvist:** And then the same billing folks are matching proof of delivery to invoices by hand. Drivers send PODs as photos from their phones. Blurry, sideways, half a thumb in the frame. There's like twelve people who do that all day.

**[00:07:31] Dev Patel:** Twelve people?

**[00:07:34] Gary Lindqvist:** Twelve. It's not my problem, technically, but they call me when DART doesn't show the load.

**[00:07:42] Maya Okafor:** Noted. Okay, Marcus. You said you did your homework. Let's come back to the why-now. Last time you said there were customer things coming and you wanted to get the details right.

**[00:07:58] Marcus Delgado:** Yes. So, there are three things, and they kind of stack on top of each other. One. Our biggest shipper, a big-box retailer, is requiring API-based tendering. They want to send us loads through an API and get real-time status back. If we can't do it, we lose preferred carrier status.

**[00:08:27] Maya Okafor:** How big is that customer?

**[00:08:30] Marcus Delgado:** About eighteen percent of revenue.

**[00:08:33] Maya Okafor:** Okay. That's real.

**[00:08:36] Marcus Delgado:** And the deadline is Q3 2027. I confirmed it with our account manager last week. It's in writing now.

**[00:08:45] Dev Patel:** Do you know their certification process? Is there a testing window?

**[00:08:51] Marcus Delgado:** They give you about ninety days of testing before go-live. So for Q3, I'd want to be in test by, call it, April.

**[00:09:03] Dev Patel:** Okay. Gary, where does tendering live? Is it in the VB6?

**[00:09:09] Gary Lindqvist:** Tendering's actually one of the cleaner modules. That was the .NET rewrite, from like 2014.

**[00:09:17] Dev Patel:** Oh, that's good news. That'd probably be the first thing you'd carve off.

**[00:09:22] Marcus Delgado:** That's what I was hoping. Okay, two. And Gary knows I'm going to say this.

**[00:09:29] Gary Lindqvist:** Here it comes.

**[00:09:32] Marcus Delgado:** Gary's been here twenty-three years, and Gary's told us he's retiring at the end of 2027.

**[00:09:39] Gary Lindqvist:** It's true. My wife has a boat picked out.

**[00:09:45] Maya Okafor:** Congratulations, Gary. Honestly.

**[00:09:47] Gary Lindqvist:** Thank you. I'd like to leave it in better shape than I found it, though. I don't want to be the guy they call from the boat.

**[00:09:57] Marcus Delgado:** And I say this with total respect, Gary is the only human being alive who understands how driver pay is calculated in DART. There was one other guy, Ray, who knew some of it. He left in 2019.

**[00:10:14] Dev Patel:** And the documentation is the binder?

**[00:10:18] Gary Lindqvist:** Marcus told you about the binder.

**[00:10:20] Dev Patel:** He did.

**[00:10:22] Gary Lindqvist:** It's from 2011. It's maybe forty percent right.

**[00:10:28] Dev Patel:** So you've got roughly fifteen months to get what's in Gary's head into something durable, ideally with Gary reviewing, not authoring.

**[00:10:39] Marcus Delgado:** Exactly. And three, the money. Maya, you asked last time if the budget rolls over. It does not. It has to be committed by December, or I lose it.

**[00:10:53] Maya Okafor:** December this year?

**[00:10:56] Marcus Delgado:** This December. Use it or lose it. And next year, I've asked for a lot more, but whether I get it depends on whether I can show progress.

**[00:11:09] Maya Okafor:** Okay, so, stacking those. Retailer API in test by April, live by Q3 2027. Gary out at the end of 2027. And this year's budget committed by December.

**[00:11:25] Marcus Delgado:** That's the picture. That's why I'm pushing.

**[00:11:29] Maya Okafor:** And on the budget, last time you said about seven hundred thousand earmarked for modernization. Is that still right?

**[00:11:38] Marcus Delgado:** So, I need to correct that, actually. It's seven hundred, but a hundred and fifty of it is already spoken for. We're doing a telematics project, new ELDs and in-cab tablets across the fleet, and finance carved that out of the same bucket. I didn't realize it had already been committed.

**[00:12:03] Maya Okafor:** Okay. So really about five-fifty available?

**[00:12:07] Marcus Delgado:** About five-fifty. Sorry, I told you seven last time.

**[00:12:13] Maya Okafor:** No, that's helpful. Better now than later. So five-fifty, committed by December.

**[00:12:21] Marcus Delgado:** Right.

**[00:12:22] Dev Patel:** The telematics, is that going to feed DART?

**[00:12:27] Gary Lindqvist:** It's supposed to. Nobody's told me how yet.

**[00:12:32] Dev Patel:** Ha. Okay, that's worth knowing. That's real-time location data, which is basically what the retailer wants for status.

**[00:12:43] Marcus Delgado:** Oh. Huh. That's a good point.

**[00:12:47] Gary Lindqvist:** And it's what customer service wants. They get, what, two thousand where's-my-load calls a week?

**[00:12:55] Marcus Delgado:** About that. I checked. It's actually a little over two thousand.

**[00:13:00] Gary Lindqvist:** If the ETA API exists, those calls go away.

**[00:13:05] Maya Okafor:** That's a good one to remember. Marcus, I asked last time who signs off on this. Did you get a chance to figure that out?

**[00:13:16] Marcus Delgado:** Um. Partly. Honestly, I assumed it'd be my call, it's my budget line. But after the 2022 thing, finance got more involved in anything big. I've got a meeting with them next week to confirm. I don't want to tell you the wrong thing twice in one call.

**[00:13:41] Maya Okafor:** Ha. That's fair. Would it help if we came prepared for whoever that is next time?

**[00:13:49] Marcus Delgado:** Yes. If it's finance, they're going to ask about 2022.

**[00:13:56] Maya Okafor:** You mentioned a rewrite last time but didn't want to get into it. Are you up for it now? Even the short version?

**[00:14:05] Marcus Delgado:** Short version. We hired a big systems integrator, not going to name them, to do a full rewrite. Ground up, cloud native, the whole pitch. Eighteen-month plan. They spent fourteen months gathering requirements and building a new UI, and when they tried to replicate driver pay, the numbers didn't match, and they couldn't figure out why.

**[00:14:36] Gary Lindqvist:** And they never really asked me. Well, the workshops.

**[00:14:42] Marcus Delgado:** We pulled the plug at fourteen months. We got a nice UI mockup out of it.

**[00:14:48] Maya Okafor:** I'm sorry. That's a rough one.

**[00:14:52] Dev Patel:** That's actually the thing we'd do differently in the first week. We wouldn't touch the UI. We'd map the code, write specs for driver pay, and build tests from, say, two years of real pay calculations. Old logic and new logic have to match to the penny. That's how you know you're done.

**[00:15:19] Gary Lindqvist:** That's exactly what they didn't do.

**[00:15:23] Dev Patel:** And then you don't replace DART. You carve off one capability at a time, put an API in front of it, and DART keeps running. Tendering first, because of the retailer.

**[00:15:37] Marcus Delgado:** See, Gary? I told you.

**[00:15:40] Gary Lindqvist:** I'm cautiously optimistic.

**[00:15:44] Maya Okafor:** Gary, what would worry you most?

**[00:15:48] Gary Lindqvist:** Time. I still have a day job. If I'm reviewing specs all day, who's on call?

**[00:15:56] Marcus Delgado:** That's real. I'd like to say fifty percent of his time.

**[00:16:01] Gary Lindqvist:** You'd like to say.

**[00:16:04] Marcus Delgado:** Realistically twenty-five, maybe thirty. Unless we backfill some of the on-call.

**[00:16:12] Dev Patel:** One thing that helps there. Once the codebase is indexed, a junior dev can ask, why is this load showing negative mileage, and get pointed at the right procedure. That takes some of the on-call off Gary.

**[00:16:30] Gary Lindqvist:** Okay, that I would pay for personally.

**[00:16:34] Marcus Delgado:** Ha.

**[00:16:37] Dev Patel:** Who else would work with us on your side?

**[00:16:41] Marcus Delgado:** Development's eight, including Gary. Two of them are decent .NET Core developers, newer hires. Target is Azure, .NET 8 or whatever's current, C#, since that's what my newer folks know.

**[00:16:59] Dev Patel:** Makes sense. Gary, can I ask, is there anything about how DART's deployed that'd make it hard to stand up an API next to it?

**[00:17:10] Gary Lindqvist:** Not really. The database is the database. If you can read the tables, you can do most of it. Writing back is the scary part.

**[00:17:21] Dev Patel:** Right. We'd start read-only where we can.

**[00:17:25] Marcus Delgado:** Oh, and, this is, I can't say much. There's a chance we add some trucks next year. A different fleet, on their own system. If that happens, whatever we build needs to be able to take them in. That's all I can say.

**[00:17:48] Dev Patel:** Okay. That argues for API-first even more. Their system could sit behind the same interfaces for a while.

**[00:17:57] Marcus Delgado:** That's what I was hoping you'd say.

**[00:18:01] Maya Okafor:** I'll keep that one quiet. Let me check the time. We've got about ten minutes. Dev, what would you need to firm up an approach?

**[00:18:12] Dev Patel:** Honestly, I'd want to see some code. Even a portion. Under NDA. Gary, would that be possible?

**[00:18:21] Gary Lindqvist:** Marcus?

**[00:18:24] Marcus Delgado:** I'd want to check with legal. But yes, I want to do that.

**[00:18:29] Gary Lindqvist:** Before we do, can I ask. Does the code go to an AI company? Like, does Anthropic train on our code? There's stuff about specific drivers in there. Comments with names.

**[00:18:45] Dev Patel:** Good question. On the commercial API, Anthropic doesn't train on your data. And we can run everything through your Azure tenant if you'd prefer. I'll send that in writing so your legal folks have it.

**[00:19:02] Gary Lindqvist:** Thanks. And honestly, I'd like to see it do something non-trivial before I get excited. Like, show me it reading real VB6.

**[00:19:14] Dev Patel:** I'll put together a sample from an open-source VB6 project, so it doesn't need your code. Ugly button-click logic and all.

**[00:19:24] Gary Lindqvist:** Okay. That would help.

**[00:19:28] Maya Okafor:** Marcus, anything else on your list? Last time you said you had one.

**[00:19:35] Marcus Delgado:** Oh, I have a long list. But I'll keep my promise and stay on DART. Mostly.

**[00:19:43] Maya Okafor:** Ha. Mostly.

**[00:19:45] Marcus Delgado:** Mostly.

**[00:19:48] Maya Okafor:** Okay. Let me play it back. DART is about six hundred thousand lines, VB6 and .NET 3.5 on SQL Server with nineteen hundred stored procedures, two hundred and twenty users. Nine outages last year at about forty thousand an hour. Gary spends seventy-plus percent of his time keeping it running.

**[00:20:14] Gary Lindqvist:** Seventy on a good week.

**[00:20:17] Maya Okafor:** On a good week. Timing is three things. The retailer API, eighteen percent of revenue, in test by April and live by Q3 2027. Gary retiring at the end of 2027. And this year's budget committed by December. Budget is seven hundred, minus a hundred and fifty for telematics, so about five-fifty available. Who signs off, still to be confirmed.

**[00:20:49] Marcus Delgado:** That's exactly it.

**[00:20:51] Maya Okafor:** Okay. So, next steps. One, Dev sends the VB6 sample and a written answer on data handling, so Gary and your legal team have it. Two, we send our NDA so we can get to the code when you're ready. Three, Marcus, you confirm who signs off, and if it makes sense, we'd love to have that person on the next call.

**[00:21:20] Marcus Delgado:** I'll know by next week. And yes, if it's who I think it is, I'll bring them.

**[00:21:27] Maya Okafor:** Perfect. And four, I'll put together a rough outline of what a first phase could look like against those dates. Not a proposal. Just a shape.

**[00:21:40] Marcus Delgado:** That would help a lot. If I'm going to walk into finance, I want something to point at.

**[00:21:48] Maya Okafor:** I'll have it to you by end of next week.

**[00:21:52] Dev Patel:** And Gary, if you're open to it, I'd love thirty minutes just with you sometime, no slides. Just to understand where the bodies are buried.

**[00:22:04] Gary Lindqvist:** Ha. There are a lot of bodies. Sure.

**[00:22:08] Marcus Delgado:** Hang on, sorry, Gary's phone.

*[00:22:12 – 00:22:54, Marcus Delgado muted]*

**[00:22:55] Marcus Delgado:** Okay, sorry. A terminal had a Citrix hiccup. Gary's going to go look.

**[00:23:02] Gary Lindqvist:** Of course it did. Nice to meet you both.

**[00:23:06] Dev Patel:** Good luck, Gary.

*[Gary Lindqvist left the meeting at 00:23:10]*

**[00:23:13] Marcus Delgado:** That's the job. Okay. Maya, thanks. This was good. I feel like I have a story now.

**[00:23:22] Maya Okafor:** You do. We'll get you the pieces. Talk soon, Marcus.

**[00:23:27] Marcus Delgado:** Talk soon.

*[Meeting ended at 00:23:31]*
