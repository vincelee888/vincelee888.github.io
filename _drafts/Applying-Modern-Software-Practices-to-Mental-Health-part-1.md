---
title: Applying Modern Software Practices to Your Mental Health
categories:
  - software
  - mental health
tags:
  - observability
  - mindfulness
  - mental health
---

Throughout my mental health journey over the years, I have come to realise the overlap of practices I do in my day job as a software engineer, and processes around maintaining good mental health. In this post I'll start to outline the common themes, and hope it will help anyone else in the industry recognise the practices and be able to apply them to help themselves.

# Observability (o11y)

Observability pertains to exposing and visualising how your software is performing, both from a technical viewpoint eg latency and errors, and from a business viewpoint eg orders per week trend.

My current engagement uses DataDog to great effect, aggregating logs and traces from AWS to build dashboards that visualise how the system is working. Embracing a DevOps culture fosters a "you build it, you run it" mentality, whereby the team is responsible for the keeping the software running.

# Ubiquitous Language

Its often said that one of hardest part of software is naming things. Establishing a common (ubiquitous) language helps clarity when discussing the domain within the team, stakeholders and subject matter experts, reducing ambiguity and misunderstanding. A ubiquitous language is a key part of domain-driven design.

# Baby Steps

Taking baby steps refers to the mindset of making small changes to the system, as opposed to large "big bang" updates. This mindset applies to making small refactorings and checking the tests still pass, committing working software and continously deploying it to production, and delivering new features iteratively, and gathering real usage data as you go.

# Context

Context is king; it gives rise to the consultant's default response to all questions "it depends...". You can rely on doctrine some of the way, but to help identify and fix a problem, you need to know its history, where it lies in the wider system, what has been tried before, what pressures were in place when sub-optimal decisions where made, and be mindful of the scars incurred from previous bad experiences.

Context is also important when slicing up the system into bounded domains, and layers within an application. Sharing too much information and responsibilities make code and systems difficult to understand and change.

# Root Cause Analysis

Inevitably, all systems fail. The sign of a good system and teams that support it, is the speed at which the problem is identified and fixed. Once operations have returned to normal, it is good to perform a root cause analysis, to ascertain why it happened. (Nowadays, this is referred to as a blameless post-mortem, but in a good team and organisation, no blame should be the default!)

It is not enough to act upon "the site went down because the newbie deleted the production database!". An3 investigation should take place to find the root cause. A standard method is Five Whys - ask why something happened, and after five iterations you should have found a number of actions that will return higher value than the immediate problem. 


# Ease of Change

# Systems Thinking

# From Project to Product
