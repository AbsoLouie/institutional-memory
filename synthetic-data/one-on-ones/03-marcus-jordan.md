# 1:1 — Marcus Lindqvist / Jordan Kim

- **Category:** one-on-one
- **Date:** Thursday, October 22, 2026
- **Duration:** 30 minutes
- **Attendees:** Marcus Lindqvist (Engineering Manager), Jordan Kim (Engineer I)
- **Company:** Scope Creepers
- **Current staffing:** Jordan, Tallgrass Outdoor Co. customer-support agent project (Claude-based support assistant for orders, returns and gear advice)

---

**[00:00:08] Marcus Lindqvist:** Hey, Jordan. Sorry, I'm two minutes late. The meeting before this went long and I didn't have the heart to cut it off.

**[00:00:24] Jordan Kim:** No worries. I was just finishing up a Slack message anyway.

**[00:00:35] Marcus Lindqvist:** How's your week been? Did you end up going to that climbing gym thing?

**[00:00:46] Jordan Kim:** I did! The bouldering league. I was definitely the worst one there, but people were nice. I'm going to go back next week, I think.

**[00:01:05] Marcus Lindqvist:** Worst one there in week one is how everybody starts. Okay. I want to start with something good today, because I've been wanting to say it properly and not just in a Slack emoji.

**[00:01:32] Jordan Kim:** Oh. Okay.

**[00:01:38] Marcus Lindqvist:** The prompt-evaluation harness. I don't know if you realize how much it's changed how the team works. Northfold is using it now, Meridian started using it last week for Tomás's extraction evals, and Priya told me she's stopped hand-running regression checks entirely. On Tallgrass, it caught the refund-loop regression on October 14th before it went to production — the one where the agent kept offering store credit on orders that were already refunded. If that had shipped, it would've been a really bad week for their support team.

**[00:02:59] Jordan Kim:** I mean, that one was mostly just the golden-set check working the way it's supposed to.

**[00:03:13] Marcus Lindqvist:** Right, and the reason it worked is that you designed the golden-set check. You chose to do pairwise grading with a rubric instead of exact-match, you made it run in CI in under four minutes, and you added the per-category breakdown so we could see that the regression was only in the refunds category. Those were all decisions you made. They were good decisions.

**[00:04:04] Jordan Kim:** *(pause)* Okay. Thank you. I guess I kind of feel like I just glued some stuff together.

**[00:04:20] Marcus Lindqvist:** I hear that a lot from people about eight months in. And I'm going to gently disagree. "Glued some stuff together" is what most good infrastructure is. The judgment is in which stuff and how. I'd like you to try taking the compliment.

**[00:04:56] Jordan Kim:** *(laughs)* Okay. Taking it.

**[00:05:04] Marcus Lindqvist:** Good. Which actually ties into the first follow-up from last time. We talked about demo day. The next internal demo day is November 19th. Last time you said you'd "think about it." Did you think about it?

**[00:05:36] Jordan Kim:** I thought about it. I think I'm still kind of on the fence. Everyone else who presents is senior, and it's like — the harness isn't really a flashy thing. It's not a cool agent demo.

**[00:06:06] Marcus Lindqvist:** Can I tell you what I think the audience actually wants?

**[00:06:14] Jordan Kim:** Sure.

**[00:06:17] Marcus Lindqvist:** Half the people at demo day are going to go back to a client project the next morning where they're nervous about a prompt change breaking something. You're the person who solved that. The October 14th catch on Tallgrass is a five-minute story with a real before-and-after. That's a better demo than most agent demos, honestly.

**[00:07:03] Jordan Kim:** Huh. I didn't think about it like that.

**[00:07:11] Marcus Lindqvist:** And I'll help. We can do a run-through beforehand, and Priya's offered to pair with you, which I want to talk about too. But on demo day — can I put you down for a ten-minute slot?

**[00:07:38] Jordan Kim:** *(pause)* Okay. Yeah. Ten minutes. Put me down.

**[00:07:47] Marcus Lindqvist:** Great. I'm genuinely excited about that. Okay, now I want to talk about a couple of growth areas. None of this is "you're in trouble." It's "here's what gets you from good junior to solid mid-level."

**[00:08:16] Jordan Kim:** Okay.

**[00:08:19] Marcus Lindqvist:** The first one is getting stuck. I want to use a specific example. The token-caching issue on the Tallgrass harness — the one where prompt-cache hits were dropping to zero on the eval runs. When did you first hit that?

**[00:08:52] Jordan Kim:** Um. That was... the Monday. The 5th.

**[00:09:00] Marcus Lindqvist:** And when did you ask for help?

**[00:09:08] Jordan Kim:** Thursday. When Priya noticed my PR was still in draft and asked about it.

**[00:09:22] Marcus Lindqvist:** Right. So that's three and a half days. And when Priya looked at it, how long did it take to figure out?

**[00:09:38] Jordan Kim:** Like, twenty minutes. It was the timestamp in the system prompt. I was injecting the current date at the top, so the prefix changed every run and nothing cached.

**[00:10:02] Marcus Lindqvist:** Yeah. And to be clear — that's a genuinely sneaky bug. People with ten years of experience make that exact mistake. The issue isn't that you didn't spot it. It's that three of those days were probably not very productive, and there was someone right there who'd seen it before.

**[00:10:46] Jordan Kim:** I know. I just — I didn't want to bother her. She's always slammed. And I felt like I should be able to figure it out myself. Like, if I can't figure out caching, what am I doing here?

**[00:11:15] Marcus Lindqvist:** *(pause)* Can I say something about that last part?

**[00:11:24] Jordan Kim:** Yeah.

**[00:11:26] Marcus Lindqvist:** "What am I doing here" — I hear that, and I don't want to just brush past it. But from where I'm sitting, you're doing exactly what we hired you to do, and doing it better than I expected eight months in. The harness is evidence of that. Asking for help after an hour isn't evidence that you don't belong. It's what people who belong do. Priya asks people things constantly. I ask people things constantly.

**[00:12:29] Jordan Kim:** *(quietly)* Okay. That's — yeah. Thanks.

**[00:12:40] Marcus Lindqvist:** So here's the concrete thing I'd suggest. A timebox. If you've been stuck on the same problem for 90 minutes without new information — not just "without solving it," but without learning anything new — you post in the team channel. Not a DM to one person, the channel, so whoever's free can answer. And write it as: what you're trying to do, what you tried, what you expected, what happened.

**[00:13:37] Jordan Kim:** Ninety minutes feels really short.

**[00:13:45] Marcus Lindqvist:** It does at first. Try it for a month. Worst case, someone says "oh, I don't know either," and you've lost nothing.

**[00:14:01] Jordan Kim:** Okay. I can try that.

**[00:14:06] Marcus Lindqvist:** And on Priya being slammed. She's specifically asked to set up a weekly pairing hour with you. That's coming from her, not me pushing her. She said, and I'm quoting, "Jordan's great, they just never ask anything." So she wants the questions.

**[00:14:44] Jordan Kim:** *(laughs)* That's — wow, okay. That's kind of embarrassing but also nice?

**[00:14:58] Marcus Lindqvist:** It's mostly nice. She should be reaching out this week to set up a time. If you haven't heard from her by Monday, ping her.

**[00:15:14] Jordan Kim:** Okay.

**[00:15:20] Marcus Lindqvist:** Second area. Client meetings. In the last three Tallgrass syncs, I don't think you spoke, other than when I asked you directly. And in the October 15th one, when their support lead, Gabe, asked why the agent was recommending sleeping bags for a camp-stove question, you knew the answer. You'd literally written the retrieval filter that caused it. But you waited for me to answer, and I gave a worse answer than you would have.

**[00:16:25] Jordan Kim:** Yeah. I knew. I just — I didn't know if it was my place to jump in. You're the one running the meeting.

**[00:16:41] Marcus Lindqvist:** That's a really reasonable thing to wonder, and I think I haven't been clear about it. So let me be clear now: if the question is about something you built, it's your place. You're the expert on it. I'd much rather you answer and I fill in context than the other way around.

**[00:17:19] Jordan Kim:** Okay. What if I get it wrong in front of the client, though?

**[00:17:30] Marcus Lindqvist:** Then you say, "Actually, let me double-check that and follow up in Slack." Which is a sentence I say probably twice a week. Clients like hearing that. It means we're being careful.

**[00:17:57] Jordan Kim:** That's — yeah, okay. That feels doable.

**[00:18:05] Marcus Lindqvist:** Here's a smaller step. For the next Tallgrass sync, on the 29th, I'd like you to own one agenda item. Five minutes. The harness results from that week — how the agent's scoring, what changed. You present, I'll back you up.

**[00:18:38] Jordan Kim:** One item. Okay. That's actually good practice for demo day, too.

**[00:18:49] Marcus Lindqvist:** Exactly. Same muscle.

**[00:18:54] Jordan Kim:** Can I — sorry, can I give you some feedback? You always ask at the end and I never say anything, so.

**[00:19:10] Marcus Lindqvist:** *(laughs)* Yes. Please. This is great.

**[00:19:18] Jordan Kim:** Um. It's — our 1:1s have been rescheduled four times since August. And every time, it kind of feels like... I'm the thing that's easy to move. And then when we do meet, I feel like I need to have, like, a big agenda to justify it.

**[00:19:56] Marcus Lindqvist:** *(pause)* Yeah. That's — you're right. I checked my calendar last week, actually, and I'd moved yours more than anyone else's. And the honest reason is exactly what you said: you never complain, so it was the easiest one to move. Which is backwards. I'm sorry.

**[00:20:37] Jordan Kim:** It's okay. I just wanted to say it.

**[00:20:42] Marcus Lindqvist:** I'm really glad you did. And notice what you just did: you raised something hard, clearly, with a specific example. That's exactly the client-meeting skill we were just talking about. So, from now on, our 1:1 doesn't move unless one of us is out sick or on PTO. And you don't need an agenda. "Nothing big this week" is a completely fine 1:1.

**[00:21:34] Jordan Kim:** Okay. Thanks.

**[00:21:39] Marcus Lindqvist:** Third thing, and it's smaller. Documentation. Last time you said you'd get the harness README written by mid-October. How far did you get?

**[00:22:01] Jordan Kim:** Um. It's — there's a README. It has the install steps. It doesn't really explain the rubric format or how to add a new category.

**[00:22:23] Marcus Lindqvist:** Right. And I think that's the one place the harness's success is starting to hurt. Tomás spent most of an afternoon last week figuring out how to write a rubric for the Meridian extraction evals, and he ended up DMing you. Which is fine once, but you're going to become the bottleneck for a tool everyone uses.

**[00:23:09] Jordan Kim:** Yeah. He did DM me. I spent like an hour on it with him.

**[00:23:20] Marcus Lindqvist:** So, two asks. Finish the README with a "how to add an eval category" section and one worked example — use the Tallgrass refunds category since it's real. And going forward, when you open a PR, the description should say what changed and why, not just "fix eval bug." Your PR 87 last week was literally titled "fixes."

**[00:24:11] Jordan Kim:** *(laughs)* Yeah. That was bad.

**[00:24:17] Marcus Lindqvist:** It happens. But for a junior engineer, documentation is the cheapest way to make your work visible. Every good PR description is a little bit of evidence of how you think.

**[00:24:41] Jordan Kim:** That makes sense. And actually, if I write the README properly, I could basically use it as the structure for the demo day talk.

**[00:25:00] Marcus Lindqvist:** That's a really good idea. Do that.

**[00:25:08] Jordan Kim:** Okay.

**[00:25:11] Marcus Lindqvist:** Last thing from me — just checking how you're feeling about where you are generally. Eight months in. How's it feel?

**[00:25:27] Jordan Kim:** Honestly? Mixed. The work is the best I've ever done. But I spend a lot of time feeling like everyone else knows what they're doing and I'm faking it. Today helped, though. Especially the part about Priya.

**[00:26:00] Marcus Lindqvist:** I'm glad. And I'll say it plainly so there's no ambiguity: you're tracking well. If you keep going on the stuff we talked about today — asking sooner, speaking up in client meetings, documenting — I'd expect us to be talking about a promotion to Engineer II sometime in the first half of next year.

**[00:26:43] Jordan Kim:** *(pause)* Oh. Okay. I didn't — okay. That's really good to hear.

**[00:26:57] Marcus Lindqvist:** It's true. Okay, let me read back what we agreed.

**[00:27:05] Jordan Kim:** Sure.

**[00:27:08] Marcus Lindqvist:** For you. One: ten-minute demo day slot on November 19th, presenting the eval harness and the October 14th refund-regression catch. Two: the 90-minute stuck rule — post in the team channel with what you tried, starting now, try it for a month. Three: own the harness-results agenda item at the Tallgrass sync on the 29th. Four: finish the README with a "how to add an eval category" section and the refunds worked example, by November 6th. Five: write real PR descriptions — what and why. Six: if Priya hasn't reached out about pairing by Monday the 26th, ping her.

**[00:28:32] Jordan Kim:** Got it. That's a lot, but it's all — yeah. Okay.

**[00:28:40] Marcus Lindqvist:** For me. One: stop rescheduling our 1:1 except for illness or PTO. Two: in Tallgrass meetings, redirect technical questions about the harness or retrieval to you instead of answering myself. Three: book a demo day dry run with you for the week of November 9th. Four: confirm with Priya she's setting up the pairing hour.

**[00:29:29] Jordan Kim:** Thanks, Marcus. Really.

**[00:29:34] Marcus Lindqvist:** Thank you for the feedback. Seriously. Have fun at bouldering.

**[00:29:45] Jordan Kim:** I'll be the worst one there again. *(laughs)* Bye.

---

### Action items (as recorded by Marcus)

| Owner | Action | Due |
|---|---|---|
| Jordan | Present eval harness (incl. Oct 14 Tallgrass refund-regression catch) at internal demo day, 10-min slot | Thu Nov 19 |
| Jordan | 90-minute stuck rule: post in team channel with goal / tried / expected / actual | Ongoing, 1-month trial |
| Jordan | Own harness-results agenda item at Tallgrass sync | Thu Oct 29 |
| Jordan | Complete harness README incl. "how to add an eval category" + refunds worked example | Fri Nov 6 |
| Jordan | Write descriptive PR descriptions (what changed and why) | Ongoing |
| Jordan | Ping Priya about weekly pairing hour if not contacted | Mon Oct 26 |
| Marcus | Stop rescheduling Jordan's 1:1 except illness/PTO | Ongoing |
| Marcus | Redirect harness/retrieval questions in Tallgrass meetings to Jordan | Ongoing |
| Marcus | Schedule demo day dry run with Jordan | Week of Nov 9 |
| Marcus | Confirm Priya is setting up pairing with Jordan | This week |
