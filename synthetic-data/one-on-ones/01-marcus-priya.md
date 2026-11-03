# 1:1 — Marcus Lindqvist / Priya Raman

- **Category:** one-on-one
- **Date:** Wednesday, October 7, 2026
- **Duration:** 31 minutes
- **Attendees:** Marcus Lindqvist (Engineering Manager), Priya Raman (Senior Engineer)
- **Company:** Scope Creepers
- **Current staffing:** Priya, tech lead in practice on the Northfold Mutual claims-summarization project (Claude-based RAG over adjuster notes)

---

**[00:00:10] Marcus Lindqvist:** Hey, can you hear me? My headphones did the thing where they connect to the laptop and the phone at the same time.

**[00:00:21] Priya Raman:** Yeah, I've got you. You sound fine. A little bit like you're in a tunnel, but fine.

**[00:00:31] Marcus Lindqvist:** That's just the vibe of my office. How was the long weekend? You went up to the cabin, right?

**[00:00:43] Priya Raman:** We did. My sister's kids were there, so "relaxing" is generous. But I got one morning of kayaking in before anyone woke up, and that was worth the drive. I didn't open Slack once, which I'm proud of.

**[00:01:14] Marcus Lindqvist:** Good. Honestly, that's great to hear. Okay, I've got a few things, and I want to save time at the end for the Staff conversation since we said we'd pick that back up. Anything you want to make sure we get to?

**[00:01:42] Priya Raman:** The Staff thing, yes. And I want to talk about Devon. Probably not in a fun way.

**[00:01:57] Marcus Lindqvist:** Okay, noted. Let's start with the follow-up from last time. Two weeks ago you said you'd try to get the retrieval re-ranking change on Northfold merged before their October 1st checkpoint. How did that land?

**[00:02:28] Priya Raman:** It landed. It went out on the 29th. Their claims ops lead, Renata, was really happy with it. The summaries stopped pulling in the irrelevant subrogation notes, which was the big complaint. Hallucinated payout amounts went from something like six percent of the eval set to under one.

**[00:03:10] Marcus Lindqvist:** That's a huge drop. And Renata actually emailed me about it, which clients almost never do unless something's on fire. She said, quote, "Priya's the reason we're renewing for Q1." So I want you to hear that clearly. The way you diagnosed the chunking problem, figured out it wasn't the prompt at all, it was the chunk boundaries splitting adjuster entries in half, that's the kind of thing nobody else on the team would've caught that fast.

**[00:04:12] Priya Raman:** Thanks. It was kind of a fun one, honestly.

**[00:04:19] Marcus Lindqvist:** It shows. Okay. So I want to move to something that's adjacent, and I'm going to be straightforward about it because I think you'd rather I be direct.

**[00:04:41] Priya Raman:** Uh-oh. Yes. Go.

**[00:04:48] Marcus Lindqvist:** Review turnaround. I pulled the numbers on the Northfold repo for September. Median time from PR opened to first review, when you're the requested reviewer, was a little over three days. When anyone else is the reviewer, it's under a day. And right now there are, I think, five PRs sitting with you as the only reviewer. The oldest one is Devon's PR 412, the citation-formatting change, and that's been open since September 24th.

**[00:05:55] Priya Raman:** Okay, but — sorry, I'm going to push back a little. The reason those are sitting is because they're not ready. Devon's 412 is a good example. The approach is wrong. It parses the model output with regexes after the fact instead of just using structured output with a citation schema. If I approve it, we're going to be ripping it out in a month.

**[00:06:45] Marcus Lindqvist:** That might be totally right on the technical side. I'm not arguing the regex thing.

**[00:06:57] Priya Raman:** And the other ones, I'm on them, I just — I get pulled into the Tallgrass escalations, and then it's Thursday.

**[00:07:13] Marcus Lindqvist:** Yeah. I hear that. Can I say the part that I think is actually the problem? Because it's not really the three days.

**[00:07:28] Priya Raman:** Sure.

**[00:07:32] Marcus Lindqvist:** On 412, what happened after you looked at it? Walk me through it.

**[00:07:44] Priya Raman:** I... okay. I pulled the branch, and I rewrote the citation piece to use tool-use structured output, and I pushed it to a branch called `priya/citations-v2` so he could see what I meant.

**[00:08:13] Marcus Lindqvist:** And did you leave review comments on his PR?

**[00:08:20] Priya Raman:** I left one comment that said "see my branch."

**[00:08:27] Marcus Lindqvist:** Right. So from Devon's side, he waited ten days, and then the feedback was a rewrite of his work with a one-line pointer. And I know that's not how you intended it. But I talked to him last week, and he said — and I'm paraphrasing — he doesn't really know what he did wrong, he just knows it wasn't what you'd have done.

**[00:09:17] Priya Raman:** That's... that's not fair, though. I've explained structured outputs to him at least twice. In standup, in Slack. At some point it's faster to just show him.

**[00:09:41] Marcus Lindqvist:** It is faster. This week. That's sort of my whole point.

**[00:09:50] Priya Raman:** *(pause)* Okay. I'm a little annoyed, I'm not going to lie.

**[00:10:00] Marcus Lindqvist:** That's fine. I'd rather you be annoyed with me in here than annoyed quietly.

**[00:10:09] Priya Raman:** It's just — I'm the one who gets the call when the summaries are wrong. Renata messages me directly. So when something's going in that I know is going to break, it feels irresponsible to let it through just so Devon feels coached.

**[00:10:43] Marcus Lindqvist:** Yeah. And that's a real tension. I don't want you to approve things you think are wrong. That's not the ask. The ask is that the way you say "this is wrong" teaches him how to get it right next time, instead of you doing it for him. Because right now, every hard thing on Northfold routes through you, and when you're out — like this weekend, which, again, good — nothing moves.

**[00:11:37] Priya Raman:** *(sighs)* Yeah. Friday, Devon was blocked on the eval regression and just... waited for me to get back.

**[00:11:54] Marcus Lindqvist:** Right. And that's not on you individually, that's partly a structure problem I've let happen. But it's going to be the thing that matters most for the Staff conversation, so I'd rather we look at it now.

**[00:12:23] Priya Raman:** Okay. I think I can hear that. Can I say the Devon part, though? Because the frustration isn't nothing.

**[00:12:37] Marcus Lindqvist:** Yes, please.

**[00:12:42] Priya Raman:** He doesn't test against the eval set before opening PRs. Like, ever. 412 dropped the citation-accuracy score from 0.91 to 0.84 on the golden set, and he didn't mention it in the description. I found it by running it myself. That's the part that makes me want to rewrite things. I can't trust what's in the PR.

**[00:13:25] Marcus Lindqvist:** That's a fair and specific concern, and I'm glad you said it with a number. That's something I can work on with him directly — running the eval suite and pasting the scores in the PR description should just be the norm, and it's not written down anywhere. That's on me.

**[00:14:00] Priya Raman:** It'd help a lot. Honestly, a PR template with an eval-results section would solve half of it.

**[00:14:12] Marcus Lindqvist:** Would you be up for writing that template? Not because I'm offloading it, but because you know what the eval output should look like better than anyone.

**[00:14:29] Priya Raman:** Yeah, I can do that. That's small.

**[00:14:36] Marcus Lindqvist:** Great. So, on Devon specifically: I'll talk to him about the eval expectation. I'd like you to do one thing differently, which is on 412 and anything else open of his, go back and leave real review comments. The "why," not just the "what." And if it's a design-level disagreement like structured output versus regex, get on a 20-minute call and pair on it, with him driving.

**[00:15:28] Priya Raman:** With him driving. Meaning I don't touch the keyboard.

**[00:15:35] Marcus Lindqvist:** Meaning you don't touch the keyboard. *(laughs)* I know.

**[00:15:43] Priya Raman:** That's going to be physically painful. But okay. Fine. I'll do 412 this week.

**[00:15:55] Marcus Lindqvist:** And can we do something about the queue? I'd like to try a rule for the next month: you're not the sole required reviewer on anything. Chidi or Jordan is first reviewer on routine stuff, and you only get pulled in for things touching retrieval or the eval harness. And if something's been with you for more than one business day, you either review it or you hand it off explicitly.

**[00:16:47] Priya Raman:** Jordan, though? They're eight months in.

**[00:16:54] Marcus Lindqvist:** Jordan built the prompt-eval harness we're all using now. They can review a config change. And if they miss something, the eval gate catches it. That's what the gate's for.

**[00:17:15] Priya Raman:** ...That's fair. Okay. Yeah. I'll try it.

**[00:17:27] Marcus Lindqvist:** Thank you. And I want to acknowledge, that was a hard few minutes, and you engaged with it instead of digging in. I appreciate that.

**[00:17:44] Priya Raman:** I dug in a little.

**[00:17:49] Marcus Lindqvist:** A little. Then you came out. That's the part that counts.

**[00:17:58] Priya Raman:** *(laughs)* Okay. Can I give you some feedback while we're doing hard things?

**[00:18:08] Marcus Lindqvist:** Please.

**[00:18:13] Priya Raman:** The Tallgrass escalations. You've volunteered me for three of them in the last month. The latest one, the one on the 30th, I found out about from the client's Slack channel. You'd tagged me in there before you'd asked me. And that's part of why my reviews are slow. I'm doing a second job.

**[00:18:55] Marcus Lindqvist:** Yeah. That's — you're right. I did that on the 30th because their support bot was looping on refund requests and I panicked a bit and reached for the person I knew would fix it. Which is the same thing I'm asking you not to do with Devon.

**[00:19:29] Priya Raman:** I wasn't going to say it, but yes.

**[00:19:36] Marcus Lindqvist:** *(laughs)* Fair. I'll stop doing that. Going forward, Tallgrass escalations go to their on-call rotation first, which is Sam and Chidi, and if I think it needs you I'll ask you directly, not tag you in front of the client. And if you're on Northfold that week, you can say no.

**[00:20:14] Priya Raman:** That'd help. Thank you.

**[00:20:19] Marcus Lindqvist:** Okay. Staff. Last time you asked me to find out what the actual criteria are, because you said it felt like a vibes-based promotion. I talked to Elena on the leadership team. The written rubric is getting updated, but the short version is: a Staff engineer at Scope Creepers is someone whose impact is measured across multiple projects, not one. Technical depth is the entry ticket, and you have that, no question. The thing they look at is leverage. Are other people better because you're here?

**[00:21:28] Priya Raman:** So, basically, everything we just talked about.

**[00:21:35] Marcus Lindqvist:** Basically everything we just talked about. Which is why I brought it up first. I genuinely think you can get there. I'd like to put you up for it in the spring cycle, but I need evidence of that leverage to write the packet, and right now the evidence mostly says "Priya solves the hardest problem herself."

**[00:22:13] Priya Raman:** Which is also valuable.

**[00:22:18] Marcus Lindqvist:** Hugely valuable. It's what makes you senior. It's not what makes you Staff.

**[00:22:30] Priya Raman:** Okay. What would the evidence look like? Concretely.

**[00:22:39] Marcus Lindqvist:** A few things. One: someone else on Northfold can own a meaningful chunk of the system without you. I'd suggest Devon owning citations end-to-end, since that's already his area. Two: something reusable that other teams pick up. You mentioned a while ago that the chunking fix could be generalized for other RAG projects —

**[00:23:24] Priya Raman:** The adjuster-note chunker, yeah. It'd work on basically any timestamped case-notes data. The Pellworth Health intake project has the same shape.

**[00:23:43] Marcus Lindqvist:** Right. So if you wrote that up as an internal pattern and ran a session on it for the other leads, that's cross-project impact. And three: mentoring that's visible. Not just Devon — you said you'd be open to pairing with Jordan, right?

**[00:24:14] Priya Raman:** I did say that. Jordan's actually great. They just never ask anything.

**[00:24:24] Marcus Lindqvist:** That's exactly what I'm working on with them. So if you set up a recurring pairing session, even an hour a week, that's useful for them and it's real evidence for you.

**[00:24:45] Priya Raman:** Okay. That's... a lot, but none of it is unreasonable. I think I'd been picturing Staff as, like, "get even better at the hard stuff."

**[00:25:07] Marcus Lindqvist:** A lot of people do. And you will keep doing the hard stuff, I'm not taking that away. It's more like, I want you deciding which hard stuff only you can do and handing the rest off with enough context that someone else can do it.

**[00:25:35] Priya Raman:** Tech-lead-ing, basically.

**[00:25:40] Marcus Lindqvist:** Yeah. On Northfold I'd like to make that official, actually. You're already doing it informally. I'd like to call you tech lead on the account starting next sprint, with the explicit expectation that part of the job is growing Devon.

**[00:26:09] Priya Raman:** I'd like that. Can I have Fridays as a no-meeting focus day if I'm taking on more coordination? Otherwise I'll stop writing any code and I'll lose my mind.

**[00:26:30] Marcus Lindqvist:** Yes. I'll block it on the team calendar. If anyone books over it, send them to me.

**[00:26:42] Priya Raman:** Deal.

**[00:26:47] Marcus Lindqvist:** Anything else on your side? How are you feeling about workload generally?

**[00:26:56] Priya Raman:** Honestly, a bit stretched. Not burning out, but the Tallgrass stuff on top of Northfold was too much. If that goes away I think I'm fine.

**[00:27:18] Marcus Lindqvist:** Okay. I'll check in on that in two weeks. If you're still stretched we'll look at it again. Let me recap the actions, and then I'll drop them in our 1:1 doc.

**[00:27:37] Priya Raman:** Go.

**[00:27:41] Marcus Lindqvist:** For you. One: rework the review on Devon's PR 412 with real written comments and a pairing session where he drives, by Friday the 9th. Two: write the PR template with an eval-results section for the Northfold repo, by the 14th. Three: for the next month, you're no longer sole required reviewer; anything with you for more than one business day, you review it or hand it off. Four: draft a short write-up of the adjuster-note chunking pattern by end of October, and we'll find a slot to present it to the other leads in November. Five: set up a weekly pairing hour with Jordan, starting next week.

**[00:29:02] Priya Raman:** Got it.

**[00:29:05] Marcus Lindqvist:** For me. One: talk to Devon about running the eval suite before opening PRs, this week. Two: update the CODEOWNERS and reviewer rotation on Northfold so Chidi and Jordan are first reviewers, by Monday. Three: stop tagging you on Tallgrass escalations, route them through Sam and Chidi. Four: announce you as Northfold tech lead starting the October 19th sprint. Five: block Fridays as your focus day. And six: get the updated Staff rubric from Elena and send it to you once it's final.

**[00:30:14] Priya Raman:** That's a good list. Thank you for the Staff stuff, actually. It's clearer than it's been.

**[00:30:26] Marcus Lindqvist:** Thank you for not throwing your laptop at me during the review part.

**[00:30:33] Priya Raman:** It was close. *(laughs)* See you at standup.

**[00:30:40] Marcus Lindqvist:** See you.

---

### Action items (as recorded by Marcus)

| Owner | Action | Due |
|---|---|---|
| Priya | Re-review Devon's PR #412 with written "why" comments; pair on structured-output approach with Devon driving | Fri Oct 9 |
| Priya | Add PR template with required eval-results section to Northfold repo | Wed Oct 14 |
| Priya | One-month trial: not sole required reviewer; review or explicitly hand off anything waiting >1 business day | Through Nov 6 |
| Priya | Write up adjuster-note chunking pattern for reuse (e.g., Pellworth Health); present to leads in November | Draft by Oct 30 |
| Priya | Start weekly pairing hour with Jordan Kim | Week of Oct 12 |
| Marcus | Talk to Devon about running eval suite and reporting scores in PRs | This week |
| Marcus | Update Northfold CODEOWNERS / reviewer rotation (Chidi, Jordan first reviewers) | Mon Oct 12 |
| Marcus | Route Tallgrass escalations via Sam/Chidi on-call; ask Priya directly, never tag her in client channel first | Ongoing |
| Marcus | Announce Priya as Northfold tech lead | Sprint starting Oct 19 |
| Marcus | Block Fridays as Priya's no-meeting focus day | This week |
| Marcus | Share final Staff rubric from Elena | When published |
