---
title: "I Have a Cloud Dream"
date: 2023-07-18T15:21:43+05:30
draft: false
summary: "False hopes and the Cloud Migration Epidemic"
pinned: false
---

![](/6.jpg)

We were sold a dream, No more worrying about hardware provisioning time, patching infrastructure, monitoring and maintenance.

> Are you in the power plant business then why build and maintain a Data center? Move to the cloud and just use the power of others

One of the most influential trends that we see in the last 10 years that seems to be taking over the industry is migrating all applications from a traditional on-premises setup to a public cloud provider like AWS / Azure / GCP. Many of the fortune 500 decided to begin a massive campaign of moving their applications bit by bit from their own data centers into one of the aforementioned providers. At this very moments millions of dollars are being spent to either lift and shift these application or completely rewrite / re-design these applications to be "Cloud Native" (What does this term even mean really!). Listening to [DHH](https://dhh.dk/)'s recent talk on Cloud exit of Basecamp I began to reflect on my own experiences over the past few years at work. Here are some of the false promises that were sold to us.

## First they came for the executives

What do executive care the most about? The answer if you didn't guess it already is Cost. One of the first concepts you are taught when doing any cloud certifications is the power of elasticity. Why pay for hardware when you don't need it. Whenever your application is not under load it automatically scales down and saves you money and whenever there is high load then the application scales up and delivers a good experience for its users. Where are we now ? I see people throwing Kubernetes clusters at every problem they see. When those clusters run for long and rack up large bills then they decide to shut down the clusters during the non business hours to save cost. Wasn't Availability also core advantage of cloud, it was !!! In an effort to reduce rampant cloud cost we compromise on the availability of the environment. Most businesses have constant or linearly scaling loads they don't need distributed clusters or serverless functions all they need is few servers.
![what if](/wait-what.gif)


## Then they came for the managers

What do managers care about the most? Productivity. Cloud providers marketed their platform as an easy to use, convinient tool through which everyday engineers and even non-technical people could spin up infrastructure, with no need for patching and maintenance you didn't need any operations folk either. Every Dev team could own and manager their own infrastructure with little to no downtime. In reality, configuring the infrastructure was not at all easy. You had to write and maintain the infrastructure in the form of templates which are basically proprietary DSLs. If your infra deployment fails then good luck figuring out what went wrong. This process became so complicated that you have specialized DevOps / Cloud developers within each Dev team now. Its almost like the good old infra team just dispersed and embedded individuals within the very teams they use to work with.
![serverless](/serverless.jpg)

## Then they came for the developers

Microsoft is the best case of how developer relations can be a trojan horse with which these cloud providers enter into a corporation. They buy up popular tools (GitHub) or make them like (VS Code) and they can build easy to use integrations with there proprietary services. They can make their proprietary solutions appear easy to use with friendly documentations, youtube videos and conference talks while hiding the cracks in their solutions.

Another neat trick is certifications. Props to whoever came up with this idea, I can literally imaging the management folks salivating at the pitch. "So you are telling us that people will give us money and we will in turn give them a piece of paper that makes them feel good about themselves. They will then go on to evangelize our proprietary products giving us free marketing." 
![bezos](/bezos.webp)

## Then they came for me & there was no-one left

Time for a personal story.

**Policy Folks** - We are doing credential management wrong. Storing database password in source code repository is very bad.

**Me** - Ok, lets move keep it on the servers in a config file and restrict access to the file

**Policy Folks** - No, you need to use a secure credential management system from where the application will read the password and then connect to the database

**Me** - Ok I guess

Few moments later... Developers spending humungous amounts of efforts migrating each and every account to a secure credential management system even for vendor products which don't give a crap about the Policy Folks.

**Policy Folks** - Now you need to migrate to new version of Postgres and We don't recommends using passwords to connect to PostgreSQL.

**Me** - Uhh, How will we connect to the database then ?

**Policy Folks** - You will create an account and call the Microsoft authentication service to get a temporary token and use that to connect to the database

**Me** - But didn't we just migrate all accounts to a Secure credential management system so we can use passwords

**Policy Folks** - We don't recommends using passwords. 

![jon stewart](/mindblown-jonstewart.gif)