# 1:1 — Marcus Lindqvist / Tomás Herrera

- **Category:** one-on-one
- **Date:** Tuesday, October 13, 2026
- **Duration:** 29 minutes
- **Attendees:** Marcus Lindqvist (Engineering Manager), Tomás Herrera (Engineer II)
- **Company:** Scope Creepers
- **Current staffing:** Tomás, Meridian Freight document-extraction project (Claude-based bill-of-lading and invoice reconciliation)

---

**[00:00:05] Marcus Lindqvist:** Hey, Tomás. Oh — is that a baby monitor behind you?

**[00:00:15] Tomás Herrera:** *(laughs)* Yeah, it's on the shelf. Lucía's napping. Ana's at her mom's this afternoon so I'm on monitor duty. If it lights up I might have to vanish for a second.

**[00:00:39] Marcus Lindqvist:** Totally fine. How's she doing? How are you doing? Last time you said you were averaging, what, four hours?

**[00:00:54] Tomás Herrera:** It's better. She's sleeping a five-hour stretch most nights now, which feels like a luxury hotel. I'm not going to pretend I'm fully rested, but I'm a person again. Mostly.

**[00:01:20] Marcus Lindqvist:** That's real progress. Okay. I want to say up front, the main thing I want to talk about today is the reconciliation feature on Meridian. I think you probably know that's coming.

**[00:01:46] Tomás Herrera:** Yeah. I figured. I've been kind of dreading it, honestly.

**[00:01:56] Marcus Lindqvist:** I get that. I'm not coming in angry. I want to understand what happened, and I want us to come out of this with a way of working that means it doesn't happen again. That's the goal. Sound okay?

**[00:02:22] Tomás Herrera:** Yeah. Okay.

**[00:02:27] Marcus Lindqvist:** So, just to lay out the facts as I understand them so we're on the same page. The multi-document reconciliation feature — matching bills of lading to carrier invoices and flagging mismatches — was estimated at two weeks during the August 24th scoping call. It shipped on September 30th, so about five weeks. And the part that's actually the bigger problem: I found out it was late on September 18th, when Hannah Wexler at Meridian emailed me asking why the demo for their finance team had been pushed twice. Is that right?

**[00:03:47] Tomás Herrera:** That's right. Yeah.

**[00:03:52] Marcus Lindqvist:** So the five weeks — features slip, that happens, and frankly the code that came out the other end is really good. I'll come back to that. The thing I need to understand is the gap between when you knew it was slipping and when anybody else knew.

**[00:04:26] Tomás Herrera:** Okay. So, honestly? I knew in week two. Probably around September 3rd. That's when I realized the invoices from their three biggest carriers don't use consistent line-item identifiers. Some use PRO numbers, some use their own internal references, one of them sometimes just doesn't include anything and you have to match on weight and date. So the "just extract and join" approach I'd estimated wasn't going to work. I needed a fuzzy matching step with a confidence score, plus a review queue for the low-confidence ones.

**[00:05:45] Marcus Lindqvist:** And that's a totally legitimate thing to discover. Why didn't it come up?

**[00:05:58] Tomás Herrera:** *(pause)* A few reasons. I think the honest one is I kept thinking I was a few days from solving it. Like, every Monday I'd think, "okay, if I get the carrier-specific prompts right this week, I'll catch up." And then I didn't want to come to you or Hannah with a problem and no answer.

**[00:06:42] Marcus Lindqvist:** Yeah.

**[00:06:45] Tomás Herrera:** And — I mean, this is going to sound like an excuse.

**[00:06:53] Marcus Lindqvist:** Say it anyway.

**[00:06:58] Tomás Herrera:** Lucía was three weeks old in early September. I was back from leave maybe ten days. I think I was just — I didn't have the bandwidth to think about anything beyond the next task. Flagging risk takes a kind of, like, zoomed-out brain, and I didn't have one.

**[00:07:39] Marcus Lindqvist:** That's not an excuse. That's context, and it's important context. I want to separate two things. One is that it was a hard time for you, and I should've checked in more than I did. I knew you'd just come back and I basically assumed no news was good news. That's on me.

**[00:08:18] Tomás Herrera:** I appreciate that.

**[00:08:20] Marcus Lindqvist:** The other thing is that, independent of the circumstances, the client found out before I did. And at a consultancy, that's the part that does the damage. Hannah wasn't upset that it took five weeks — she told me as much. She was upset that she'd told her CFO it'd be ready for a demo on the 11th, and then had to walk it back. Twice. That's trust we spend down.

**[00:09:14] Tomás Herrera:** Yeah. I know. I felt sick when I saw her email.

**[00:09:25] Marcus Lindqvist:** I know you did. I could tell from how fast you replied. *(pause)* Can I push on one thing, though? You said you didn't want to come with a problem and no answer. Where'd that come from? Is that something I've done?

**[00:09:56] Tomás Herrera:** Um. Kind of, actually? Can I be honest?

**[00:10:03] Marcus Lindqvist:** Please.

**[00:10:06] Tomás Herrera:** In my first year, when I was on the Brightwell Retail chatbot, I brought you a blocker in standup once and you said something like, "Okay, what's your proposal?" And I didn't have one, and it felt — I know you didn't mean it this way — but it felt like I shouldn't bring things up until I had a plan.

**[00:10:50] Marcus Lindqvist:** Oh. Huh. Yeah, I do say that a lot.

**[00:10:57] Tomás Herrera:** And on the scoping call, too. The two-week number. I said "two to three weeks" and you said "let's say two, they're price-sensitive," and then that just became the number. I didn't push back because I figured you knew the client better.

**[00:11:31] Marcus Lindqvist:** *(pause)* That's fair, and I'm glad you said it. I did do that. I rounded your estimate down in front of the client. That's a bad habit, and it put you in a position where the real number was already behind before you'd started. I'm sorry.

**[00:12:04] Tomás Herrera:** It's okay. I should've said something then, too.

**[00:12:12] Marcus Lindqvist:** Maybe. But I'm the one who should be protecting your estimates, not trimming them. So, two changes on my side. First, I won't round down an engineer's estimate in a client meeting. If I think it's too high, I'll talk to you about it afterward, not in front of them. Second — and this is the bigger one — "what's your proposal" is fine when someone's ready, but I want "I don't have a plan yet, but this is slipping" to be a completely normal sentence on this team. Early and incomplete beats late and polished. Every time.

**[00:13:24] Tomás Herrera:** Okay. That actually helps a lot to hear.

**[00:13:35] Marcus Lindqvist:** Good. Now, from your side. Let's talk about what you'd do differently, and I've got a suggestion, but I want yours first.

**[00:13:53] Tomás Herrera:** I think... at the point I realized the identifiers were inconsistent, that was the moment. That's when the estimate became invalid. I should've written two lines in the project channel: "Found that carrier invoices don't share IDs, the original approach won't work, I think this adds two to three weeks, investigating." Even that would've been enough for you to manage Hannah.

**[00:14:47] Marcus Lindqvist:** Exactly. That's exactly it. That's the whole thing. You don't need to have solved it, you need to say the estimate's broken.

**[00:15:05] Tomás Herrera:** Yeah.

**[00:15:08] Marcus Lindqvist:** So, my suggestion builds on that. Two habits. One: a tripwire rule. If you're more than 25 percent through the time budget and less than 25 percent confident in the remaining approach, or if you discover something that changes the shape of the work, you flag it within one business day. Doesn't need a solution. Just "the estimate is at risk, here's why."

**[00:15:59] Tomás Herrera:** Twenty-five percent. Okay. So on a two-week thing, that's like day three or four.

**[00:16:09] Marcus Lindqvist:** Right. Two: a weekly status note to Hannah, every Friday, that you write and I'm cc'd on. Three bullets. What shipped, what's next, what's at risk. Green, yellow, red. Five minutes.

**[00:16:40] Tomás Herrera:** Directly to Hannah? Not through you?

**[00:16:46] Marcus Lindqvist:** Directly to Hannah. Honestly, she'd like that. She told me she likes you and she likes your work — she just wants visibility. And it gives you a forcing function. It's hard to write "green" on Friday when you know it's not.

**[00:17:16] Tomás Herrera:** *(laughs)* Yeah, that's a little evil. But it'll work.

**[00:17:27] Marcus Lindqvist:** That's the idea. Does Friday work with the — with Lucía, with your schedule?

**[00:17:40] Tomás Herrera:** Friday morning is good. Ana does mornings Fridays, so I'm usually at my desk early.

**[00:17:53] Marcus Lindqvist:** Great. Okay, I want to spend a minute on the stuff that went well, because it'd be weird and wrong to only talk about the slip.

**[00:18:11] Tomás Herrera:** Sure.

**[00:18:13] Marcus Lindqvist:** The reconciliation module itself is excellent. I asked Priya to look at it with fresh eyes, and she said — I'm quoting from Slack — "this is the cleanest extraction code on any of our accounts." The confidence-scored matching with the human review queue for anything under 0.8 is exactly right for a finance use case. And the test coverage. You wrote fixture invoices for all three carriers, including the one with no identifiers, and the eval set has 140 real document pairs. That's going to save us on every future change.

**[00:19:33] Tomás Herrera:** Thanks. That's — I was worried the whole thing would just be remembered as "the late feature."

**[00:19:46] Marcus Lindqvist:** No. And Hannah's team has already run 2,000 invoices through it since launch with a 96 percent auto-match rate. That's a real outcome. The lateness and the quality are both true. I want you to hold both.

**[00:20:20] Tomás Herrera:** Okay.

**[00:20:22] Marcus Lindqvist:** One more thing from last time. You'd said you wanted to get better at estimation, specifically on LLM extraction work, since it's so variable. Did you get a chance to look at the estimation retro doc from the Okonjo Legal project that I sent?

**[00:20:53] Tomás Herrera:** I read it. Honestly, it was very relevant. They had the exact same pattern — the "happy path" took a week and the messy-document long tail took three. I think the takeaway for me is I should estimate the long tail separately, explicitly, instead of folding it into one number.

**[00:21:32] Marcus Lindqvist:** Yes. I'd love to see that become how you scope extraction work. Like: "Core extraction, one week. Edge-case handling, unknown until we've seen fifty real documents; we'll re-estimate on day three."

**[00:22:03] Tomás Herrera:** Yeah. And I'd want to look at real documents before the scoping call, not after. On Meridian I didn't see their actual carrier invoices until the first day of the build.

**[00:22:26] Marcus Lindqvist:** That's a really good point, and it's a process gap on our side. Let's make it a rule for extraction scoping: we ask for a sample set before we give a number. I'll raise it with the sales leads.

**[00:22:52] Tomás Herrera:** That'd help a lot.

**[00:22:57] Marcus Lindqvist:** Okay. Next up on Meridian is the customs-declaration extraction, right? That's due to scope next week?

**[00:23:12] Tomás Herrera:** Yeah, the scoping call is the 20th.

**[00:23:17] Marcus Lindqvist:** I'd like you to lead the estimate on that call. You present the number, with the long tail split out. I'll be there, and I'll keep my mouth shut on the number.

**[00:23:41] Tomás Herrera:** *(laughs)* Okay. I'll hold you to that.

**[00:23:48] Marcus Lindqvist:** Please do. And before the call, let's do a 15-minute dry run on the 19th so you're not walking in cold.

**[00:24:04] Tomás Herrera:** Yeah, I'd like that.

**[00:24:09] Marcus Lindqvist:** How are you otherwise? Workload, energy, the baby? Is there anything you need from me — flexible hours, anything?

**[00:24:27] Tomás Herrera:** Um. Honestly, the Thursday 8 a.m. Meridian sync is hard. That's right in the middle of the morning chaos. If we could move it to ten, that'd make a real difference.

**[00:24:53] Marcus Lindqvist:** I'll ask Hannah. I'd be surprised if she minds. And if you need to log off early or shift hours, just put it on your calendar, you don't need to ask me. Seriously.

**[00:25:16] Tomás Herrera:** Thanks, Marcus.

**[00:25:19] Marcus Lindqvist:** And one more thing. I want to apologize again for not checking in more in September. That's the period where I should've been more present, not less. If you're having a rough week, just say "rough week" in our DM. No detail needed.

**[00:25:50] Tomás Herrera:** I appreciate that. Really.

**[00:25:57] Marcus Lindqvist:** Okay. Let me read back actions.

**[00:26:02] Tomás Herrera:** Go ahead.

**[00:26:05] Marcus Lindqvist:** Yours. One: starting this Friday, the 16th, send Hannah a weekly status note, three bullets — shipped, next, at risk — with a green/yellow/red, cc me. Two: adopt the tripwire rule. If you're 25 percent through the budget and not confident, or the shape of the work changes, flag it in the project channel within one business day, solution not required. Three: lead the estimate for customs-declaration extraction on the October 20th scoping call, with the long tail estimated separately. Four: before the call, get a sample of real customs docs from Meridian.

**[00:27:25] Tomás Herrera:** Got it.

**[00:27:27] Marcus Lindqvist:** Mine. One: I don't round down engineer estimates in front of clients. Ever. Two: dry run with you on the 19th. Three: ask Hannah about moving the Thursday sync to 10 a.m., by end of this week. Four: propose the "sample documents before estimate" rule to the sales leads by end of month. Five: a quick two-minute check-in with you each Wednesday through November, just on how things are going, not status.

**[00:28:27] Tomás Herrera:** That's a good list. Thanks for being decent about this.

**[00:28:35] Marcus Lindqvist:** Thanks for being honest about it. Including the part about me. Go rescue your monitor, I think it just lit up.

**[00:28:50] Tomás Herrera:** *(laughs)* It did. Okay, talk soon.

---

### Action items (as recorded by Marcus)

| Owner | Action | Due |
|---|---|---|
| Tomás | Weekly Friday status note to Hannah Wexler (shipped / next / at risk, RAG status), cc Marcus | Starting Fri Oct 16 |
| Tomás | Tripwire rule: flag estimate risk in project channel within 1 business day of discovery (no solution required) | Ongoing |
| Tomás | Request sample customs documents from Meridian before scoping | Before Oct 20 |
| Tomás | Lead the estimate on customs-declaration extraction scoping call; split long-tail estimate out | Tue Oct 20 |
| Marcus | Never round down engineer estimates in client meetings | Ongoing |
| Marcus | 15-min estimate dry run with Tomás | Mon Oct 19 |
| Marcus | Ask Hannah to move Thursday sync from 8 a.m. to 10 a.m. | Fri Oct 16 |
| Marcus | Propose "sample documents before estimate" rule for extraction work to sales leads | Fri Oct 30 |
| Marcus | Brief weekly Wednesday wellbeing check-in with Tomás | Through November |
