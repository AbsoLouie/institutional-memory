# Discovery Call: Ironbridge Freight x Scope Creepers

- **Category:** sales-discovery
- **Date:** 2026-09-03
- **Duration:** 22 min
- **Platform:** Zoom
- **Call type:** Discovery call 1 of 3 (prospect)

## Attendees

| Name | Company | Role |
|---|---|---|
| Maya Okafor | Scope Creepers | Partner / Account Executive |
| Marcus Delgado | Ironbridge Freight | Chief Technology Officer |

---

## Transcript

**[00:00:05] Marcus Delgado:** Hey, there you are. Maya, right? Sorry, I was on another call that ran over.

**[00:00:12] Maya Okafor:** No problem at all. Hi Marcus, thanks for making the time. Is that a truck model behind you?

**[00:00:20] Marcus Delgado:** Ha, yes. That's a 1979 Kenworth W900. My dad drove one just like it. Ironbridge started with four of those. Now we're at about eleven hundred tractors, so, things have changed a bit.

**[00:00:41] Maya Okafor:** That's a great story. Okay, so, this is meant to be pretty informal. You replied to our note about legacy modernization, and I'd love to just hear what's going on. I'm not going to pitch you anything today. Does that work?

**[00:01:01] Marcus Delgado:** That works. Honestly, I almost didn't reply. I get, I don't know, ten of those emails a week. But the subject line said "the system only one person understands" and I laughed out loud, so here we are.

**[00:01:23] Maya Okafor:** Ha. That one gets a lot of replies. So what's the system?

**[00:01:29] Marcus Delgado:** So we have a dispatch system. It's homegrown. It's old. It runs basically everything on the operations side. Load assignment, dispatch, a bunch of the stuff that feeds billing. And it's, how do I put this. It's old, and there's one guy who really understands it.

**[00:01:58] Maya Okafor:** How old are we talking?

**[00:02:01] Marcus Delgado:** Parts of it are older than some of my developers. I'd have to get you the exact breakdown. There's some VB in there, there's some .NET from later, there's a lot of SQL. I'm the CTO, I should know this cold, but honestly the guy who knows it is the guy who knows it.

**[00:02:29] Maya Okafor:** And that's one person?

**[00:02:32] Marcus Delgado:** One person. Gary. He's been here forever, he's fantastic, and if you ask him why something works the way it does he'll usually know. Nobody else will. There was another guy who knew some of it and he left years ago.

**[00:02:54] Maya Okafor:** Is any of it documented?

**[00:02:58] Marcus Delgado:** Ha. There's a binder.

**[00:03:01] Maya Okafor:** A binder.

**[00:03:04] Marcus Delgado:** A physical binder. I've seen it. I wouldn't trust it.

**[00:03:10] Maya Okafor:** Okay. So when you say it runs everything, how many people are in it day to day?

**[00:03:18] Marcus Delgado:** Dispatchers, planners, billing, a few others. A couple hundred people. Across, we have four terminals.

**[00:03:30] Maya Okafor:** And what's the pain, practically? Like, what actually goes wrong?

**[00:03:36] Marcus Delgado:** Um. It's more of a, it's a general feeling of dread, honestly. It goes down sometimes. When it goes down, dispatchers are on the phone with drivers manually and it's chaos. When the business asks for something new, the answer is usually "we can't do that in the system" or "Gary would have to look at it." And Gary's always busy, because Gary's also the one who fixes it when it breaks.

**[00:04:12] Maya Okafor:** So he's the bottleneck on both new work and keeping the lights on.

**[00:04:18] Marcus Delgado:** Yes. That's a good way to say it. I'm going to steal that.

**[00:04:24] Maya Okafor:** Please do. How often does it go down?

**[00:04:29] Marcus Delgado:** I'd have to pull the numbers. Often enough that I notice. Often enough that the ops VP has my cell.

**[00:04:38] Maya Okafor:** Ha. Okay. Have you tried to do anything about it before?

**[00:04:44] Marcus Delgado:** We did, yeah. We tried a rewrite a few years ago with a big integrator. It did not go well. I'd rather get into that another time, if that's okay. It's a long story and I'm still a little sore about it.

**[00:05:04] Maya Okafor:** Of course. We can come back to it. That's actually really common, for what it's worth. A lot of the folks we work with have one of those in their past.

**[00:05:17] Marcus Delgado:** That makes me feel slightly better.

**[00:05:20] Maya Okafor:** Can I tell you very briefly how we tend to think about it, just so you have context on who we are?

**[00:05:28] Marcus Delgado:** Sure.

**[00:05:30] Maya Okafor:** So Scope Creepers is a small AI consultancy. A lot of our work is exactly this, old systems that a few people understand. The short version is, we don't start by rewriting. We start by using AI to read the whole codebase and build a map of what it actually does. Then the person who knows it, your Gary, reviews and corrects that, instead of having to explain everything from memory.

**[00:06:05] Marcus Delgado:** Huh. Okay. That's, that's different.

**[00:06:10] Maya Okafor:** It tends to be a lot less painful for the Garys of the world. But I'll let our solutions engineer, Dev, get into the details if we get there. He's much better at it than I am.

**[00:06:23] Marcus Delgado:** Okay. Yeah, I'd want Gary to hear that. He'd be skeptical, but he'd want to hear it.

**[00:06:31] Maya Okafor:** Let me ask a few boring questions. Where does the system live? Is it on-prem?

**[00:06:37] Marcus Delgado:** On-prem. Citrix for the remote terminals. We're moving more stuff to Azure, but this is not one of those things yet.

**[00:06:48] Maya Okafor:** And your team? How big is IT?

**[00:06:53] Marcus Delgado:** About thirty people. Development's a handful. Most of them are maintaining integrations, EDI stuff, that kind of thing. Then infrastructure and help desk.

**[00:07:07] Maya Okafor:** EDI with customers?

**[00:07:11] Marcus Delgado:** Customers, brokers, a bunch of trading partners. That's its own thing. Every time sales signs a new shipper, my EDI people disappear for a month building maps. I joke that sales should have to pay my team a commission.

**[00:07:31] Maya Okafor:** Ha. That's a fun one. Okay. I'm making a note.

**[00:07:36] Marcus Delgado:** Make a big note.

**[00:07:40] Maya Okafor:** So, the question I always ask. Why now? You've had this system for a long time. What's making you look at it this year?

**[00:07:52] Marcus Delgado:** Um. Honestly, a few things, and I'm still, I'm still pulling them together. Part of it is just, we can't keep doing it this way. Part of it is, there are some customer things coming that I think the system won't handle. I don't want to get too far into those yet because I'm not sure I've got the details right.

**[00:08:19] Maya Okafor:** That's fine. Is there a date you're working toward? Something where, if it's not done by then, it really hurts?

**[00:08:29] Marcus Delgado:** Probably? I don't, I don't have a hard date I can give you right now. Sooner is better. I'd want to talk to a couple people internally before I say a date out loud, because if I say it on a call, it becomes the date.

**[00:08:49] Maya Okafor:** Ha. Fair enough. I won't hold you to anything. Next time, maybe.

**[00:08:55] Marcus Delgado:** Next time. Yeah.

**[00:08:59] Maya Okafor:** What about budget? Is there money set aside for this kind of thing, or would this be a, go find the money conversation?

**[00:09:08] Marcus Delgado:** No, there's money. That's actually part of why I took the call. We have about seven hundred thousand earmarked for modernization this fiscal year.

**[00:09:22] Maya Okafor:** Seven hundred thousand. Okay. And is that specifically for the dispatch system, or modernization more broadly?

**[00:09:30] Marcus Delgado:** Modernization broadly, on paper. In practice, the dispatch system is the elephant. Everybody knows that's where it should go. But there's always other stuff that wants a piece of it.

**[00:09:47] Maya Okafor:** Sure. That's helpful. And just so I understand, is that roughly the number, or is there a range?

**[00:09:55] Marcus Delgado:** It's roughly the number. Seven hundred, give or take. I'd have to check exactly what's left of it.

**[00:10:04] Maya Okafor:** Got it. And who would sign off on something like this? Is that you, or does it go further up?

**[00:10:12] Marcus Delgado:** Ooh. Good question. Honestly? I'd have to check who signs off on that. After the last project, things got, the process got a little more involved. I don't want to tell you it's me and then find out it isn't.

**[00:10:32] Maya Okafor:** That's totally fair. Would it help if I put together something you could share internally, whenever you figure out who that is?

**[00:10:41] Marcus Delgado:** Maybe. Let me figure out the who first. I don't want to send something around before I know where it should go.

**[00:10:50] Maya Okafor:** Makes sense. We'll keep it light for now.

**[00:10:55] Marcus Delgado:** Appreciate it.

**[00:10:58] Maya Okafor:** Can I go back to the system for a second? You said Gary's busy because he's also fixing things. What does that look like week to week?

**[00:11:08] Marcus Delgado:** Something breaks, basically every week. Sometimes it's small. A load won't save, a report's wrong, the pay calculation for a driver looks off. And it goes to Gary. And Gary's good, but he's one guy. So if two things break, one of them waits.

**[00:11:34] Maya Okafor:** The pay calculation is in the dispatch system too?

**[00:11:37] Marcus Delgado:** Driver pay, yeah. That's the scary part, honestly. That's the part where if it's wrong, drivers notice immediately, and drivers have a lot of options. They'll just leave.

**[00:11:53] Maya Okafor:** Right. Okay, that's important. That's the kind of thing where you'd want to be very careful about any change.

**[00:12:01] Marcus Delgado:** Very careful. That's where the last project fell apart, actually. But, again, another time.

**[00:12:10] Maya Okafor:** Noted. I won't push. Can I ask, what do customers see? Like, is any of this visible to shippers?

**[00:12:19] Marcus Delgado:** Not directly. They see it indirectly. They call us. We have a customer service team and I think a huge chunk of their day is "where's my truck" calls. Shippers calling to ask where their load is, because we can't really give them that any other way.

**[00:12:42] Maya Okafor:** How big is that team?

**[00:12:46] Marcus Delgado:** I don't know exactly. More than it should be. I'd guess they field a couple thousand calls a week? I'd have to check. It's not my department, but every time I walk past them they're on the phone.

**[00:13:02] Maya Okafor:** That's interesting. That's one of those things that tends to go away once the underlying data is accessible.

**[00:13:11] Marcus Delgado:** That's what I keep saying. If the system could just, tell people where things are, half those calls disappear.

**[00:13:20] Maya Okafor:** Okay. Let me ask what you'd want out of a conversation with us. If we did this right, what would you want to walk away with?

**[00:13:31] Marcus Delgado:** Um. Honestly, at this point, I want somebody to tell me it's not hopeless. I want to understand what's actually in there. Before I spend a dollar on rebuilding anything, I want to know what I've got.

**[00:13:50] Maya Okafor:** That's actually exactly where we'd want to start too.

**[00:13:54] Marcus Delgado:** Good. Because the last group wanted to start by designing screens.

**[00:14:01] Maya Okafor:** Ha. Yeah. We'd skip the screens for a while.

**[00:14:06] Marcus Delgado:** Good.

**[00:14:08] Maya Okafor:** Are you talking to anyone else about this?

**[00:14:13] Marcus Delgado:** Kind of. Our Microsoft partner's been pitching me stuff. There's been a couple of offshore firms in my inbox. I haven't really engaged. I wanted to understand the problem better first.

**[00:14:30] Maya Okafor:** That's smart. Honestly, that's the right order.

**[00:14:35] Marcus Delgado:** Hang on one second, sorry, I have to answer this.

*[00:14:38 – 00:15:34, Marcus Delgado muted]*

**[00:15:35] Marcus Delgado:** Sorry. That was, of course, a dispatcher issue. Something froze at one of the terminals. It's fine, it's handled. This is the kind of thing I'm talking about.

**[00:15:49] Maya Okafor:** Ha. Perfect timing, in a sad way.

**[00:15:53] Marcus Delgado:** In a very sad way.

**[00:15:55] Maya Okafor:** Who handled it, if Gary's the only one?

**[00:15:59] Marcus Delgado:** Someone restarted the session. That's our first fix for everything. If that doesn't work, it goes to Gary.

**[00:16:08] Maya Okafor:** Got it. So I'm hearing three things. One, the system is old and one person understands it. Two, it breaks often enough that it's pulling that one person away from anything new. And three, the business is asking for things it can't do, which you're still pulling together.

**[00:16:32] Marcus Delgado:** That's it. That's a better summary than I'd have given.

**[00:16:37] Maya Okafor:** And there's roughly seven hundred thousand earmarked this fiscal year. Timeline and who signs off, TBD.

**[00:16:46] Marcus Delgado:** TBD. Yes. Don't write that in pen.

**[00:16:50] Maya Okafor:** Pencil. Promise.

**[00:16:53] Marcus Delgado:** Ha.

**[00:16:55] Maya Okafor:** Is there anything about how Ironbridge works that I should know before we get further? Culture-wise, how decisions get made?

**[00:17:06] Marcus Delgado:** Um. We're a family company, kind of. Third generation of leadership. People have been here a long time. We're careful. After the last project, people are extra careful. So, slow and proof-heavy is better than fast and flashy.

**[00:17:29] Maya Okafor:** That's good to know. That fits how we work.

**[00:17:34] Marcus Delgado:** And Gary. Gary needs to feel like he's part of it. The last group kind of steamrolled him.

**[00:17:42] Maya Okafor:** That's important. Would Gary be up for joining next time?

**[00:17:48] Marcus Delgado:** I think so. If I tell him it's not another workshop.

**[00:17:54] Maya Okafor:** It's not another workshop. I'd bring Dev, our solutions engineer, and he'd mostly want to ask Gary questions about how the thing is built. Gary would be the expert in the room.

**[00:18:10] Marcus Delgado:** He'd like that. Honestly, he'd like that a lot.

**[00:18:14] Maya Okafor:** Okay. Anything else on your mind? Even outside of the dispatch system?

**[00:18:22] Marcus Delgado:** Oh, I have a list. But I'll save it. If I start, we'll be here all day.

**[00:18:29] Maya Okafor:** Ha. Save it for next time, then.

**[00:18:32] Marcus Delgado:** Deal.

**[00:18:35] Maya Okafor:** Let me ask one more about the numbers, actually. When you said seven hundred, is that money that rolls over if you don't use it, or does it go away at year end?

**[00:18:47] Marcus Delgado:** That's, honestly, a finance question. I know the number. I don't know all the rules around it. Let me find out.

**[00:18:56] Maya Okafor:** Totally fine. I'll put it on the list.

**[00:19:01] Marcus Delgado:** My list or your list?

**[00:19:04] Maya Okafor:** My list. You just tell me when you know.

**[00:19:07] Marcus Delgado:** Ha. Okay.

**[00:19:10] Maya Okafor:** So, next steps. Here's what I'd suggest. One, let's get a second call on the books, maybe in about four weeks, with Gary and Dev. Dev would want to understand the architecture at a high level. No code, nothing sensitive. Just a conversation.

**[00:19:31] Marcus Delgado:** That works. Early October-ish?

**[00:19:35] Maya Okafor:** Early October's great. Two, I'll send you a short case study from a similar project. It was an insurance company, a policy admin system with the same kind of problem. One person who knew it, a failed rewrite in their history.

**[00:19:54] Marcus Delgado:** Oh, I'd love that. Honestly, I'd forward that to Gary tonight.

**[00:20:00] Maya Okafor:** Perfect. And three, on your side, whenever you have it, any rough numbers on the outages, and whatever you're comfortable sharing about the customer things you mentioned. No pressure on timing.

**[00:20:17] Marcus Delgado:** I can probably get you outage numbers. The customer stuff, let me see what I can share.

**[00:20:24] Maya Okafor:** That's great. And if you figure out who signs off, that'd be helpful too, but again, no rush.

**[00:20:32] Marcus Delgado:** Yeah. I'll ask around.

**[00:20:36] Maya Okafor:** Okay. Anything you need from me before then?

**[00:20:40] Marcus Delgado:** Um. Maybe just, can you send me a one-paragraph description of who you are? Something I can paste into an email to Gary so he knows it's not, you know, another big integrator.

**[00:20:55] Maya Okafor:** Absolutely. I'll send that today along with the case study.

**[00:21:01] Marcus Delgado:** Great.

**[00:21:04] Maya Okafor:** And Marcus, I'll send a calendar hold for the week of September twenty-eighth. If that doesn't work for Gary, just move it.

**[00:21:13] Marcus Delgado:** Sounds good. Gary's calendar is basically "whenever DART isn't on fire."

**[00:21:20] Maya Okafor:** DART?

**[00:21:23] Marcus Delgado:** Oh, sorry, that's the system. Dispatch And Routing Tool. Gary's predecessor named it.

**[00:21:31] Maya Okafor:** Ha. I love it. Okay, DART. Got it.

**[00:21:36] Marcus Delgado:** It's a good name. It's a bad system. Well, it's not a bad system. It's an old system.

**[00:21:44] Maya Okafor:** That's usually the more accurate way to say it.

**[00:21:48] Marcus Delgado:** Ha. Okay. Thanks Maya. This was more useful than I expected, honestly.

**[00:21:55] Maya Okafor:** I'll take that. Thanks Marcus. Talk soon.

**[00:22:00] Marcus Delgado:** Talk soon.

*[Meeting ended at 00:22:04]*
