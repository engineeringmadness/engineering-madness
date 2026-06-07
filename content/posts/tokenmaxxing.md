---
title: "The End of Tokenmaxxing"
date: 2026-06-07T07:51:28+05:30
draft: false
pinned: false
summary: "Its Magnificent"
tags: ["Shorts"]
---

### What is it

For the uninitiated, Tokenmaxxing is a trend in the software industry where people are incentivized to use as many tokens as they can. Often times this phenomena is gamified with company wide leaderboards showcasing people who used the most tokens. 

To understand the absurdity of this idea one has to fundamentally differentiate between Inputs, Outputs and Outcomes. When a human writes software the inputs could be time, documents, meetings etc. the output being lines of code written and the outcome being hopefully solving a business problem. 

### Understanding the Stupidity

LOCs (line of code) which is basically a measurement of software engineering output was often used in the past to judge engineering performance. For any person with critical analysis skills it may be obvious that volume of code is not directly proportional to its quality and volume does not guarantee any outcome whatsoever. For instance we often write throwaway code to do experiments, build MVPs that don't make it to production. In other cases code may not be used due to change in business requirements or priorities.

To quote Linus Torvalds, creator of Linux - "Anyone who thinks Lines of code is a valid metric is too stupid to work at a tech company".

Now consider "token usage" which is quite different from LOC in the sense tokens can both form inputs (user prompt, file reads, web research) and outputs (lines of code). An average LLM request is composed of 80-85% input tokens and 15-20% output tokens. So when we're measuring token usage we're not even measuring outputs let alone outcomes, we're mostly measuring inputs 🤔. While outputs did not guarantee outcomes, inputs simply have no correlation with outcomes, which basically implies that measuring tokens is pointless. 

### Why is it coming to an end

Turns out the subscription plans that enabled this kind of extreme usage of tokens were never sustainable. Both Anthropic and OpenAI lost tons of money on these 20 dollar / 40 dollar plans. The equivalent cost of the tokens at API pricing would often range from 200 - 1500 dollars, which is a loss of 90%.

In the enterprise companies the tokenmaxxing trend was killed primarily by [GitHub Copilot switching from a requests model to API based usage]({{% relref "ai-billing-shift.md" %}}). People who had been heavily using (or abusing) the generous limits of GitHub Copilot reporting that they've exhausted 25% - 50% of their monthly usage after just few days. 

### Conclusion

As someone who is probably in the AI skeptic camp, this is just magnificent. I believe a good thing that has emerged from this era of Agentic coding hype is the shine has come off big tech. 

Big tech companies like Meta, Amazon & Microsoft have pioneered mass layoffs combined with ridiculous AI mandates only to then backtrack on the same. As we settle into the post tokenmaxxing reality as the AI hype train is subsiding, here are some of the greatest hits from this era - 

- [Amazon now mandates sign off from staff engineers on AI generated PRs after a slew of production outages](https://www.fintechweekly.com/news/amazon-ai-coding-outage-review)
- [Microsoft is cutting Claude code subscriptions citing cost issues](https://fortune.com/2026/05/22/microsoft-ai-cost-problem-tokens-agents/)
- [Uber blew through their entire AI budget in a few months](https://techcrunch.com/2026/06/02/uber-caps-employee-ai-spending-after-blowing-through-budget-in-four-months/)
- [Meta now using software engineers as professional AI labelers](https://timesofindia.indiatimes.com/technology/tech-news/meta-to-selected-engineers-joining-the-new-applied-ai-engineering-unit-is-no-longer-optional-it-is-now-compulsory-as-the-company-is-moving-to-/articleshow/130183798.cms)
