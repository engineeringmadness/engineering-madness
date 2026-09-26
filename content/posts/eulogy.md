---
title: "A Eulogy for Programming"
date: 2026-09-26T10:19:48+05:30
draft: false
summary: "A sad day has arrived"
pinned: false
---

### We're here now

![](/rant.jpeg)

The so-called AI revolution is everywhere now, but for me it's personal: it's the turn of internal tooling software to suffer the repercussions. Internal tools are what I've worked on since the start of my career. What defines this world is fast, sometimes unreasonable deadlines and non-existent scale, with most software projects having ten thousand users at best. There is a lot of obfuscation and a lack of clarity on requirements when it comes to functional processes.

Funnily enough, this AI coding revolution that has people hating their jobs has nothing to do with AI coding agents at all. AI is simply the medium for what has really brought about the end of programming.

### Why we're here

To understand how we have reached here, we need to understand the factors that enabled AI coding agents to take over the job of programmers, especially when it comes to the world of internal software. Three things stand out.

1. Quality stopped mattering - Having worked in this space for many years, I've come to realize that a vast majority of such internal software is below average. Think line-of-business apps, mostly CRUD apps along with workflow engines, data platforms, reporting solutions etc. It has been written to meet deadlines fast rather than to survive for years in production. The codebase is often completely illogical in its nature, the kind of stuff you look at and go WTF was the person thinking when they wrote this. But the real shift was that defects started being just numbers on a JIRA board: whether a release was greenlit with ten defects or a hundred defects or five hundred defects stopped making a difference.
2. Releases became Marketing Gimmicks - Release mails are sent with fervor even if the functionality being released doesn't actually work. Long term foundation work is ignored, the only thing that matters is how shiny the release announcement is. Deliverables stopped being measured by their impact or by what they enabled downstream, and instead became about what seemed the shiniest and most complicated.
3. Leadership hates engineers - Most people don't realize this, but executives hate engineers. Good engineers take an insane amount of money, are slow, temperamental, insufferable and question everything. If given a magic solution that could do 80% of what an engineer does (or at least appear to do so), these executives would fire a majority of their engineers gleefully.

Put those three together and the current enthusiasm starts to make sense. The concept of software factories, aka Claude Code being used to automate software development end to end from tickets to specs to code, test and deployment, is basically a wet dream for these executives. I have seen Managing Directors espouse vibe coding and literally say stuff like the language or framework being used does not matter. Apparently now even reading the code is a bottleneck.

### What do I feel

I feel sad, because the writing really is on the wall. I feel angry towards the people in management for pretending that the vibe coded AI slop is all hunky dory just so they can appear AI native. Will programming die permanently? I don't know the answer to that question, but yes, it's dying for the time being. Maybe there is a future where these executives go neck deep in vibe coding, make a mess so big that they get fired, and the engineers make a comeback, or maybe that doesn't happen. Either way I don't feel like going through this phase and letting myself be turned into a Claude Code junkie.

### Where do I go from here

My hypothesis is that there are 3 fields within tech that are possibly the least likely to be surrendered to AI completely. Software engineering is not one of them, because broken software never caused any problems even in the pre-AI era. Infra, on the other hand, is a different story. If infra goes down, then the software running on it goes down completely. Storage going down can cause data loss. So as the number of vibe coded prototypes increases, we need more Ops and SRE to ensure that the software runs continuously. I don't think any company would be dumb enough to let AI have complete control of their infra even if there is only a 1% chance that AI can delete your database.

As it happens, I've already had a taste of this. As part of my role in a data platform team, I got the opportunity to do a lot more ops work and be much more involved with the infra side of things, and honestly it wasn't too bad. Hence I think a DevOps / Ops / SRE role is where my future lies.

That leaves the question of how I get there. I need to polish up my fundamentals - Linux, Git, Python - and get hands on with the 2 main infra tools that have taken over the entire industry, that is, Kubernetes and Terraform. Additionally, I would need to have a good idea of at least one CI/CD platform like GitHub Actions / GitLab CI / ArgoCD etc. I am planning to pursue certifications in Kubernetes and Terraform to bolster my chances prior to looking for a switch. For all of this, I plan to use a really cool website called KodeCloud.
