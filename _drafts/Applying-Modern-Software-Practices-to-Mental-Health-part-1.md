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

## In Software

Observability pertains to exposing and visualising how your software is performing, both from a technical viewpoint eg latency and errors, and from a business viewpoint eg orders per week trend.

My current engagement uses DataDog to great effect, aggregating logs and traces from AWS, as well as user activity to build dashboards that visualise how the system is working. Embracing a DevOps culture fosters a "you build it, you run it" mentality, whereby the team is responsible for the keeping the software running.

When there is a known issue that happens regularly, we can compose runbooks that give us a detailed plan on how to remediate the issue. This can then be given to out of hours support to relieve the pressure on the delivery team, enabling them to put in a longer term fix.

## For You

In the same way we want to know when are system is starting to fail before it has a wide effect on our users, we want to be able to recognise when we start to  ;think and behave in a way that might lead to undesirable outcomes. A tool which we can use is being mindful of our thoughts and physical feelings. 

# Ubiquitous Language

Its often said that one of hardest part of software is naming things. Establishing a common (ubiquitous) language helps clarity when discussing the domain within the team, stakeholders and subject matter experts, reducing ambiguity and misunderstanding. A ubiquitous language is a key part of domain-driven design.

# Baby Steps

Taking baby steps refers to the mindset of making small changes to the system, as opposed to large "big bang" updates. This mindset applies to making small refactorings and checking the tests still pass, committing working software and continously deploying it to production, and delivering new features iteratively, and gathering real usage data as you go.

# Context

Context is king; it gives rise to the consultant's default response to all questions "it depends...". You can rely on doctrine some of the way, but to help identify and fix a problem, you need to know its history, where it lies in the wider system, what has been tried before, what pressures were in place when sub-optimal decisions where made, and be mindful of the scars incurred from previous bad experiences.

Context is also important when slicing up the system into bounded domains, and layers within an application. Sharing too much information and responsibilities make code and systems difficult to understand and change.

---

I'll follow this up with a future post with some more themes.
