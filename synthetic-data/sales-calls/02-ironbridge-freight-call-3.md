# Discovery Call: Ironbridge Freight x Scope Creepers

- **Category:** sales-discovery
- **Date:** 2026-10-27
- **Duration:** 22 min
- **Platform:** Zoom
- **Call type:** Discovery call 3 of 3 (prospect)

## Attendees

| Name | Company | Role |
|---|---|---|
| Maya Okafor | Scope Creepers | Partner / Account Executive |
| Dev Patel | Scope Creepers | Principal Solutions Engineer |
| Marcus Delgado | Ironbridge Freight | Chief Technology Officer |
| Linda Brandt | Ironbridge Freight | Chief Financial Officer |

---

## Transcript

**[00:00:06] Marcus Delgado:** Hi, hi. Okay, Linda's joining from her office, she'll be on in a second.

**[00:00:13] Maya Okafor:** Hi Marcus. No rush. How's Gary?

**[00:00:17] Marcus Delgado:** Gary is, honestly, a convert. He ran Dev's VB6 sample past two of our developers and said, quote, "it's annoyingly good." From Gary that's a standing ovation.

**[00:00:34] Dev Patel:** Ha. I'll take it. I'll frame it.

**[00:00:39] Marcus Delgado:** He also said the button-click example was "too clean" and ours are worse. So, be warned.

**[00:00:47] Dev Patel:** I believe him.

**[00:00:50] Linda Brandt:** Hello? Can you hear me?

**[00:00:53] Maya Okafor:** We can. Hi Linda, I'm Maya. Thanks for joining. And this is Dev.

**[00:01:00] Linda Brandt:** Hi both. Sorry, I'm coming out of a lender call. Marcus has told me a lot about you.

**[00:01:09] Maya Okafor:** All good, I hope.

**[00:01:12] Linda Brandt:** Mostly. He's excited. My job is to be less excited.

**[00:01:19] Maya Okafor:** Ha. That's fair, and honestly, that's why we wanted you here. So, quick recap for you, Linda. On our last call with Marcus and Gary, we went through DART in some detail, and the timing. The retailer API by Q3 2027, Gary retiring at the end of 2027, and the modernization budget, seven hundred minus a hundred and fifty for telematics, so about five-fifty, committed by December. And Marcus, you were going to confirm who signs off.

**[00:02:02] Marcus Delgado:** Right. So. I owe you a correction there, too. I'd been assuming it was mine to sign. It's not.

**[00:02:13] Linda Brandt:** It's not.

**[00:02:14] Marcus Delgado:** Linda, do you want to explain it? You'll explain it better.

**[00:02:19] Linda Brandt:** Sure. After 2022, the board changed the approval policy. Anything over two hundred and fifty thousand, any single commitment, needs my approval and then board approval. Doesn't matter whose budget it's in. Under two-fifty, I can approve it. Marcus can sign operating stuff, licenses, that kind of thing, but not a project like this.

**[00:02:54] Maya Okafor:** That's really helpful, thank you. So the CTO doesn't sign this. You and the board do.

**[00:03:03] Linda Brandt:** For anything at the size Marcus has been describing, yes. And honestly, I'd rather you hear that from me than find out at contract time.

**[00:03:14] Maya Okafor:** Agreed. When does the board next meet?

**[00:03:19] Linda Brandt:** December ninth. That's the last meeting before year end. So if this is going to use this year's money, it has to be approved on the ninth. There's no second chance in December.

**[00:03:36] Marcus Delgado:** Which is why I wanted Linda on this call and not the next one.

**[00:03:42] Maya Okafor:** That makes sense. And it lines up with the December commit date you mentioned, Marcus.

**[00:03:49] Marcus Delgado:** Exactly.

**[00:03:52] Linda Brandt:** Can I be blunt?

**[00:03:55] Maya Okafor:** Please.

**[00:03:56] Linda Brandt:** I negotiated the exit from the 2022 contract. We spent two point one million dollars over fourteen months and got a UI mockup. I had to explain that to the board, three times. So my bar for walking into that boardroom with another modernization project is very high. Not because I don't think DART needs it. It obviously does. Because I can't do 2022 again.

**[00:04:35] Maya Okafor:** That's completely fair. Can I ask what went wrong, from your seat? Marcus has given us the technical side.

**[00:04:45] Linda Brandt:** From my seat? Three things. One, the contract was time and materials with a cap that we hit and then renegotiated. Twice. Two, there was nothing I could measure. Every status report said "on track" until the day it said "we need another nine months." And three, there was no point where we could stop and keep something. It was all or nothing, and we got nothing.

**[00:05:23] Maya Okafor:** Okay. Those are really clear. Dev, do you want to take the measurement one?

**[00:05:30] Dev Patel:** Sure. Linda, the short version is, the thing we measure is whether the new logic produces the same numbers as the old logic. We take, say, two years of real driver pay calculations from production, run them through both, and they have to match to the penny. So instead of "on track," the report says "we've reproduced ninety-four percent of pay runs exactly, here are the six percent that don't match and why."

**[00:06:09] Linda Brandt:** That I can read.

**[00:06:12] Dev Patel:** And the driver pay piece is exactly where the last project fell apart. The numbers didn't match and nobody could say why. In our approach, every mismatch is a specific case with a specific driver and a specific rule. It's work, but it's visible work.

**[00:06:38] Linda Brandt:** And the all-or-nothing part?

**[00:06:42] Dev Patel:** We don't replace DART. We carve off one capability at a time and put an API in front of it. DART keeps running the whole time. So if you stopped us after the first slice, you'd still have a working tendering API for the retailer, and DART would still be doing everything else.

**[00:07:08] Linda Brandt:** So each piece stands on its own.

**[00:07:10] Dev Patel:** Each piece stands on its own. That's the point.

**[00:07:15] Maya Okafor:** And on the contract side, we'd structure it the way you just described wanting it. Fixed fee per phase, defined deliverables, and an explicit point between phases where you can stop and keep what you've got.

**[00:07:33] Linda Brandt:** Okay. I'm listening.

**[00:07:38] Marcus Delgado:** See? I told you.

**[00:07:40] Linda Brandt:** Marcus, you told me the last ones were great too.

**[00:07:45] Marcus Delgado:** Fair. That's fair.

**[00:07:49] Linda Brandt:** Let me ask about money, since that's my job. Marcus says five-fifty is available. That's right. The telematics hundred and fifty is committed, the ELD contract's signed. So you're working with five-fifty, and it has to be approved on December ninth. What would you want to spend it on?

**[00:08:16] Maya Okafor:** Honestly, I don't think we should ask you for five-fifty today. I don't think you could take that to the board on December ninth without evidence, and I wouldn't want you to.

**[00:08:32] Linda Brandt:** Okay. Go on.

**[00:08:35] Maya Okafor:** What we'd suggest is a paid two-week assessment first. Fixed fee. Dev and the team take the DART codebase, map it, and produce real outputs. A code map of tendering, since that's the retailer piece. A sample driver pay spec, for the line-haul pay. Gary already told Dev to leave local pay for later.

**[00:09:03] Marcus Delgado:** Ha. He did.

**[00:09:06] Maya Okafor:** A security scan of the codebase. And a phased plan with costs, with the tendering API as phase one. So when you walk into the board on the ninth, you're not asking them to trust a pitch. You're showing them work on your own code.

**[00:09:29] Linda Brandt:** What does the assessment cost?

**[00:09:32] Maya Okafor:** For a codebase this size, forty to sixty thousand. We'd firm it up once Dev sees the repo structure. Fixed, not hourly.

**[00:09:45] Linda Brandt:** That's under my threshold. I can approve that without the board.

**[00:09:51] Marcus Delgado:** Which is why I didn't want to just sign it myself. I can't.

**[00:09:56] Linda Brandt:** You can't.

**[00:09:58] Dev Patel:** Timing-wise, if we start the week of November ninth, we'd have the readout by November twentieth. That gives you almost three weeks before the board.

**[00:10:12] Linda Brandt:** I need the board pack done by December second. So that works, but not with a lot of slack.

**[00:10:21] Maya Okafor:** Understood. We'd plan around the second, not the ninth.

**[00:10:26] Linda Brandt:** Good. What happens if the assessment says this is a mess?

**[00:10:32] Dev Patel:** Then you've spent fifty thousand to learn that, instead of two million. And honestly, you'd still have the code map and the security scan. Gary mentioned there's some, let's say, sensitive data hard-coded in old test procedures.

**[00:10:54] Linda Brandt:** Marcus?

**[00:10:55] Marcus Delgado:** There are some hard-coded SSNs in test procedures from like 2006. Gary's been meaning to clean them up.

**[00:11:05] Linda Brandt:** Marcus.

**[00:11:06] Marcus Delgado:** I know. I know. It's on the list.

**[00:11:11] Linda Brandt:** That needs to be in the assessment regardless of what we do after.

**[00:11:16] Dev Patel:** It will be. The scan will find them.

**[00:11:21] Linda Brandt:** Okay. Let me ask a different question. What else comes out of this for the business? The board's going to ask what we get besides a newer DART.

**[00:11:35] Maya Okafor:** That's a good question. Marcus has mentioned a few things. The where's-my-load calls, the POD matching in billing. Is there anything on your side?

**[00:11:48] Linda Brandt:** Reporting. We have, Marcus, how many Crystal Reports?

**[00:11:54] Marcus Delgado:** About three hundred and fifty.

**[00:11:56] Linda Brandt:** Three hundred and fifty Crystal Reports. My team exports every single one of them to Excel and redoes them. I've been asking for a data warehouse for three years. If this project makes DART's data accessible, I want to know that's on the roadmap.

**[00:12:19] Dev Patel:** It falls out pretty naturally. Once there's an API layer and the data's mapped, a warehouse is a much smaller project.

**[00:12:29] Linda Brandt:** Good. Write that down.

**[00:12:32] Maya Okafor:** Written.

**[00:12:34] Linda Brandt:** And, this isn't IT, but, my AP team keys in fuel receipts. By hand. Thousands a month. Every time I see the headcount I wince.

**[00:12:48] Maya Okafor:** That's a common one. We can talk about it another time.

**[00:12:54] Linda Brandt:** Another time. I'm just saying, if I'm going to the board with an AI story, I'd like it to be bigger than one system.

**[00:13:04] Marcus Delgado:** Pat's going to ask "what's our AI strategy" at the January meeting anyway. One of the board members sits on the board of a logistics tech company and keeps asking.

**[00:13:18] Maya Okafor:** Could the assessment include a one-page view of that? DART modernization as the foundation, and the other use cases sitting on top. Not a full roadmap. A page.

**[00:13:34] Linda Brandt:** A page is plenty. Boards don't read more than a page.

**[00:13:39] Maya Okafor:** Then we'll do a page.

**[00:13:42] Linda Brandt:** Who's Pat going to want to meet?

**[00:13:47] Marcus Delgado:** Pat'll want to meet them before the ninth. Pat's going to ask one question. "How is this different from last time."

**[00:13:57] Dev Patel:** The tests are the answer. Proof, not promises.

**[00:14:02] Linda Brandt:** Put that on a slide.

**[00:14:05] Marcus Delgado:** That's what I said!

**[00:14:08] Linda Brandt:** Then you were right once.

**[00:14:11] Maya Okafor:** Ha. Linda, are there other approvals we should know about? Legal, procurement?

**[00:14:18] Linda Brandt:** Legal reviews the SOW and the NDA. Procurement isn't involved under two-fifty. Over two-fifty, procurement wants three quotes. Marcus, you have other quotes?

**[00:14:34] Marcus Delgado:** There's an offshore firm that does automated VB6 conversion, and our Microsoft partner's been pitching something with Copilot. I haven't engaged seriously with either.

**[00:14:49] Linda Brandt:** Get them to quote anyway. The board will ask.

**[00:14:54] Marcus Delgado:** Fine.

**[00:14:57] Dev Patel:** For what it's worth, Gary looked at the converter output. He said it was VB6 written in C# syntax.

**[00:15:07] Linda Brandt:** I don't know what that means, but I can tell it's bad.

**[00:15:12] Dev Patel:** It's bad.

**[00:15:15] Linda Brandt:** One more thing. Gary. Marcus tells me if Gary's not in, this doesn't work. How much of Gary does this take?

**[00:15:27] Dev Patel:** For the assessment, a ninety-minute working session up front, then maybe four or five hours over the two weeks reviewing what we produce. He's correcting, not authoring.

**[00:15:41] Marcus Delgado:** And for the full thing, realistically twenty-five, thirty percent of his time. I want to backfill some on-call.

**[00:15:51] Linda Brandt:** Backfill costs money.

**[00:15:54] Marcus Delgado:** It does. It's less than an outage.

**[00:15:58] Linda Brandt:** Ha. Fair.

**[00:16:01] Dev Patel:** We'll also need production pay data for the tests. Anonymized. Gary said that'd eat a week.

**[00:16:10] Marcus Delgado:** It would. He was clear.

**[00:16:12] Dev Patel:** We'll write the anonymization script with him. That takes it down to a day or two.

**[00:16:20] Linda Brandt:** Good. If driver data's leaving the building, I want that in writing.

**[00:16:25] Maya Okafor:** We'll include it in the SOW, along with the data-handling note Dev sent Gary.

**[00:16:32] Linda Brandt:** Okay.

**[00:16:35] Marcus Delgado:** Sorry, while we're on Gary. HR's going to ask me to borrow him for the driver recruiting thing again.

**[00:16:44] Linda Brandt:** Oh, not that again.

**[00:16:47] Marcus Delgado:** We hire about four hundred drivers a year to keep the trucks filled. Recruiting's drowning in applications and DOT paperwork, and they think DART should do it. It shouldn't.

**[00:17:02] Maya Okafor:** I'll add it to the page.

**[00:17:05] Linda Brandt:** Everything's going on the page.

**[00:17:10] Maya Okafor:** It's a big page.

**[00:17:12] Linda Brandt:** Ha. Okay. Let me tell you where I am. I'm not going to the board with five-fifty today. I'll approve a two-week assessment, fixed fee, if the SOW says what you just said. Deliverables, a firm price, and nothing that auto-renews into a bigger engagement.

**[00:17:38] Maya Okafor:** That's exactly how we'd write it.

**[00:17:41] Linda Brandt:** And if the readout's good, Marcus and I take a phase one to the board on the ninth. With a stop point.

**[00:17:51] Marcus Delgado:** That works for me.

**[00:17:54] Maya Okafor:** Okay. Let me lay out next steps and you tell me if I've got it. One, we send the SOW for the two-week assessment by Thursday. Fixed fee, firmed up once Dev sees the repo, and the deliverables: code map of tendering, a line-haul driver pay spec, a security scan, a phased plan with costs and stop points, and a one-page AI view for the board.

**[00:18:28] Linda Brandt:** And the data handling.

**[00:18:31] Maya Okafor:** And the data handling, in writing. Two, Marcus, your legal team turns the NDA, and Gary gives Dev read access to TFS or an export.

**[00:18:44] Marcus Delgado:** Legal has the NDA already. I'll push them.

**[00:18:48] Maya Okafor:** Three, kickoff the week of November ninth with a ninety-minute working session with Gary. Readout by November twentieth.

**[00:18:58] Dev Patel:** I've held the time. I'll send Gary an agenda this week so he isn't walking in cold.

**[00:19:05] Maya Okafor:** Four, after the readout, a session with Pat before the board pack's due on the second. Linda, would you want to be in that?

**[00:19:17] Linda Brandt:** Yes. I'll want to see the readout before Pat does.

**[00:19:23] Maya Okafor:** Of course. We'll walk you and Marcus through it first.

**[00:19:27] Linda Brandt:** Good.

**[00:19:28] Maya Okafor:** And I'll pull together a short reference call with the insurance client, if you'd find that useful. They had a failed rewrite too. Their CFO might be the right person for you to talk to.

**[00:19:44] Linda Brandt:** That would actually be very useful. CFO to CFO.

**[00:19:50] Maya Okafor:** I'll ask them this week.

**[00:19:53] Marcus Delgado:** Oh, one thing. Linda, can I mention the, the Midwest thing?

**[00:20:00] Linda Brandt:** Carefully.

**[00:20:03] Marcus Delgado:** The fleet I mentioned last time. It's further along. About two hundred trucks, on a different TMS. If it closes, it'd be mid-next year, and whatever phase one is, they'd need to plug into it.

**[00:20:21] Dev Patel:** That's fine. API-first is built for that. I'll call it out in the plan without naming anyone.

**[00:20:30] Linda Brandt:** Please don't name anyone.

**[00:20:33] Dev Patel:** I won't.

**[00:20:36] Linda Brandt:** Okay. I need to jump. Maya, Dev, thank you. That was more concrete than I expected.

**[00:20:46] Maya Okafor:** Thanks, Linda. You'll have the SOW Thursday.

*[Linda Brandt left the meeting at 00:20:51]*

**[00:20:56] Marcus Delgado:** So. That went well, right?

**[00:21:00] Maya Okafor:** That went really well. She told us exactly what she needs. That's the best kind of skeptic.

**[00:21:08] Marcus Delgado:** She liked "stop point." I could see it. She wrote it down.

**[00:21:16] Dev Patel:** It's the thing the last group didn't give her.

**[00:21:20] Marcus Delgado:** Yeah. Okay. Thursday. I'll tell Gary to clear the week of the ninth.

**[00:21:27] Maya Okafor:** Perfect. Talk soon, Marcus.

**[00:21:30] Marcus Delgado:** Talk soon.

*[Meeting ended at 00:21:34]*
