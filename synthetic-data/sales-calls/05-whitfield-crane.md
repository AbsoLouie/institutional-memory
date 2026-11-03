# Discovery Call: Whitfield & Crane LLP x Scope Creepers

- **Category:** sales-discovery
- **Date:** 2026-10-28
- **Duration:** 32 min
- **Platform:** Zoom
- **Call type:** First discovery call (prospect)

## Attendees

| Name | Company | Role |
|---|---|---|
| Maya Okafor | Scope Creepers | Partner / Account Executive |
| Dev Patel | Scope Creepers | Principal Solutions Engineer |
| Eleanor Vance-Hughes | Whitfield & Crane LLP | Chief Knowledge Officer |
| Jonathan Crane | Whitfield & Crane LLP | Managing Partner (00:00 – ~00:07) |
| Priya Raman | Whitfield & Crane LLP | Director of Innovation |

---

## Transcript

**[00:00:07] Eleanor Vance-Hughes:** Good afternoon. I think we're all here. Jonathan, can you hear?

**[00:00:15] Jonathan Crane:** I can. I have about ten minutes, I'm afraid. I'm between a client call and a partners' lunch.

**[00:00:25] Maya Okafor:** Thank you for squeezing us in, Jonathan. We'll make it worth it. Hi Eleanor, hi Priya.

**[00:00:35] Priya Raman:** Hi! Hi Dev, we met at the legal tech meetup in Chicago, I think?

**[00:00:42] Dev Patel:** We did! You asked the hard question about retrieval evaluation. I remember.

**[00:00:50] Priya Raman:** Ha. That's my brand.

**[00:00:54] Maya Okafor:** Jonathan, since you're short on time, maybe I'll start with you. What do you want out of this, from where you sit?

**[00:01:06] Jonathan Crane:** Well. I'll be candid. I'm not sure we need this. I'm here because Eleanor and Priya think we do, and I trust them. My concerns are three. Confidentiality, first and foremost. Our clients trust us with the most sensitive information they have. Second, accuracy. You've seen the stories about lawyers filing briefs with fabricated citations. That cannot happen here. Ever. And third, frankly, economics. We're a law firm. We sell time. If a tool makes an associate twice as fast, I need to understand what that does to the firm.

**[00:02:06] Maya Okafor:** Those are exactly the right three. Can I ask about the third one, since it's the one people talk about least?

**[00:02:16] Jonathan Crane:** Please.

**[00:02:18] Maya Okafor:** Are your clients pushing on fees? Alternative fee arrangements?

**[00:02:26] Jonathan Crane:** Increasingly. About, I'd say, a quarter of our revenue is now under some form of fixed or capped fee. Mostly in the M&A and commercial contracts practices. Several of our largest clients' general counsels have told us, explicitly, that they expect AI efficiencies to show up in their bills.

**[00:02:57] Maya Okafor:** So on that quarter of the business, efficiency is margin.

**[00:03:03] Jonathan Crane:** On that quarter, yes. On the hourly work, it's more complicated.

**[00:03:11] Priya Raman:** And on the hourly work, the clients are refusing to pay for first-year associate time on routine review anyway. We wrote off, Jonathan, what was the number?

**[00:03:24] Jonathan Crane:** Write-downs on junior associate time were around three point eight million last year. I don't love that number.

**[00:03:36] Priya Raman:** So we're already not getting paid for it.

**[00:03:40] Jonathan Crane:** Priya's made this argument to me several times.

**[00:03:46] Priya Raman:** I'll keep making it.

**[00:03:50] Maya Okafor:** That's a really useful frame. And Jonathan, on confidentiality and accuracy, those are design requirements for us, not afterthoughts. Dev can go into it, but the short version: client data stays in a deployment you control, no training on your data, and every answer cites the source document so a lawyer can verify it. Nothing is presented as authority without a link to the actual text.

**[00:04:31] Jonathan Crane:** The other vendor said the same things.

**[00:04:36] Maya Okafor:** Which vendor, if I can ask?

**[00:04:40] Eleanor Vance-Hughes:** Lexwright. They presented to the technology committee in September.

**[00:04:48] Jonathan Crane:** It was a polished presentation. Very confident.

**[00:04:54] Maya Okafor:** What did you think of it?

**[00:04:58] Jonathan Crane:** I thought it was a product looking for a law firm. Eleanor, you were less charitable.

**[00:05:08] Eleanor Vance-Hughes:** I thought it was a black box. They couldn't tell me how it decided which precedents were relevant. And they wanted all our documents in their cloud.

**[00:05:23] Priya Raman:** To be fair, the contract review module was pretty good. I'd say that's a real option.

**[00:05:33] Eleanor Vance-Hughes:** It was good on their demo documents.

**[00:05:37] Priya Raman:** That's fair.

**[00:05:41] Jonathan Crane:** I'm going to have to go shortly. Let me just say: whatever you propose, I want it piloted with one practice group, measured honestly, and I want the general counsel's office, our own GC, Martin Feld, to sign off on the confidentiality piece. If those things happen, I'm open-minded. More than I sound.

**[00:06:12] Maya Okafor:** That's a clear bar. Thank you.

**[00:06:16] Jonathan Crane:** And, ah, one more. If this goes well, our London office will want it. They're thirty lawyers and they're always the last to hear about anything. Make sure whatever you do works under UK data rules too.

**[00:06:37] Maya Okafor:** Noted. Very helpful.

**[00:06:41] Jonathan Crane:** Good. Eleanor, Priya, I'll see you at lunch. Nice to meet you both.

**[00:06:49] Dev Patel:** Thanks, Jonathan.

*[00:06:53 – Jonathan Crane left the meeting]*

**[00:06:59] Priya Raman:** So that's Jonathan.

**[00:07:03] Eleanor Vance-Hughes:** That was actually a good outcome. He said "open-minded."

**[00:07:09] Priya Raman:** He did say open-minded.

**[00:07:12] Maya Okafor:** Ha. Okay. So, let's get into the substance. Eleanor, you're CKO, so I'm guessing the knowledge search piece is closest to you?

**[00:07:26] Eleanor Vance-Hughes:** Yes. So, the firm has, um, three hundred and six lawyers as of this month. Eight practice groups. Our biggest are M&A, commercial contracts, real estate, and litigation. We have about forty years of work product in our document management system. NetDocuments. Something like eleven million documents.

**[00:08:01] Dev Patel:** Eleven million.

**[00:08:03] Eleanor Vance-Hughes:** Eleven million. Of which, maybe four percent is properly curated as precedent. My team, there are six of us, maintains a precedent bank of about nine thousand model documents and clauses. But it's always out of date, and lawyers don't use it. They email each other. "Does anyone have a good earnout clause for a pharma deal?" That email goes to the whole M&A group about twice a week.

**[00:08:46] Maya Okafor:** Ha. The "does anyone have" email.

**[00:08:50] Eleanor Vance-Hughes:** The "does anyone have" email. I've been fighting it for nine years.

**[00:08:58] Priya Raman:** We actually counted. In Q2, there were about three hundred and forty of those across the firm.

**[00:09:07] Dev Patel:** And how long does it take someone to find a good precedent today, without the email?

**[00:09:15] Eleanor Vance-Hughes:** For a senior associate, searching NetDocuments, maybe forty-five minutes to an hour to find something they trust. For a junior, they often can't find it at all, and they draft from scratch, which then gets marked up heavily by a senior. That's where the write-downs come from.

**[00:09:45] Dev Patel:** Is there any search on NetDocuments today?

**[00:09:50] Eleanor Vance-Hughes:** Keyword search. Which is fine if you know the exact term. Useless if you're looking for "an indemnity cap that carves out data breaches" and the document says "limitation of liability shall not apply to losses arising from unauthorized access."

**[00:10:16] Dev Patel:** Right. That's exactly the gap semantic search fills.

**[00:10:22] Eleanor Vance-Hughes:** Here's my worry, though. Ethical walls. We have, at any given time, two hundred-plus active ethical walls. Lawyers who can't see certain matters because of conflicts. If a search tool surfaces a document from a walled matter to the wrong lawyer, that's a disqualification motion. That's career-ending for someone.

**[00:10:57] Dev Patel:** Yes. That's the most important technical requirement in the whole thing. The search has to respect NetDocuments permissions exactly, at query time. Not a copy of the permissions from last week. Live. We'd test it specifically, adversarially, before anyone uses it.

**[00:11:24] Eleanor Vance-Hughes:** How would you test it?

**[00:11:28] Dev Patel:** We'd set up test users on both sides of real walls, with your IT team, and try to break it. Thousands of queries. And we'd log every retrieval for audit.

**[00:11:43] Eleanor Vance-Hughes:** Okay. I'd want to see that test plan in writing.

**[00:11:49] Dev Patel:** Of course.

**[00:11:51] Maya Okafor:** Priya, what about contract review? That sounds like more your area.

**[00:11:59] Priya Raman:** Yes. So, our commercial contracts and M&A groups do a lot of first-pass review. Diligence on deals, reviewing a target's contracts. On a mid-size deal, it might be eight hundred to fifteen hundred contracts. We staff it with juniors and contract attorneys. A typical diligence review is, uh, around two thousand hours of attorney time. And honestly, the quality varies wildly, because it's hour twelve of a review and people are tired.

**[00:12:48] Dev Patel:** What are they looking for, usually? Change of control, assignment, exclusivity, that kind of thing?

**[00:12:58] Priya Raman:** Exactly. Change of control, assignment, termination rights, MFN, exclusivity, non-competes, IP ownership, the usual. And then a summary memo.

**[00:13:13] Maya Okafor:** And on the client side, is that billed hourly or fixed?

**[00:13:19] Priya Raman:** Increasingly fixed. Which is why I care. On a fixed-fee diligence, every hour we save is ours. On the last big one, a medical device acquisition, we were thirty percent over our internal budget. We ate that.

**[00:13:42] Eleanor Vance-Hughes:** And the partner on that deal is still upset about it.

**[00:13:48] Priya Raman:** Still upset.

**[00:13:52] Maya Okafor:** And the other side. Drafting and negotiating against counterparty paper, is that part of this too?

**[00:14:02] Priya Raman:** I'd love it to be. Reviewing third-party paper against our clients' playbooks. Some of our corporate clients have playbooks, like, "we never accept unlimited indemnity," and we review their vendor contracts for them. That's a lot of volume. A retail client sends us, maybe, sixty vendor agreements a month.

**[00:14:33] Eleanor Vance-Hughes:** Priya, that's a different use case. Let's stay focused.

**[00:14:39] Priya Raman:** It's the same technology.

**[00:14:41] Eleanor Vance-Hughes:** It's the same technology, but it's a different client relationship, and a different risk profile. If we get that wrong, it's a client's contract, not our own internal work.

**[00:14:57] Priya Raman:** Fine. Phase two.

**[00:15:00] Maya Okafor:** I'll note it as a phase two. Can I ask about the Lexwright comparison more directly? Where are you in that process?

**[00:15:12] Priya Raman:** They've sent a proposal. Per-seat license, three-year term. It's, uh, it's a lot. And they want a firm-wide commitment, not a pilot.

**[00:15:28] Eleanor Vance-Hughes:** Which I find telling.

**[00:15:32] Priya Raman:** They'd do a sixty-day pilot. But with a commitment to buy at the end, unless we can show it "materially failed."

**[00:15:43] Dev Patel:** That's a pretty aggressive structure.

**[00:15:47] Priya Raman:** It is. Their argument is that they have a legal-specific model and a team of lawyers who built their review templates. Which, that is a real advantage.

**[00:16:03] Dev Patel:** It's a real advantage for standard review. Where it's weaker, usually, is your own precedent. A vendor product doesn't know Whitfield & Crane's forty years of work, and it's not going to work with your ethical walls the way you need. Honestly, it might not be either/or. Some firms use a vendor tool for first-pass diligence and build their own for knowledge search.

**[00:16:40] Eleanor Vance-Hughes:** That's interesting. That's actually where I've been landing.

**[00:16:46] Priya Raman:** I'd want to see that compared, honestly. Like an actual test. Same contracts, both tools.

**[00:16:55] Maya Okafor:** That's a reasonable ask. We could set that up as part of a pilot.

**[00:17:01] Eleanor Vance-Hughes:** Can I raise the citation issue? Because this is the one that keeps me up at night.

**[00:17:09] Maya Okafor:** Please.

**[00:17:11] Eleanor Vance-Hughes:** Contract review is internal work product. It gets reviewed. But if we ever extend this to research, case law, which people will want to, the moment someone cites a case that doesn't exist in a brief, we're in the news. How do you prevent that?

**[00:17:36] Dev Patel:** So, honestly, the safest answer is: the system shouldn't generate case citations at all from the model's own memory. Anything it cites has to come from a retrieved document, from your DMS or a licensed research database, and it shows you the source passage. If there's no source, there's no citation. And we'd want a verification step, automated, that checks every citation against the source before the lawyer even sees it.

**[00:18:19] Eleanor Vance-Hughes:** Can you guarantee it?

**[00:18:23] Dev Patel:** Guarantee, no. I'd be lying. What I can say is we can design it so that an unverified citation is visibly flagged, and we measure the rate during the pilot. And the lawyer still has the professional obligation to check. That doesn't go away.

**[00:18:49] Eleanor Vance-Hughes:** I appreciate you not saying yes.

**[00:18:52] Priya Raman:** Lexwright said yes.

**[00:18:56] Eleanor Vance-Hughes:** I know they did.

**[00:19:00] Maya Okafor:** Is research in scope for now, or later?

**[00:19:06] Eleanor Vance-Hughes:** Later. Much later. Our litigation group would want to be involved, and the head of litigation, Sam Okonjo, is, um, a skeptic.

**[00:19:22] Priya Raman:** He's more than a skeptic.

**[00:19:26] Eleanor Vance-Hughes:** He's a skeptic with a lot of influence.

**[00:19:30] Maya Okafor:** Okay. Understood. Let's talk about the decision. Who's involved, and what's the process?

**[00:19:39] Eleanor Vance-Hughes:** The technology committee makes a recommendation to the management committee. Jonathan chairs management. Technology committee meets monthly, next one is November eighteenth. Then Martin, our GC, for confidentiality, and IT security.

**[00:20:05] Priya Raman:** And the CIO, Greg Lyons. He's supportive but he's going to want to know what this does to his team. They're small and they're already managing the NetDocuments migration to the new cloud tenant.

**[00:20:24] Dev Patel:** Oh, you're mid-migration?

**[00:20:28] Priya Raman:** Finishing in January.

**[00:20:30] Dev Patel:** That's actually good timing. We'd want to build on the new tenant, not the old one.

**[00:20:38] Maya Okafor:** Budget. Is there a number, or a range?

**[00:20:44] Priya Raman:** I have an innovation budget. It's not huge. About two hundred and fifty thousand for this fiscal year, which ends January thirty-first. Some of that is committed already.

**[00:21:01] Eleanor Vance-Hughes:** And Knowledge has a budget that, um, I can redirect if this replaces some of what we spend on manual precedent curation. We pay for two contract paralegals, basically for precedent maintenance.

**[00:21:21] Maya Okafor:** So the pilot could be funded this fiscal year, and if it works, the scale-up is a next-year conversation with management.

**[00:21:30] Priya Raman:** That's the plan. And honestly, Lexwright's pricing is a useful anchor. Whatever we propose to management has to look reasonable against their three-year number.

**[00:21:46] Maya Okafor:** Can you share it?

**[00:21:50] Priya Raman:** Not the document. But it's north of a million over three years.

**[00:21:56] Maya Okafor:** Okay. That's helpful.

**[00:22:00] Dev Patel:** Can I ask about the pilot group? Which practice?

**[00:22:06] Eleanor Vance-Hughes:** Commercial contracts. Smaller, about thirty-five lawyers, and the practice leader, Diane Ferris, is enthusiastic. She's been asking me for a year.

**[00:22:21] Priya Raman:** M&A would be a better test. The diligence volume is there.

**[00:22:27] Eleanor Vance-Hughes:** M&A is also where the partners are most resistant, and if the pilot fails in M&A, it's dead firm-wide.

**[00:22:39] Priya Raman:** And if it succeeds in M&A, it's alive firm-wide.

**[00:22:45] Eleanor Vance-Hughes:** Priya.

**[00:22:46] Priya Raman:** I'm just saying.

**[00:22:50] Maya Okafor:** Could it be both, staged? Knowledge search with commercial contracts first, since Diane's a champion and the walls issue can be tested in a smaller group, and then a diligence review pilot on one M&A deal, with a willing partner?

**[00:23:16] Eleanor Vance-Hughes:** Hm. That could work.

**[00:23:20] Priya Raman:** There's a partner in M&A, Ken Abernathy, who'd probably volunteer. He's got a deal coming in Q1 that's going to be mostly fixed fee.

**[00:23:33] Eleanor Vance-Hughes:** Ken would do it. Ken likes being first.

**[00:23:39] Maya Okafor:** Okay. That's a good structure.

**[00:23:43] Dev Patel:** For success criteria on knowledge search: what would you need to see?

**[00:23:51] Eleanor Vance-Hughes:** Zero wall breaches. Non-negotiable. Then, honestly, I want the "does anyone have" emails to drop. If they drop by half in commercial contracts, I'll be thrilled. And time to find a precedent, under ten minutes.

**[00:24:16] Priya Raman:** For diligence: hours per contract down by at least forty percent, with equal or better accuracy on a sample checked by a senior associate.

**[00:24:30] Dev Patel:** Those are good. Measurable.

**[00:24:34] Maya Okafor:** Outside of these two, I'm curious, where else is the firm feeling pressure? Just so we understand the bigger picture.

**[00:24:45] Priya Raman:** Oh, everywhere. Business development is huge. Our marketing and BD team writes, I think, around two hundred RFP responses a year, for panel appointments with corporate clients. Every one is a scramble for lawyer bios, matter experience, diversity stats. It's mostly copy-paste from old RFPs.

**[00:25:19] Eleanor Vance-Hughes:** And they constantly ask Knowledge for "matters we've done like this." Which, our experience database is, um, bad.

**[00:25:30] Priya Raman:** And conflicts. New business intake. The conflicts team runs every new matter, and it's very manual. Like, three or four days for a complex one, and partners are always angry about the delay.

**[00:25:50] Maya Okafor:** Conflicts is interesting, it's related to the walls problem.

**[00:25:56] Priya Raman:** And, uh, the billing side. Time entry narratives. Clients reject invoices because the narratives don't follow their outside counsel guidelines. Finance spends a lot of time on that. I think the rejection rate is like eleven percent on our top twenty clients.

**[00:26:21] Eleanor Vance-Hughes:** That's a finance problem, Priya.

**[00:26:25] Priya Raman:** Everything's my problem, I'm innovation.

**[00:26:29] Maya Okafor:** Ha. I'll keep a list. Not today's scope.

**[00:26:35] Eleanor Vance-Hughes:** Let's talk next steps. I need to go to that partners' lunch too.

**[00:26:42] Maya Okafor:** Of course. So here's what I'm hearing. A two-part pilot. Part one: precedent and knowledge search for commercial contracts, about thirty-five lawyers, built on the new NetDocuments tenant, with live ethical-wall enforcement and an adversarial wall test before anyone uses it. Part two: diligence review on one M&A deal with Ken, compared head-to-head against Lexwright on the same documents if you want that. Success measured on wall breaches, "does anyone have" email volume, time to find precedent, and hours per contract with accuracy checked by a senior associate. Funded from innovation and Knowledge budgets this fiscal year.

**[00:27:49] Priya Raman:** Yes.

**[00:27:51] Eleanor Vance-Hughes:** Yes. That's a fair summary.

**[00:27:55] Maya Okafor:** Next steps from our side. A written proposal, including Dev's ethical wall test plan, ahead of the technology committee on the eighteenth. When would you need it to get it on the agenda?

**[00:28:14] Eleanor Vance-Hughes:** By the eleventh. Committee papers go out a week before.

**[00:28:20] Maya Okafor:** Done. By the eleventh. We'll also send a short confidentiality and data handling memo for Martin, the GC.

**[00:28:32] Dev Patel:** And a one-page architecture showing where the data lives. Including what we'd do for London, under UK GDPR. I'll need to look into whether we'd want a separate UK deployment or not. I don't have a firm answer on that today.

**[00:28:53] Priya Raman:** Thanks. Jonathan will ask.

**[00:28:57] Maya Okafor:** And on the Lexwright comparison, I want to think about how we'd structure that fairly. If their pilot terms require a purchase commitment, running them side by side might be tricky for you. Let us think about it and come back.

**[00:29:18] Priya Raman:** That's fair. I'll find out if they'd do a no-commitment bake-off. I doubt it.

**[00:29:26] Eleanor Vance-Hughes:** From our side, I can get you a sample of precedents, the public ones, things we've published or that are already in the public record, so you can see what we're working with before anything confidential.

**[00:29:46] Dev Patel:** That'd be great.

**[00:29:48] Priya Raman:** And I'll set up a call with Greg Lyons, the CIO, and our IT security lead. Probably the week of November second.

**[00:29:59] Maya Okafor:** Perfect. And should we plan to meet Diane, the commercial contracts leader?

**[00:30:07] Eleanor Vance-Hughes:** Yes. After the committee, though. I don't want to get her hopes up before we have approval.

**[00:30:17] Maya Okafor:** Understood.

**[00:30:19] Priya Raman:** Oh, and Maya, one thing. If this goes well, the managing partners of a couple of other firms in our network, we're part of an international alliance of independent firms, about forty firms, they'll want to know what we did. There's a knowledge management working group I sit on.

**[00:30:46] Maya Okafor:** That's really kind of you to mention. Let's earn it first.

**[00:30:52] Priya Raman:** Ha. Obviously.

**[00:30:56] Eleanor Vance-Hughes:** Alright. Thank you both. This was more substantive than I expected, honestly.

**[00:31:04] Maya Okafor:** Thank you, Eleanor. Thank you, Priya. We'll be in touch with the proposal.

**[00:31:12] Dev Patel:** Thanks, everyone.

*[Meeting ended at 00:31:15]*
