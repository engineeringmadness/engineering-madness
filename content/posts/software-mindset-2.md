---
title: "A Treatise on Software Development Process (Part 2)"
date: 2024-04-07T11:34:15+05:30
draft: false
pinned: false
summary: "The Way"
tags: ["Software Engineering"]
---

## Setting the context

Let's start from where I left off in the previous entry where we talked about finite vs infinite games. If you believe my hypothesis that many aspects of software projects can be modeled using an infinite game, the logical follow-up is how do we ensure we can sustain an infinite game compared and not slip back into a finite one? This brings me nicely to the second question.

## Question 2 - Goals vs Systems

“Goals are about the results you want to achieve. Systems are about the processes that lead to those results. You don’t rise to the levels of your goals you fall to the level of your systems” - James Clear

In his book, James Clear uses an interesting analogy of a 100-meter race. All the athletes competing have the same goal which is to win but the person who ends up winning has the best systems in preparation for the race. Winning the race is not a function of clarity of the goal but instead a function of training and hard work put in over a long period. It's the intensity and consistency of the athlete that differentiates them from others and helps them win.

How do we approach the abstract ideas of Quality, Reliability, UX, etc along the same lines? A common approach is to define metrics, and KPIs and go about it numerically. Let's take one of these ideas e.g. reliability. Let's say you want to ensure that there are very few defects in the system so the software solution is easier to use. You can try to track defects in terms of their origin or root cause, maybe attribute them somehow to specific feature requests or even developers. But this violates the trusting teams principle which is a prerequisite of infinite games. Attribution also establishes a not so fun work environment and the developers may not feel confident while making changes to an inherently fragile system.

Instead, we can focus on building safety nets in the form of a comprehensive testing pyramid. With a large base of unit tests (often the part that is missed), a smaller suite of integration tests, and an even smaller set of end-to-end acceptance tests. We also must ensure that the developer experience (DX) is such that writing new tests and maintaining existing tests is super smooth for developers otherwise such test suites often become obsolete. These tests serve as a safety net for anyone who is implementing new functionality or more importantly refactoring the core functionality of the system. How? By providing confidence and peace of mind to developers that they can mold the software without blowing things up. Further removal of friction can be achieved by making these fully automated and triggering them with each commit or PR or on a regular schedule. All of these are not new ideas either and have been repeated time and again in many books and talks by industry experts. But what I am saying is that we need to engage first in an infinite mindset and we need to stop focusing on metrics like code coverage and instead focus on engraining the habit of testing within the team. Introducing any change in behavior needs incentives and thus we need to design our incentives to reward habit building and consistency instead of results. We need to move just a little bit in the right direction every day putting focus on systems that prepare us to achieve our goal of reliability rather than measuring our progress towards the goal itself.

## A Personal Story

Diving deeper into how I made the connection between Atomic habits and my day-to-day work comes from a personal story. I recently gained this perspective when going through a journey of embracing fitness after struggling for many years with overeating. I realized that while I had tried previously many times, I had often failed due to overambitious goals, stretching beyond my capacity, and fatigue. This time when I succeeded it was because I focused on designing simple routines focused on the fundamentals of nutrition and exercise. The basic routine reduced friction in adopting the healthy practices that got me moving in the right direction. Why do most people fail to change their habits? because changing habits is hard and our inherent nature is to resist change. I trusted the fundamental process I was following rather than tracking my results and the consistency of my habits is what ultimately helped me reach my goal in due time.

Reference - Atomic Habits by James Clear
