# Discovery Call: Whitfield & Crane LLP x Scope Creepers

- **Category:** sales-discovery
- **Date:** 2026-09-22
- **Duration:** 21 min
- **Platform:** Zoom
- **Call type:** Discovery call 1 of 3 (prospect)

## Attendees

| Name | Company | Role |
|---|---|---|
| Maya Okafor | Scope Creepers | Partner / Account Executive |
| Dev Patel | Scope Creepers | Principal Solutions Engineer |
| Eleanor Vance-Hughes | Whitfield & Crane LLP | Chief Knowledge Officer |
| Priya Raman | Whitfield & Crane LLP | Director of Innovation |

---

## Transcript

**[00:00:07] Eleanor Vance-Hughes:** Good afternoon. Can everyone hear me? I'm in one of our phone booths, they're not very soundproof.

**[00:00:15] Maya Okafor:** You sound great. Hi Eleanor, hi Priya. Thanks for making the time.

**[00:00:22] Priya Raman:** Hi! And hi Dev, we met at the legal tech meetup in Chicago, I think?

**[00:00:29] Dev Patel:** We did! You asked the hard question about retrieval evaluation. I remember.

**[00:00:37] Priya Raman:** Ha. That's my brand.

**[00:00:41] Maya Okafor:** Well, that's a good sign for today. So, I'd love to just understand what's going on at Whitfield & Crane, and what made you want to talk. Eleanor, maybe you start?

**[00:00:55] Eleanor Vance-Hughes:** Sure. So, the firm has, um, three hundred and six lawyers as of this month. Eight practice groups. Our biggest are M&A, commercial contracts, real estate, and litigation. We have about forty years of work product in our document management system. NetDocuments. Something like eleven million documents.

**[00:01:25] Dev Patel:** Eleven million.

**[00:01:27] Eleanor Vance-Hughes:** Eleven million. Of which, maybe four percent is properly curated as precedent. My team, there are six of us, maintains a precedent bank of about nine thousand model documents and clauses. But it's always out of date, and lawyers don't use it. They email each other. "Does anyone have a good earnout clause for a pharma deal?" That email goes to the whole M&A group about twice a week.

**[00:02:09] Maya Okafor:** Ha. The "does anyone have" email.

**[00:02:13] Eleanor Vance-Hughes:** The "does anyone have" email. I've been fighting it for nine years.

**[00:02:21] Priya Raman:** We actually counted. In Q2, there were about three hundred and forty of those across the firm.

**[00:02:29] Dev Patel:** And how long does it take someone to find a good precedent today, without the email?

**[00:02:37] Eleanor Vance-Hughes:** For a senior associate, searching NetDocuments, maybe forty-five minutes to an hour to find something they trust. For a junior, they often can't find it at all, and they draft from scratch, which then gets marked up heavily by a senior. And clients increasingly won't pay for that.

**[00:03:07] Dev Patel:** Is there any search on NetDocuments today?

**[00:03:13] Eleanor Vance-Hughes:** Keyword search. Which is fine if you know the exact term. Useless if you're looking for "an indemnity cap that carves out data breaches" and the document says "limitation of liability shall not apply to losses arising from unauthorized access."

**[00:03:40] Dev Patel:** Right. That's exactly the gap semantic search fills. It matches on meaning rather than the literal words.

**[00:03:49] Eleanor Vance-Hughes:** Here's my worry, though. Ethical walls. We have, at any given time, two hundred-plus active ethical walls. Lawyers who can't see certain matters because of conflicts. If a search tool surfaces a document from a walled matter to the wrong lawyer, that's a disqualification motion. That's career-ending for someone.

**[00:04:23] Dev Patel:** Yes. That's the most important technical requirement in the whole thing. The search has to respect NetDocuments permissions exactly, at query time. Not a copy of the permissions from last week. Live.

**[00:04:41] Eleanor Vance-Hughes:** How would you prove that to me?

**[00:04:46] Dev Patel:** We'd set up test users on both sides of real walls, with your IT team, and try to break it. Thousands of queries, adversarially. And we'd log every retrieval for audit, so you can always answer "who saw what, and when."

**[00:05:06] Eleanor Vance-Hughes:** Okay. I'd want to see that test plan in writing at some point.

**[00:05:12] Dev Patel:** Of course.

**[00:05:14] Maya Okafor:** And confidentiality more broadly. Where the data lives, who can see it?

**[00:05:20] Eleanor Vance-Hughes:** That's the other half of it. Our clients trust us with the most sensitive information they have. Deal terms before they're public. Litigation strategy. I will not put that into somebody's shared cloud and hope.

**[00:05:40] Maya Okafor:** That's a design requirement for us, not an afterthought. The short version is client data stays in a deployment you control, nothing is used to train a model, and every answer cites the source document so a lawyer can check it.

**[00:06:01] Eleanor Vance-Hughes:** I've heard that sentence before.

**[00:06:04] Maya Okafor:** I'm sure you have. That's why we'd rather show you than tell you.

**[00:06:10] Priya Raman:** We've had another vendor in touch, and they said, word for word, more or less, the same thing.

**[00:06:17] Maya Okafor:** That's fair. Can I ask how that's going?

**[00:06:22] Priya Raman:** Early. They've been very keen.

**[00:06:26] Eleanor Vance-Hughes:** Very keen. Honestly, my impression was a black box. I asked how it decided which precedents were relevant and nobody could tell me. And they wanted all our documents in their cloud.

**[00:06:42] Priya Raman:** To be fair, the contract review part looked pretty good.

**[00:06:48] Eleanor Vance-Hughes:** It looked good on their demo documents.

**[00:06:51] Priya Raman:** That's fair.

**[00:06:54] Maya Okafor:** Let's talk about contract review then, Priya. That sounds like more your area.

**[00:07:01] Priya Raman:** Yes. So, our commercial contracts and M&A groups do a lot of first-pass review. Diligence on deals, reviewing a target's contracts. On a mid-size deal, it might be eight hundred to fifteen hundred contracts. We staff it with juniors and contract attorneys. A typical diligence review is, uh, around two thousand hours of attorney time. And honestly, the quality varies wildly, because it's hour twelve of a review and people are tired.

**[00:07:51] Dev Patel:** What are they looking for, usually? Change of control, assignment, exclusivity, that kind of thing?

**[00:08:00] Priya Raman:** Exactly. Change of control, assignment, termination rights, MFN, exclusivity, non-competes, IP ownership, the usual. And then a summary memo for the partner.

**[00:08:15] Maya Okafor:** And is that billed hourly or fixed?

**[00:08:19] Priya Raman:** More and more, fixed. Which is why I care. On a fixed-fee diligence, every hour we save is ours. On the last big one, a medical device acquisition, we were thirty percent over our internal budget. We ate that.

**[00:08:41] Eleanor Vance-Hughes:** And the partner on that deal is still upset about it.

**[00:08:45] Priya Raman:** Still upset.

**[00:08:49] Dev Patel:** How do they capture the output today? Spreadsheet?

**[00:08:53] Priya Raman:** A giant spreadsheet. One row per contract, one column per issue. Then someone senior spot-checks maybe five percent of it, and the rest goes into the memo on trust.

**[00:09:09] Dev Patel:** That's actually a nice shape for us. If the model fills in the same grid, with a link to the clause it's relying on for each cell, your senior can check far more than five percent in the same time.

**[00:09:26] Priya Raman:** That's what I want. I want to check the machine, not trust it.

**[00:09:31] Maya Okafor:** And is there an outward-facing version of this? Reviewing third-party paper for clients?

**[00:09:38] Priya Raman:** I'd love it to be. Some of our corporate clients have playbooks, like, "we never accept unlimited indemnity," and we review their vendor contracts against them. A retail client sends us, maybe, sixty vendor agreements a month.

**[00:09:57] Eleanor Vance-Hughes:** Priya, that's a different use case. Let's stay focused.

**[00:10:02] Priya Raman:** It's the same technology.

**[00:10:04] Eleanor Vance-Hughes:** Same technology, different client relationship, different risk profile. If we get that wrong, it's a client's contract, not our own internal work.

**[00:10:17] Priya Raman:** Fine. Someday.

**[00:10:20] Maya Okafor:** I'll write it down as "someday." Eleanor, you said earlier there's one thing that keeps you up at night?

**[00:10:28] Eleanor Vance-Hughes:** Citations. Contract review is internal work product. It gets reviewed. But you've seen the stories, lawyers filing briefs with cases that don't exist. If a tool we've deployed ever invents a case, or invents a clause and says it came from one of our precedents, we're in the news. How do you prevent that?

**[00:10:56] Dev Patel:** So, honestly, the safest answer is the system shouldn't generate citations from the model's own memory at all. Anything it cites has to come from a retrieved document, from your DMS or a licensed source, and it shows you the passage. If there's no source, there's no citation. And we'd add an automated check that verifies every citation against the source before the lawyer even sees the answer.

**[00:11:34] Eleanor Vance-Hughes:** Can you guarantee it?

**[00:11:38] Dev Patel:** Guarantee, no. I'd be lying. What I can say is we can design it so that an unverified citation is visibly flagged, and we measure the rate during any pilot. And the lawyer still has the professional obligation to check. That doesn't go away.

**[00:12:02] Eleanor Vance-Hughes:** I appreciate you not saying yes.

**[00:12:05] Priya Raman:** The other folks said yes.

**[00:12:08] Eleanor Vance-Hughes:** I know they did. That's partly why we're talking to you.

**[00:12:14] Maya Okafor:** Good to know. And on the knowledge side, Eleanor, what does "good" look like, if it worked?

**[00:12:21] Eleanor Vance-Hughes:** Zero wall breaches. Non-negotiable. Then, honestly, I want the "does anyone have" emails to drop. If they dropped by half in one group, I'd be thrilled. And time to find a trusted precedent, under ten minutes.

**[00:12:43] Priya Raman:** For diligence, I'd say hours per contract down by at least forty percent, with equal or better accuracy on a sample checked by a senior associate.

**[00:12:56] Dev Patel:** Those are good. Measurable, which is rare at this stage.

**[00:13:02] Maya Okafor:** Can I ask about the people who'd use it? Is everyone in one office?

**[00:13:07] Eleanor Vance-Hughes:** Mostly here. There's London, thirty lawyers, but they're, um, they're always the last to hear about anything. If this went well they'd want it eventually, and then we'd have UK data rules to think about. But not now.

**[00:13:27] Dev Patel:** Good to know early, though. It changes where you'd want things hosted.

**[00:13:32] Eleanor Vance-Hughes:** Mm. Fair.

**[00:13:35] Maya Okafor:** And who internally would we need to bring along? IT, security?

**[00:13:41] Priya Raman:** Our CIO, Greg Lyons. He's supportive but he's going to want to know what this does to his team. They're small, and they're in the middle of moving NetDocuments to a new cloud tenant.

**[00:13:57] Dev Patel:** Oh, you're mid-migration? When does that finish?

**[00:14:01] Priya Raman:** January, supposedly.

**[00:14:05] Dev Patel:** That's actually useful. We'd want to build on the new tenant, not the old one.

**[00:14:11] Eleanor Vance-Hughes:** And Martin Feld, our general counsel, would need to sign off on anything touching client confidentiality.

**[00:14:20] Maya Okafor:** Understood. And on the decision itself, how does something like this get made at the firm?

**[00:14:28] Eleanor Vance-Hughes:** Honestly, it's with me. Knowledge management is my budget line. Precedent, search, the DMS content, that's my remit. I'll keep Jonathan, our managing partner, informed, of course, and Priya and I work on this together. But this is a knowledge decision, and I'll make it.

**[00:14:56] Maya Okafor:** That's helpful. So you're the person we need to convince.

**[00:15:00] Eleanor Vance-Hughes:** I'm the person you need to convince.

**[00:15:04] Priya Raman:** And I'm the person who'll be annoying about the evaluation.

**[00:15:08] Dev Patel:** Ha. We'll take it.

**[00:15:11] Maya Okafor:** Is there a rough sense of when you'd want to have something running? Or is it too early?

**[00:15:18] Eleanor Vance-Hughes:** Too early to say, really. I want to understand what's possible first. I don't want a date driving a bad decision.

**[00:15:28] Maya Okafor:** That's fair. And I won't push on budget today either. Let's figure out whether we're the right fit first.

**[00:15:35] Eleanor Vance-Hughes:** Thank you. I'd rather that.

**[00:15:38] Dev Patel:** Can I ask a couple of technical things while I have you both?

**[00:15:43] Eleanor Vance-Hughes:** Go ahead.

**[00:15:45] Dev Patel:** How is the DMS organised? By client and matter?

**[00:15:49] Eleanor Vance-Hughes:** Client, matter, then folders the lawyers make up as they go. So there's structure at the top and chaos underneath. Document types are tagged, sort of. Maybe sixty percent accurately.

**[00:16:06] Dev Patel:** That's typical. And the precedent bank, is that inside NetDocuments too?

**[00:16:11] Eleanor Vance-Hughes:** Yes, a separate cabinet. With its own permissions, which are broader. Anyone at the firm can see the precedent bank.

**[00:16:21] Dev Patel:** Good. That's a natural place to start testing, since the wall risk is lower, and then expand into the matter workspaces once the permission enforcement is proven.

**[00:16:34] Eleanor Vance-Hughes:** I like that sequencing.

**[00:16:37] Priya Raman:** Can I ask one? How do you evaluate retrieval quality? Since that's my brand.

**[00:16:44] Dev Patel:** Ha. So, we'd build a test set with your knowledge team. A few hundred real questions lawyers have asked, the "does anyone have" emails are perfect for this actually, and the documents a senior lawyer would have pointed to. Then we measure whether the right documents come back in the top few results. Before and after every change.

**[00:17:13] Priya Raman:** Oh, using the emails is clever.

**[00:17:17] Eleanor Vance-Hughes:** That's the first good use anyone's found for them.

**[00:17:21] Maya Okafor:** Ha. Outside of search and review, I'm curious, where else is the firm feeling pressure? Just so we understand the bigger picture.

**[00:17:31] Priya Raman:** Oh, everywhere. Business development is a big one. Our marketing and BD team writes, I think, around two hundred RFP responses a year, for panel appointments with corporate clients. Every one is a scramble for lawyer bios, matter experience, diversity stats. It's mostly copy-paste from old RFPs.

**[00:18:00] Eleanor Vance-Hughes:** And they constantly ask Knowledge for "matters we've done like this." Which, our experience database is, um, bad.

**[00:18:10] Maya Okafor:** That sounds like the same search problem with a different audience.

**[00:18:14] Eleanor Vance-Hughes:** It is, a bit. But let's not get ahead of ourselves.

**[00:18:19] Maya Okafor:** Noted. Not today's scope.

**[00:18:22] Dev Patel:** One more practical thing. Would it be possible to see some real examples of what you work with? Even non-confidential?

**[00:18:30] Eleanor Vance-Hughes:** I can get you a sample of precedents, the public ones, things we've published or that are in the public record, so you can see what we're working with before anything confidential.

**[00:18:43] Dev Patel:** That'd be great.

**[00:18:45] Priya Raman:** And I can share a redacted version of a diligence spreadsheet. Just the column headings and a few made-up rows.

**[00:18:53] Dev Patel:** Perfect. That's enough to show you what the output would look like.

**[00:18:57] Eleanor Vance-Hughes:** I do have to go in a few minutes. Can we talk next steps?

**[00:19:01] Maya Okafor:** Of course. So here's what I'm hearing. Two needs. One, knowledge search across forty years of work product in NetDocuments, where live ethical-wall enforcement is non-negotiable. Two, first-pass contract review for diligence, where the output is the issue grid with a source link on every answer. Underneath both: client confidentiality, and no invented citations, ever, with anything unverified flagged. Eleanor, you own the decision. Priya, you own how we measure it.

**[00:19:46] Priya Raman:** Yes.

**[00:19:48] Eleanor Vance-Hughes:** Yes. That's a fair summary.

**[00:19:51] Maya Okafor:** From our side, we'll send a short write-up of that, plus an outline of how we'd approach the wall testing. Dev, you'll do that part?

**[00:20:01] Dev Patel:** Yes. A rough test plan. And I'll put together a short demo on the public precedents once Eleanor sends them, so you can see semantic search on your own kind of documents rather than ours.

**[00:20:16] Eleanor Vance-Hughes:** That would be much more convincing.

**[00:20:20] Maya Okafor:** And I'll try to dig up a reference from another firm that's done something similar, if they're willing to talk. No promises, law firms are shy.

**[00:20:31] Priya Raman:** Ha. We are.

**[00:20:33] Maya Okafor:** Shall we find a time for a follow-up in a few weeks, once you've seen the demo?

**[00:20:38] Eleanor Vance-Hughes:** Yes. Priya, can you sort out a time? Mid-October, probably.

**[00:20:44] Priya Raman:** I'll send something.

**[00:20:46] Eleanor Vance-Hughes:** Alright. Thank you both. This was more substantive than I expected, honestly.

**[00:20:52] Maya Okafor:** Thank you, Eleanor. Thank you, Priya. Talk soon.

**[00:20:57] Dev Patel:** Thanks, everyone.

*[Meeting ended at 00:21:00]*
