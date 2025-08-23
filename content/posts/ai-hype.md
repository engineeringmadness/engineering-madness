---
title: "AI: The Age of Silver Bullets"
date: 2025-08-23T11:34:15+05:30
draft: false
pinned: false
summary: "Cause I'm a punk rocker"
tags: ["Software Engineering"]
---

![](/7.jpg)

## Why the Rant

How can you tell that something is hyped in technology? Well, thankfully we have Gartner to make such predictions. As per their latest report, [40% of Agentic AI projects will end up canned by the end of 2027](https://www.gartner.com/en/newsroom/press-releases/2025-06-25-gartner-predicts-over-40-percent-of-agentic-ai-projects-will-be-canceled-by-end-of-2027). That's weird because if you look on YouTube or Instagram, then AI agents are not changing the world—they have already succeeded in doing so. I am not denying LLMs are fascinating and have the potential to solve some unique problems that were previously hard or impossible to solve, but the way Agentic AI is being marketed to the moon, you would believe they can literally solve every problem statement ever. Need to travel somewhere, need to code an app, need to write an essay, need to do graphic designing—they've got you covered. The best part: all these agents can "collaborate," aka work together to produce a quality output. It seems to be right out of a Sci-fi movie.

## What the hell is an AI Agent

Honestly, it's one of those terms which is used quite loosely. In the simplest of terms, an AI Agent is a large language model (LLM) paired with a system prompt. It may have access to one or more tools. It may have access to some sort of vector store knowledge base for reference (I consider everything apart from the prompt to be optional, but some hardliners don't). So, I put forward a simple definition: An AI agent is simply a tailored system on top of an LLM which has been armed with some form of additional context, whether that be through the system prompt, a set of tools, or a vector database.

## Why Everyone is aboard the hype train

### Infinite Money Glitch

In a post-Covid world fraught with recession, mass layoffs, and drying-up venture capital, AI seems to be the one area that is flush with funding, whether it be in large corporations, boring enterprises, or startups. Budget cuts and hiring freezes are put aside as soon as that one magical word is uttered (and its not Shazam!)

### A Solution without the need for a Problem

In most enterprise companies right now, you will hear things like "We are launching initiatives for 'Using Gen AI for X'" or hackathon statements like "Agentic AI for Y." This pattern is something I have seen quite often in the past too—Data Mesh, Blockchain, Microservices. Speaking those magic words regardless of the context of a problem gets you a pat on the back by the talking heads. But of course, this approach is backwards. The key to creating a good solution is to start with the problem first and then pick the tool best suited.

### Reductive UX

Chat is quite possibly the worst user experience for a multitude of use cases. Of course, it makes sense in a few cases as well, e.g., customer support where people are already used to a chat-like interface. For everything else, we have years of muscle memory for how to operate mobile and web UI, and chat removes all that leverage for designers. Intuitive controls, beautiful UI elements, smooth transitions—all the frontend craft gone straight out of the window. E.g., if I want to plan a trip, instead of speed running through options, I have to sit and chat with a bot who will go ahead and find me options.

### Fetish for Everything Micro

Honestly, this one is bizarre, but solution architects love everything that involves making small colorful boxes, and Agentic workflows are a perfect match. Whether it be microservices or micro-frontends or agentic workflows, the more the boxes, the merrier. My hypothesis is that the increased complexity gives a natural ego boost by making people feel that whatever they are doing is hard and important. As Terry Davis brilliantly puts it—

> An idiot admires complexity, a genius admires simplicity

## How I use LLMs

### A Piece of Your Design Toolkit

I see LLMs as yet another Lego block in your arsenal when building a flow in a system. It's how you would use a database or a message queue or a Spark cluster for certain use cases. The same way these systems have their pros and cons, so do LLMs. LLMs can be seen as engines that encode a large chunk of world knowledge. They are best suited for tasks where you can't define a set of steps or an algorithm, but you can explain your task in good detail covering all edge cases in plain English.

### Translating from Unstructured Data to Structured Data

Structured outputs are also a great use case for LLMs. Converting any kind of text input and extracting attributes from it in a particular schema like JSON or CSV is very useful. Why? Because JSON allows you to plug in other deterministic blocks like traditional software pipelines. Nowadays, libraries have gone a step further and they can deserialize the output JSON directly into a native object in the programming language of your choice.

### Real Contextual Search

Gen AI-powered search is a real game changer. If you are still reading and haven't used Perplexity, please try it out. LLMs, being encoded with a large chunk of the internet's knowledge, means that they can parse through large swaths of text and correlate direct or indirect dependencies between pieces of content. This could be applied to documentation, requirements, tickets, etc.
