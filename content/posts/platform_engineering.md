---
title: Building an Internal Platform Engineering Team, Why and How
date: 2023-04-01T22:58:33+02:00
draft: false
tags:
    - platform
    - devexp
    - organization
    - developer
---

## Introduction

In this article, we will explore the concept of platform engineering and its importance in modern software development organizations. We will discuss the problems it aims to solve, provide a real-world example, and offer some tips on building an effective platform engineering team.

## A Story Before We Start

Before diving into the topic of platform engineering, let's consider a story that illustrates the problem it aims to solve.

*The story of Namira and her struggles with creating a database*

1. Namira, a software engineer, joins a new company and is assigned to bootstrap a new service for the recommendation API.
2. To create a database for the service, she is instructed to submit a ticket to the DB team.
3. The DB team assigns the ticket to Felix, who requests additional information from Namira.
4. Namira, busy with Q1 planning, takes a couple of days to respond.
5. Felix creates the database and forwards the ticket to the identity and access team.
6. Sophia, from the identity and access team, creates a service account and asks Namira about the database's purpose.
7. Namira informs her that the database will be used by her application in Kubernetes (k8s).
8. Sophia routes the ticket to the Vault team to set up the password in Vault and enable the k8s operator to read it.
9. Hassan from the Vault team completes the task and marks the ticket as "DONE!"
10. Namira deploys a test application, only to encounter an error: "Cannot Resolve the Host."
11. The team realizes the database is in the wrong Availability Zone (AZ) and asks Namira to create tickets for a new database in the correct AZ and decommissioning the old one.
12. Namira becomes frustrated and demotivated by the convoluted process.


## The Problem

The story of Namira highlights several issues that software development teams may face:


1. **Fragmented processes**: Each team completes their work, but the overall process is disjointed and cumbersome for Namira, who is trying to create a new service.
2. **Decreased productivity**: Namira spends a significant amount of time and energy navigating the process, leaving her with less time and motivation to focus on her primary tasks.
3. **Lack of a clear, efficient workflow**: The story assumes that teams correctly route tickets to the next team, but in reality, engineers like Namira might struggle to determine the next step or team involved in the process.
4. **Limited scope**: The story only covers the creation of a database, without considering other aspects such as messaging or additional infrastructure requirements.


To address these challenges, organizations can turn to platform engineering.

## What is Platform Engineering?

Platform engineering is about building products that combine one or more infrastructure systems to enable self-service capabilities for engineers. It focuses on switching from an "Ops" mindset to a "Product" mindset, delivering turn-key solutions for engineers and creating a "paved" path for them.

The goal of platform engineering is not to create fancy tools or deploy additional software in production. Instead, it aims to help the majority of engineers be more productive and deliver business value much faster, enabling the business to move quickly.

## The Benefits of Platform Engineering

With a well-implemented platform engineering approach, Namira's story could have been quite different:

1. Namira fills out a form in a UI or CLI with some inputs.
2. She waits for 5 minutes.
3. She gets everything ready to use immediately, without tickets, queues, or the need to navigate the organization tree for multiple teams.

## Building a Platform Engineering Team

Creating a successful platform engineering team involves more than just assembling a group of talented individuals. It requires cultivating a unique team culture that supports the goals and values of platform engineering. Here are some key aspects to consider when building a platform engineering team:

### 1. Good Communication

Effective communication is crucial for a platform engineering team. The team members, including managers, engineers, and product managers, should be able to communicate well, listen attentively, and establish connections. They need to directly engage with feature-making engineering teams and understand their pain points. A few ideas to enhance communication within the team include:

- Conducting customer interviews with engineers from various teams, both senior and junior.
- Embedding platform team members within other teams to experience their daily challenges firsthand.
- Establishing strong relationships with SRE teams and working closely with them as partners.

### 2. Focus on MVPs (Minimum Viable Products)

Since platform teams indirectly impact the business through feature teams, they should avoid embarking on extensive projects without testing the waters first. The platform team should be able to create MVPs to test ideas and gauge their viability. This allows them to make necessary adjustments to their plans based on the feedback gathered after each MVP. They should be open to conducting small, action-driven experiments that help them assess the feasibility of their ideas.

### 3. Validation and Measurement

Platform teams must validate their assumptions and measure the impact of their work. It is not enough to simply "ship" a product and move on. They need to ensure that the tools they build truly benefit the intended users. A few approaches to validate and measure the team's work include:

- Inviting feature engineers to use new capabilities and observing their experiences firsthand.
- Using OKRs or measurable outcomes to assess the impact of a tool before and after its release.
- Relying on metrics such as [DORA metrics](https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance) or [The golden four as mentioned in the Accelerate book](https://www.goodreads.com/en/book/show/35747076) to evaluate the team's performance.

### 4. Strong Leadership

Leadership plays a vital role in shaping the platform engineering team's culture. Leaders should support the team's efforts to build a strong culture, foster a sense of psychological safety, and provide the necessary resources for success. Without strong leadership, the entire foundation of the platform engineering team may crumble.

## Conclusion

Platform engineering can address many of the challenges faced by modern software development teams. By building a strong platform engineering team and fostering a culture that supports their goals, organizations can improve productivity and deliver business value more quickly.

## References

* [DORA metrics](https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance)
* [The accelerate book](https://www.goodreads.com/en/book/show/35747076)
* [Crossing the chasm](https://www.goodreads.com/book/show/61329.Crossing_the_Chasm)
* [Google SRE toil definition](https://sre.google/sre-book/eliminating-toil/)
* [The Unicorn Project Book](https://www.goodreads.com/en/book/show/44333183)
* [CNCF Cloud Native Interactive Landscape](https://landscape.cncf.io/)
