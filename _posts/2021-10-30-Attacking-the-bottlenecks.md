---
title: Attack the Bottleneck
categories:
  - software
tags:
  - agile delivery
  - metrics
---

I was recently introduced to Actionable Agile, a tool to gather metrics around your delivery process. it comes as a plugn for jira and imports your data to analyse and report on 4 metrics:

* __cycle time__ - the time it takes for a work item to be deployed to live; low is good
* __throughput__ - the rate at which items are deployed to live over a given time period; high is good
* __work in progress (WIP)__ - the number of work items that are in flight and not yet completed; low is good
* __work item age__ - the time a given work item is in progress for; low is good

We should assume we are working on the change that is deemed most valuable to our users, and our work items are deemed 'done' when it has been released to the production environment. 

Given this caveat, the faster we get that valuable change out to our users the better, as we start to receive feedback sooner, and the customer can make use of the new change, be it a new feature, bug fix, or UX tweak.

Reducing the amount of work going on at the same time (WIP) reduces the chance of time-wasting context switching when we have to re-work an item because of bugs, merge conflicts and determining which change has caused a bug. 

Reducing the size of work items reduces the amount the new work deviates from the working software, and reduces the time taken to receive feedback on that change.

## What about Accelerate?

We can compare these with another modern set of metrics from the DevOps Research and Assessment (DORA) group aka the Accelerate metrics: 

* __lead time__ - the time it takes for a work item to be released to the customer; this is AA's cycle time.
* __number of deployments__ - the number of deployments to live that are made over a given time; this is the same as AA's throughput
* __change failure rate__ - the ratio of unsuccessful to successful deployments; this relates to work item age, in that smaller changes are likely to have a smaller chance of going wrong 
* __mean time to recovery (MTTR)__ - the time taken to resolve an issue in production; again, deploying smaller changes reduces the blast radius of faults and easier to identify which change caused the issue.

## Monte Carlo or bust

Another great feature of Actionable Agile is its Monte Carlo forecasting. This uses the analysis of historical work to predict when work will be complete by the in future. TO me, working with agility is to be flexible to change, but also predictable, in order to align work with wider concerns such as marketing campaigns and spinning up teams to support physical processes.

Past experiences of attempting to find expected delivery dates often involved scrum poker, which comes with a lot of baggage, misunderstanding and requires time for the team to settle into a routine. Estimation often becomes a deadline, with teams expected to keep to these dates, even when requirements were minimal at the time!

### Should we still estimate?

Despite being an advocate for #noestimates, it was pointed out to me that the process of estimation is still useful to ensure all the team know what the work item in question involves, and serves as a discussion point to discover unknowns.
