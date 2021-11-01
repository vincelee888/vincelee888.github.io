---
title: Attack the Bottleneck
categories:
  - software
tags:
  - agile delivery
  - metrics
---

I was recently introduced to Actionable Agile, a tool to gather metrics around your delivery process. it comes as a plugn for jira and imports your data to analyse and report on 4 metrics:

* cycle time - the time it takes for a work item to be deployed to live; low is good
* throughput - the rate at which items are deployed to live over a given time period; high is good
* work in progress (WIP) - the number of work items that are in flight and not yet completed; low is good
* work item age - the time a given work item is in progress for; low is good

Assuming we are working on the change that is deemed most valuable to our users, and our work items are deemed 'done' when it has been released to the production environment - the faster we get that valuable change out to our users the better. Reducing the amount of work going on at the same time (WIP) reduces the chance of time-wasting context switching when we have to re-work an item because of bugs, merge conflicts and determining which change has caused a bug. Reducing the size of work items reduces the amount the new work deviates from the working software, and reduces the time taken to receive feedback on that change.

## What about Accelerate?

We can compare these with another modern set of metrics from the DevOps Research and Assessment (DORA) group aka the Accelerate metrics: 

* lead time - the time it takes for a work item to be released to the customer; this is AA's cycle time.
* number of deployments - the number of deployments to live that are made over a given time; this is the same as AA's throughput
* change failure rate - the ratio of unsuccessful to successful deployments
* mean time to recovery (MTTR) - the time taken to resolve and issue in production

# Glossary

* Production/Live - the environment that your users access eg not a test environment
* Context switching - the negative effect of having to pull yourself out of the flow of one piece of work, and get up to speed with another. Usually caused by "multi-tasking", having to fix a bug in a recent release, or being interrupted by the dreaded "just a quick one...".
