---
layout: post
title: "Where Did Everyone Actually Land? 713 Comments, Coded"
date: 2026-08-23
categories: [Virtualization, Infrastructure]
tags: [VMware, Broadcom, Proxmox, Nutanix, Hyper-V, XCP-ng, OpenShift, KVM, OpenStack, HPE-Morpheus, data, virtualization]
description: "I coded all 713 comments from the Broadcom retrospective by destination, org size, sentiment, and argument. The full interactive dashboard and the complete raw dataset are both here to download and check yourself."
banner:
  image: https://img.youtube.com/vi/FV-YEu6tXZk/maxresdefault.jpg
  opacity: 0.618
---

![](//youtu.be/FV-YEu6tXZk)

**The full dashboard and the raw dataset are both published here, exactly as built:**

- 📊 **[Open the interactive Comment Ledger dashboard](/assets/data/vmware-comment-ledger-v3.html)** — every chart from the video, in one page.
- 📄 **[Download the complete coded dataset (CSV, 653 rows)](/assets/data/vmware-coded-comments-v3.csv)** — every comment I coded, with my destination, scope, sentiment and theme tags. Check my read on any of it.

---

## Introduction

Hey there homelabbers, self-hosters, IT-pros, and engineers. Rich here! The last video was wildly successful, and so many of you leaned in to give me your thoughts on Broadcom, my research, what happened to you, and so much more. As I read through all of the comments, I realized there was an even more interesting story to tell from the data sitting inside them. Once I dug in, it painted the most honest and accurate picture I've got of where you actually went and how things shook out.

---

## What This Data Is, and What It Isn't

Before I show you anything, I want to be straight with you about what this data is and what it isn't. Because I'm about to put a bunch of charts in front of you, and charts are very good at looking more authoritative than they deserve to.

YouTube says that video has 841 comments. I pulled 713 of them. That's just under 85%. The missing 15% are comments that got deleted, held for review, or came from accounts that no longer exist. **So this is not a census.**

It's also **not a survey**. Nobody randomly sampled you. This is a self-selected group of people who watched a 20 minute video about where the hypervisor world shook out and then felt strongly enough to respond. That skews toward people with opinions and people with war stories.

And one more thing. Out of everyone who told me where they landed, only about a third also told me how big their organization is. So anywhere I split this by company size, I'm working from that subset, not the whole thing.

None of that makes this useless. It makes it **directional**. I'm not trying to sell you on this as some more accurate alternative to real market research, or trying to argue with the actual numbers that exist out there. But I think the information sitting inside these comments is fascinating, and it tells a story of its own. Let's dig in.

---

## Where People Landed

Let's start with the headline chart. Every commenter who told me what they're running now or what they're actively migrating to is represented. I took great effort to categorize, where possible, what sector or group each commenter was coming from: enterprise, education, SMB and mid-market, MSP and consultant, homelab, and finally unstated.

**Proxmox leads here with 51 total mentions.** Hyper-V is second at 31. VMware itself holds third at 24. Then Nutanix at 20, raw KVM at 18, XCP-ng at 17, OpenShift at 9, and a long tail after that.

Two things on this chart are worth calling out before we move on.

Hyper-V's 31 undersells itself in the raw comment feed, because that kind of comment tends to be short and doesn't get much engagement, so it's easy to scroll past. The data doesn't care about engagement. It counts the same either way.

And VMware's 24 isn't pure inertia. **15 of those are people explicitly choosing to stay**, with specific reasons, not people who just haven't gotten around to leaving yet. We'll get to exactly what those reasons are later on.

---

## The Segmentation, Using Only Commenters Who Revealed Their Scale

Now let's look at the data a different way, sliced by how big the commenter's organization is, using only the people who actually shared that information.

OpenShift was **100% enterprise or education**, which isn't a surprise given the market space it serves. Nutanix is at 89% enterprise and VMware at 55%. But around Hyper-V is where we see the shift happen, at 52% enterprise. KVM: 42%. Proxmox: 31%. And XCP-ng: 15%, the low end of the scale.

Two platforms sit at hard extremes here, and one platform breaks the assumption you'd make from the first chart.

OpenShift and Nutanix are basically enterprise-only in this data. XCP-ng is the mirror image, essentially an SMB and homelab platform. Honestly, there's nothing surprising in either of those.

**Proxmox is the one that doesn't fit the story you'd tell from mentions alone.** It gets talked about like the scrappy small-shop pick, and plenty of it is. But a third of its identified landings are enterprise, including estates in the thousands of VMs. It's not winning at just one segment; it's winning at breadth, across the widest range of shop sizes of anything in this dataset.

---

## Weighted by Workloads, the Ranking Inverts

Now the same question asked a different way. Not who's running what, but **how many machines are actually moving**.

27 people who told me where they landed also told me their fleet size, adding up to 82,100 workloads total. Weight the landings by machine count instead of by person, and the ranking flips. **Nutanix takes a third of everything moving** in first place. Proxmox drops to second at 22%, and Hyper-V, second place by mentions, falls under 5%.

Both of those charts are completely accurate, and they completely disagree with each other. I find that genuinely fascinating, because it shows an entirely different perspective on the same comments.

If we count people, we learn what the community is doing. If we count machines, we learn where the compute is actually going. On the first chart, one person equals one vote. That same one person can also equal a five-figure fleet on the second one. So fundamentally: **Proxmox is winning on breadth and Nutanix is winning on depth.** Both of those are real ways to win, and neither cancels the other out.

---

## How People Talk About Each Platform

Let's talk pure opinion now: how much praise and criticism each platform picked up from commenters, regardless of what they're running.

Once again, **Proxmox is the darling here at +52.** No other platform comes close. KVM, XCP-ng, Nutanix, OpenShift and Hyper-V are all net positive. VMware lands at -17, which is no surprise.

But then there's this: one alternative platform comes out net negative, and that's **HPE Morpheus, at -5**.

That last one is the single most interesting number on this chart, because it sits right next to a fact that isn't in the sentiment data at all: HPE is currently running one of the most aggressive migration incentive programs in the market, free licensing and hardware support to pull people off VMware.

So at the exact moment HPE is paying to win these customers, it's the only alternative with a negative reputation among the people already evaluating or using it. And the criticism in the data isn't really about the product. **It's about HPE as a vendor.** That tension between HPE's offer and the word of mouth is worth watching, because I don't think it's resolved yet.

---

## What the Comments Argue About

This chart is more interesting from a human perspective. It's my coding of every recurring argument, ranked, across all 653 statements.

The single most common thing in the entire dataset, outside of nostalgia comments, ahead of any platform or complaint, showing up **53 separate times**: the fact that the three-year license agreements signed right before the Broadcom acquisition expire in 2027. A lot of people believe that date will trigger yet another massive wave of migrations off VMware.

Sitting right alongside that is a second, related argument: **the hardware refresh cycle.** Nobody replaces a hypervisor in isolation. They replace it when they're already buying new servers, because that's the moment migration cost drops to nearly nothing. Which means the 2027 licensing cliff and the next hardware refresh cycle are lining up for a lot of shops at the same time, and that combination is probably the real trigger for the next wave, not the licensing deadline by itself.

One more thing worth mentioning: there were a grand total of **just six comments** pushing back and defending Broadcom's position. I point this out because it's important to be aware of: there are still some true VMware believers out there, and while their voices were very much in the minority, they did speak up.

---

## The Price Shock, in Their Own Numbers

Twelve people put a specific number on their renewal increase. The range runs from **15% at the low end to 5,400% at the high end, with a median of 400%.** The dashboard table includes where those commenters landed, where they shared it.

The 5,400% number is the one that'll get screenshotted, and it's real, but it's the tail, not the center. What the twelve numbers actually cluster around is **400%**, and that's not just an artifact of my small sample. It lines up with what the analyst firms covering this have been saying for a while. Gartner, for example, has cited a typical range of 300 to 400% for organizations converting from perpetual licensing to the new subscription model, and that shows up across multiple independent surveys, not just one report.

Seeing that number reflected in the video's comments gives me more confidence in what my own numbers are showing. The wider figures you'll see elsewhere — a thousand percent, fifteen hundred percent — are also real. They're just the more extreme cases.

---

## Fleet Sizes Named

27 comments named a specific VM or host count. Added together, that's the 82,100 workloads behind the weighted chart from earlier. These are the raw numbers driving that third chart, and it's where you see Nutanix pulling some serious numbers compared to the other platforms.

What the table makes visible is **how concentrated that number is.** A handful of very large estates account for most of the total volume, and everything below a few thousand VMs is a rounding error against them. That's the exact mechanic behind the gap between the two landing charts: a small number of very large movers can outweigh a much larger number of small ones.

---

## Platforms You Asked Me to Cover

This is what the data says people wanted covered, and didn't get, in the original video.

**SUSE Harvester leads the list**, followed by CloudStack, oVirt, Sangfor and VirtualBox, then a long tail of smaller requests. Some of these, like the use of VirtualBox for business virtualization, came as a surprise to me, and I don't know that I'd consider that a virtualization platform myself. I may revisit a few of these names in the future, but regardless, I thought having them represented here was good enough.

A good chunk of that list is platforms with almost no footprint in mainstream English-language tech coverage. That's not a coincidence, and it connects to something bigger in the data about where in the world people are actually landing.

---

## Signals Worth Building On

Beyond the charts, the dashboard pulls out specific patterns that don't show up cleanly in any single graph.

### HPE Is Giving Away Hardware

HPE is running an aggressive incentive program to win VMware refugees onto its Morpheus platform. And Morpheus, as we already saw, is the only alternative platform with net negative sentiment in the entire dataset. The criticism is aimed at HPE as a company, not necessarily the product itself.

Free hardware and financing on one side, a reputation problem on the other, at the exact same time. That's the most interesting open question in this whole market right now, and the data doesn't resolve it either way.

### Nutanix Cuts Both Ways

Nutanix shows the same kind of split, at a smaller scale.

One organization in the data consolidated eight or nine VMware clusters down into two Nutanix clusters, a real efficiency win. But a separate, independently documented pattern in the same dataset describes the opposite outcome: mismatched end-of-life timelines that kept organizations from realizing return on their hardware, and a compatibility list strict enough to disqualify the older servers a lot of shops are stuck extending right now.

Both of those are true, in the same dataset, about the same platform. That's Nutanix in one sentence: **it delivers exactly what it promises for the shops it fits, and it's rigid enough to punish the shops it doesn't.**

### Proxmox's Real Ceiling

Proxmox's limitations in the data cluster in one specific place: **support, not capability.**

Contractual SLA requirements it doesn't meet at some companies. Storage configuration that takes more manual work than a comparable VMware setup. Open questions about maintenance burden at real scale.

One piece of that gap closed itself while I was coding this. LVM snapshots over iSCSI, a commonly cited missing piece, shipped as a technology preview in Proxmox VE 9. Still not something I'd put in production without testing hard, but it's real, and it's newer than most of the criticism about it.

### The People Staying Have Reasons

Back to that 15-comment figure from the first chart. Here's what the data says those reasons actually are.

A full VCF stack — vSphere plus vSAN plus NSX plus Automation — with no single-vendor replacement available yet. Application certifications tied specifically to VMware. Storage architecture that rules out the obvious alternative. A VDI deployment on Omnissa.

**None of those are inertia.** They're specific, technical blockers, and they're the strongest counterweight in the whole dataset to the idea that leaving is automatically the right call for everyone.

### Digital Sovereignty Is Now a Buying Criterion

Thirteen comments raise digital sovereignty, and it's not abstract. It shows up as an actual purchasing criterion, with specific non-US and non-cloud platforms named, and the pattern spans multiple continents, not just Europe.

That's the blind spot this data exposes most clearly. Most English-language coverage of this whole saga treats the alternative market as five or six platforms everyone's heard of. **The comment section alone names close to twenty**, and a meaningful chunk of that list is being driven by geography and sovereignty concerns that barely register in the US conversation.

### The Individuals Nobody Serves

Twelve comments in this dataset aren't from organizations at all. They're from individuals who lost a hypervisor they used for personal projects, hobby labs, or one-off technical needs, and they don't fit into any of the enterprise or SMB framing the rest of this data uses.

That's a segment with no chart of its own, because there's no fleet size or price increase to plot. But it's twelve people telling the data the same thing four different ways: **there was no plan for them in this transition, and there still isn't one.**

### Four Smaller Patterns

Rounding out the signals section:

- **The cost crisis stacked.** Hardware and cloud costs climbed at the same time this transition was happening, which is pushing some platform choices as much as licensing is.
- **The certification glut.** A certification market that's about to be oversupplied with VMware specialists and undersupplied with everything else.
- **OpenShift's clean record just broke.** Even OpenShift, the most uniformly positive platform in the sentiment data, has its first documented production failure report in this pull.
- **The retooling problem nobody budgeted.** A recurring point that the actual blocker at a lot of shops isn't the technology at all, it's that the people running it don't know their new stack yet.

---

## So What Does All of This Add Up To?

There's no single winner in here, and that's the real finding sitting underneath every chart on that page.

Proxmox wins on breadth. Nutanix wins on the biggest fleets, with real friction attached. Hyper-V wins quietly on inertia and license bundling. OpenShift wins inside Red Hat shops. HPE is buying its way into contention while its own customers argue about whether to trust it. And there's an entire sovereignty-driven layer of the market running platforms that barely register in English-language coverage at all.

Two years ago there was basically one default answer. **This data says there are at least eight now, and every one of them has real production workloads behind it.**

That's not a market anybody conquered. That's a market that got created by accident, on the way out the door.

---

## Go Check My Work

I'm putting the full dashboard, every chart on this page, plus the complete coded dataset right here so you can go through it yourself and check my read on any of it:

- 📊 **[The interactive Comment Ledger dashboard](/assets/data/vmware-comment-ledger-v3.html)**
- 📄 **[The complete coded dataset (CSV)](/assets/data/vmware-coded-comments-v3.csv)**

Here's what I actually want to know next. If you're one of the fifty-three people staring down a contract expiration in 2027, I want to hear where you actually land when that deadline hits, not where you're planning to land today. If you're willing to share that in the comments, I'm willing to listen — and maybe there's another video in that down the road.

To everyone who commented on the last one: thank you. You helped expand a video where I gave you my readout on the market into a video built on the actual data you handed me by sharing your real-life experiences.

---

Thanks for watching and reading, folks, and thank you to the fine people who support us through **Patreon** and the **YouTube Membership** program. If you'd like to support what we do here, consider checking those out. Join our community **Discord** and chat with me and like-minded homelabbers, geeks, and nerds, and as always, we'll see you on the next one!
