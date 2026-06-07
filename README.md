# GoodCompany Ecosystem — Open Design Invitation

> v0.4 · Living document · Cardano / Midnight ecosystem

---

## Who is writing this

I'm Sander, a solo entrepreneur and freelancer based in the Netherlands. I'm not a developer. My ideas come from years of working independently and the frustrations that come with it — and I think that's exactly why this project ended up being bigger than most.

Because I don't think in terms of what's technically feasible, my creative boundaries sit much further out. Most projects on Cardano are designed by developers who already filter their ideas through implementation constraints. I don't have that filter. What I have instead is a clear memory of what it actually feels like to work as a freelancer — the trust problems, the payment risks, the lack of real protection — and a strong conviction that those problems deserve a serious solution.

I've been developing this ecosystem seriously for about two years. The ideas are solid. But this project is too large and too impactful to be shaped by one person alone. I'm looking for developers who want to think alongside me — not to implement a finished spec, but to help figure out what the right spec even is.

---

## Where this started

In 2018 I had a slow period at work and started asking myself a hypothetical: if I had unlimited resources, what would I build — something the whole world would notice? I ended up designing a professional platform from scratch. It had a reputation system, headhunting, job postings, and a job application module I was particularly proud of: you could break your work experience into specific skill blocks and send only the relevant ones to a recruiter, each accompanied by a short pre-recorded video. A developer friend looked at it and said *"it's like LinkedIn on steroids."*

Then I told my aunt about it. She was Head of HR at ING Global at the time. She liked the concept but pointed out a real problem: anti-discrimination law in the Netherlands and EU means recruiters cannot see who a candidate is at early stages. My reaction was that bias can enter at any point in a hiring process anyway — so the law doesn't really solve the problem. She agreed. But governments had decided, and that was that. It took the wind out of my sails.

In 2021 I encountered Cardano for the first time. The vision of Charles Hoskinson, the research-first approach, the community — it struck me as genuinely noble in a space that often isn't. Charles talks about the need for real-world use cases and meaningful adoption. I think that's precisely what this is: a project born not from blockchain enthusiasm, but from real frustrations that real workers face every day. Something clicked. Several ideas I'd been sitting on since 2018 could live inside this ecosystem — but with a completely different intent. Not building to extract value, but building something structurally beneficial to the people who use it. GoodCompany grew from there.

> What you're reading is the point where I've decided it needs more than one mind.

---

## What this is

GoodCompany started as a community-driven work and finance platform on Cardano. While building its internal governance — voting on treasury decisions, loan requests, community rules — I realised the same mechanism could do something much bigger outside the platform. That insight produced two standalone projects, each with its own mission and audience, all three sharing the same underlying technical primitives.

### GoodCompany *(the origin)*
A community platform for work, contracts, lending, and economic coordination. Members govern their own shared treasury and community bank through an internal voting system. Also a marketplace where third-party services — insurance, pensions, professional tools — can be offered to the community.

### P3 — People Powered Politics *(born from GoodCompany's voting system)*
A standalone democratic participation platform. The same voting and proposal mechanics that govern GoodCompany's treasury turned out to be a powerful tool for real-world civic decision-making. P3 lets citizens submit proposals, vote on policy directions, and give politicians structured, verifiable data to make better decisions — repairing trust in democracy without replacing it. Completely independent of GoodCompany.

### Whistleblower / Journalism *(born from GoodCompany's dispute layer)*
A standalone platform for structured whistleblowing and investigative journalism. Originally designed to let GoodCompany workers report workplace misconduct anonymously — using the same evidence-and-review structure as a contract dispute. Expanded to cover journalistic investigations: evidence submission, peer review, validation, and publication to news outlets. Completely independent of GoodCompany.

> These three are not a hierarchy. None of them is the "parent." They share infrastructure — SSI, a case engine, a voting mechanism, an evidence layer — but each has a distinct mission, a distinct audience, and can stand entirely on its own.

---

## The core insight

Across all three platforms, the same primitive keeps appearing. I call it a **Case**: a structured unit containing identity, evidence, conditions, a review process, and a settlement outcome.

| Domain | Example Case |
|---|---|
| Work | Freelance contract |
| Finance | Loan request |
| Governance | Policy proposal |
| Truth | Whistleblower report |
| Journalism | Investigation dossier |
| Insurance | Claim |

```
Case → define conditions → add evidence → review → settle
```

The templates differ. The engine is the same. You don't build three systems — you build one coordination engine and three domain interfaces on top of it.

---

## Technical direction

| Layer | Responsibility |
|---|---|
| **Midnight** | Contract negotiation · evidence handling · dispute resolution · private communication · review workflows |
| **Cardano** | Escrow funding · milestone confirmation · final settlement · audit trail · governance outcomes |
| **SSI** | Identity backbone across all three platforms |

Reputation is domain-separated — your economic track record in GoodCompany doesn't affect your weight in a P3 vote or a journalism peer review.

---

## Open questions — this is where you come in

These are not rhetorical. I genuinely don't have the answers and I'm looking for people to pick them apart.

### 📁 [Case schema](/discussions)
What does a Case object look like that works for both a freelance contract and a governance proposal without becoming so abstract it's useless? Anyone want to draft a schema?

### 📁 [Reputation design](/discussions)
How do you prevent domain-separated reputation from being gamed by early users who accumulate score across all three platforms?

### 📁 [Midnight boundary](/discussions)
Where exactly is the right cut between what stays private on Midnight and what gets settled publicly on Cardano — especially for whistleblower cases where the evidence itself is the sensitive part?

### 📁 [Whistleblower anonymity floor](/discussions)
What is the minimum trust model that keeps a reporter genuinely anonymous while preventing the system from being flooded with bad-faith reports?

---

## What I'm actually looking for

Not investors. Not endorsements. Not someone to implement a finished spec — there is no finished spec yet.

I'm looking for people who find this interesting enough to think about it in the background — and want to meet once a week to share what came up. Cardano or Midnight developers, SSI engineers, governance designers, ZK researchers, people who have built escrow systems or worked seriously on reputation models. The kind of person who reads the case schema question above and thinks *"let me take a stab at that."*

The goal is to reach a point where the architecture is solid enough to build from — and at that point, real funding paths open up: Cardano treasury, Project Catalyst, external investors. But we're not there yet. Right now I just want sharp people in the room.

---

## Get in touch

- X / Twitter: **@[your handle]**
- GitHub Discussions: open a thread in this repo

*This document will evolve as the conversation does.*
