---
title: "Platform Engineering: Take 2"
date: 2026-07-02T12:00:00+05:30
draft: true
pinned: false
summary: "A Failure story"
---

![](/15.jpg)

This is a follow up from an original [manifesto post from many years ago](/posts/platform-engineering) so I would probably give that a read before proceeding with this rant. I switched teams around 2 years back and joined a data platform project. Why ? the opportunity was appealing for a number of reasons, I get to shape the platform software I want, I get to right the wrongs I faced many years prior with the same project and I get to design the abstractions all the users would be using. Its like being a dev's dev. 

## What's the platform

The data platform has essentially 5 teams of analysts & engineers spread across 4 business streams. We use Databricks at the heart of the platform because of its dexterity and developer focus. The surrounding operations such as feed metadata registration, ingestion and merging layer, credential and access management is build on Spring Boot REST APIs.

## What went wrong ?

### Politics and Mandates

My company already has a data platform software bundle that is developed in-house on similar lines but much more convoluted and hard to manage. Initially we had used this piece of junk in our project as well and the results were beyond our imagination. Our project failed miserably and was on the brink of shutting down. Why ? because the in-house software simply didn't have the essential features we needed. 

### Failure of beliefs
