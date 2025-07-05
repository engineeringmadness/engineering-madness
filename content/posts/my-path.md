---
title: "Fork in the road (Part 1)"
date: 2025-07-05T09:47:46+05:30
draft: false
pinned: false
summary: "What really matters"
tags: ["Software Engineering"]
---

![](/4.jpg)

## The Timeline so far

### Level 0 - noob [Sept 2019 - March 2020]

I joined my first company fresh out of college. I was a clueless idiot, like a deer in headlights. I first started out working on a Spring 2.0 legacy project with code from the late 2000s. Being a Pythonista in college, this was quite a shock. Tutorials were almost non-existent (YouTube wasn't really a thing back when this project was written). My only reference was the codebase and the official Spring documentation.

### Data Engineering Stint 1 [March 2020 - March 2021]

After 6 months in the legacy backend project, I got the chance to be part of a brand new initiative to revamp the reporting and analytics side of my department. What's the catch? We had to use an internal big data platform as a mandate. My thoughts on mandates are well documented [Here]({{< relref "posts/platform-engineering.md" >}}). The requirements did not exist; instead, we were handed a 1000+ line SQL Python turdball and our job was to migrate it to a Java/Spark pipeline. As expected, this failed miserably. I left the project using my connections, and ultimately this initiative died a slow death.

### Good Ol Backend [March 2021 - September 2021]

At this point, I am just shy of 2 years into the job, have worked on 3-4 projects, and am no longer a noob. I implement features end-to-end, write documentation, and even participate in hiring, albeit all my work had been in projects of not significant functional complexity. The project I now found myself in was very different. A team of 20 developers working on a monster monolith. An extremely complex codebase with a fully custom form renderer and workflow engine, full of fragile connections that break often. Sounds scary? This is where I learned how to play in the big leagues—how to follow a structured process with involvement of Product Owners, Business Analysts, QA, and Production Support teams.

### React Junkies [October 2021 - December 2022]

The key business stakeholder in my project decided he wanted to modernize the interface of our system and brought in a small UI/UX design firm to consult (The mechanics of how that happens in an MNC baffles me to this day). We needed to build a solution that not only revamped the UI but the entire business process while being compatible with all the existing functionality. I became part of a core group of developers that built a ReactJS adapter to the existing custom form renderer written in Java, thereby bringing the project into the 21st century. This was an effort intensive taks as we had to ensure that all workflows that were in progress could seamlessly be continued in the new and improved interface. As a result we built a very well thought through system and due to this turn of events, I briefly considered becoming specialized in Frontend engineering. I have to admit I was somewhat enamored by React at that time and I have been rid of those delusions now. Unfortunately for me, life had other plans.

### Manager's Dog [January 2023 - April 2024]

After the modernization initiative had wrapped up, I had expressed my desire to specialize in Frontend engineering to my manager multiple times. Even though initially I received some positive encouragement, later on it was made clear to me that my services were needed in other technical initiatives which my manager had in mind. Thus began a journey of complete dismantling of everything that I had learnt about software development. I was drafted into a team designed to execute refactoring and tech debt initiatives. This team did away with Product Owners and Business Analysts, and the requirements were directly dictated by my manager and the way to implement them was also dictated by him. QA was still a part of the team, but they did not follow the standard process of logging defects into JIRA. This was probably the saddest phase of my development career. While I was learning a lot, I felt sad, depressed, and suffocated. A good thing that came out of it was that I used this motivation to divert my attention to my health and fitness. (That's a story for another time.)

### Data (Platform) Engineering Stint 2 [May 2024 - June 2025]

After I reached my breaking point, I decided to have a 1:1 with my manager and we went back and forth for an hour, after which I realized the only way forward was out. So I used my connection with my department lead, directly approach him and orchestrated a move to another team. It was a return to the revamped reporting and analytics project. A lot had changed during the time I was away: we had a new team lead who was my former colleague, new teammates including experienced data engineers, and a new (and hugely improved) tech stack.

Apache Spark had come a long way with the advent of Databricks, Spark 3.x, Delta Lake, etc. On top of that, the project was structured such that I would be part of the "platform team" doing the software engineering part to build the common abstractions used by data analysts and data engineers alike. This has been a fun ride. I realized that Developer Experience was something I was quite good at. I also worked as a data engineer on a few initiatives and honestly it wasn't so bad as the technology was much more bearable now. I was even considering specializing in Data Engineering, the very same thing I thought was deplorable due to its lack of focus on development best practices. 

But should I do it? Is Data Engineering the thing I was meant to do ? What value do Data Engineers really bring ? These questions have plagued me for the better part of 2025. The underlying question of picking my specialization for a lot longer than that, but finally had an epiphany recently that has brough clarity to me in unforseen ways.

### Realizing what I want [July 2025 - Forseeable Future]

To be continued in the next part...