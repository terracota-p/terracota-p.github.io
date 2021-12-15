---
layout: post
title: "Retrospective - My first year in PeerWell"
date: 2021-07-14
categories: retrospective
---

Personal retrospective from the time I joined PeerWell (end of Apr 2020) till now (Jul 2021).

Overall, a very positive outcome.

## Liked

Some things I contributed that I remember and am proud of (in no particular order):

- Speed up CICD pipeline **from >1h to ~18min**. Keys for improvement were:
  - parallel acceptance tests (independent scenarios by design)
  - parallel integration tests (spawn an in-mem DB server for each test worker, to tackle non-independent legacy scenarios)
- Big refactor to replace problematic queue with **crash-proof eventual consistency**
- New microservices, including service boundary with a DDD approach
- **Partner API** - a pull-only API designed for automatic integration of corporate systems with PeerWell
- **OAuth2** client credentials grant, **A2A** auth schema with PKI
- Introduced **BDD**, **TDD** and **agile**
- Introduced **openapi**
- Promoted [**continuous delivery**](https://continuousdelivery.com/) and [**trunk based development**](https://trunkbaseddevelopment.com/)
- **Monitoring & alerting**
- **K8s migration** - Refactor apps as per [12factor](https://12factor.net/) principles for scalability and maintainability (eg: stateless services with externalized config)
- Big refactor to move **from coffeescript to js** to use best-of-breed tools
- Solved some **hard to diagnose bugs and system issues** involving all software components
- **Dashboard 2** - For workerscomp corporate and care team users
- **Patients self registration**

## Learned

Gained experience in:

- js and ts, FP, clean code and architecture
- eventual consistency, DDD
- k8s
- CICD with jenkins
- Monitoring & alerting
- helm - I hadn’t used before

## Loathed

- Lack of transactions in AWS version of mongoDB
- A bit of coffeescript

## Longed for

Things that I’d like to improve:

- Frontend - I’d like to do more
- GraphQL
- Personal projects - Find a little time to move them forward
- Haven’t read much books of CS this year, just some parts of _Composing Software (Eric Elliott)_ and _Agile Coaching (Rachel Davies)_ - Though I’m glad I’ve been heavily applying concepts from previous readings like _Continuous Delivery (Jez Humble)_, _Building Microservices (Sam Newman)_ or _Clean Architecture (Robert C. Martin)_.
