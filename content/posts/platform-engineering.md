---
title: "Platform Engineering 💟"
date: 2025-01-19T12:51:42+05:30
draft: false
summary: "Lessons in empathy and humility"
tags: ["Software Engineering"]
---

![](/1.jpg)

## What is a Platform

> It is a foundation of **self-service** APIs, tools, services, knowledge, and support which are arranged as a **compelling** internal product - Evan Bottcher 

## Platforms live and die by DX
Having worked at the same company for more than 5 years gives you a unique perspective. You start observing the subtle ways things change with time
and become larger trends. The move from applications to platforms is a trend I see everywhere. It's driven I think by 3 key factors. Firstly, 
there are obvious common patterns that start to emerge across applications and it makes sense to not reinvent the wheel. Secondly, everyone in our industry likes chasing impact and impact is directly proportional to career growth (at least theoretically). Lastly, it feels good as most engineers are vain creatures and have some level of pride in their work hence if others use their software then it serves as validation.

All of these sound fine so where does the problem arise? 
> With great power comes great responsibility.

Just as our representatives are elected to serve not to rule, platforms are meant to make engineer's life easier not harder. The core idea is to abstract away or automate the mundane repetitive things that plague a particular problem area e.g. infra provisioning, scalability, monitoring, release management, etc.

Sometimes in this quest for building the most ideal platform, we get entangled in the intricacies of our codebase to such an extent that we lose perspective of the core mission of platforms which is to make engineers' lives easier. Hence the key metric of a platform should be its Developer Experience (DX). In reality, what we see is that these platforms are often mandated by CTOs, architects, and management folks which is not a good idea in the long run. Giving recommendations is fine, but the platform should be capable itself to attract developers. Platforms that don't prioritize DX can survive based on mandates but they do more damage in terms in the area of mental health of their users.

One exception I can think of is probably the realm of security where mandates are necessary to maintain safety standards but apart from that someone choosing to not use a platform should not be a world-ending event. Engineers are thoughtful and creative people and they don't need to be given to be goaded into technical decisions (please save that approach for LLMs).


## Operations 
I see that in the industry there is a fundamental belief that ops is tedious, boring, and life-draining. But is that really because it's ops or because you are doing ops wrong? Ops rotations become problematic due to a lack of support and structure. So how do you fix it? 
1. L2 teams are antiquated, The developers that created the platform are also best placed to run it. Vertically integrate business, tech and ops while cutting out red tape to increased efficiency.
2. Load balancing and triaging mechanisms - A very basic ticketing system combined with a triage mechanism to evenly distribute issues can ensure one person doesn't get overloaded or fatigued.
3. Ensure people either have the context to the problem they are supplied with or they know who to reach out to for gaining that context. The struggle people face due to not having context is what makes people hate operations work in reality. If they have the tools to solve the issues then they will feel good about their work.
4. Ensure things are written down in some form. It does not have to follow X formatting or Y architect's standards. Instead, documentation should be simple to understand and more importantly navigate. This helps speed up new joiners catching up and also reduces struggles surrounding missing context.
5. Energy is infectious - Something I have seen personally is that if you approach users with a positive attitude then 90% of the time it they respond in kind. Of course, some people don't operate in good faith and will try to take advantage of you but that doesn't mean you start expecting that every user has mal-intent.

## Backwards Compatibility
Linux exemplifies this best. A large codebase that is constantly evolving but is cognizant of the impact of kernel failures. Some 96% of all servers run Linux and it was possible due to the core tenant that you do not break user space. Something that you do in the platform space should never cause breakage in the application space. Applications and users can be somewhat late in the adoption of features so backward compatibility becomes crucial. 

Here's an anecdote from Linux. The kernel team at some point changed the manner in which the current version of the kernel was reported from one format to another. Turns out there was software out there that depended on the old format used by the kernel and it took a few months post the change for these issues to be reported. 

While this was obviously a design flaw on the part of the application developers, the Kernel developers went out of their way to remedy this situation.
They added a Compatibility flag and enabling this would ensure that the kernel version was reported in the older format. They didn't have to go overboard like this and I am pretty sure that no one would have blamed them if they had just left this for the application developers to sort out, but it's the principle of never breaking user space that led them to prioritize a fix for this.

## The Implementation Spectrum
Running a platform means you have to maintain a delicate balance between forcing standardization versus allowing users the freedom to develop or solve problems their own way. This balance can be expressed as a spectrum between a managed service that completely abstracts away the problem from its users at one end, a framework that allows some customization but overarches your implementation and a library that completely offloads control to its users who can use and extend it freely on the other end.

A good tenet would be to classify the functionality as essential or additional. Essential functionality could be modeled as a managed service especially if it's a tedious use case. Examples of such use cases would be automated deployments, access management, and credential management.
On the other hand, utilities, testing helpers, and integration code/glue code are good examples of things that could be packaged in a library allowing users to pick and choose what works for them.

Connecting with your users by embedding in their daily or weekly scrums can be a fantastic yet obvious technique to understand user behavior and shed light on where a particular functionality should be placed on the spectrum.


## A Manifesto Emerges
So here's what I consider to be core tenets of a good platform, distilled from my own experiences over the past years.

```html
> DX over mandates

> Incremental adoption over Big bang revamps

> Feature pruning over Feature packing

> Golden paths over Golden cages
```

