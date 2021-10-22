---
layout: page
title: Experience
permalink: /experience/
---

Content:

- [Work](#work)
  - [2020-present - Senior, then Lead engineer @ PeerWell (remote, US)](#2020-present---senior-then-lead-engineer--peerwell-remote-us)
  - [2017-2020 - Senior, then Principal engineer @ Orwell Group (remote, UK)](#2017-2020---senior-then-principal-engineer--orwell-group-remote-uk)
  - [2015-2017 - Development team leader @ Acotel / Exceltia (Spain)](#2015-2017---development-team-leader--acotel--exceltia-spain)
- [Education](#education)
  - [2006 - Computer science engineer (Bachelor's degree)](#2006---computer-science-engineer-bachelors-degree)

## Work

Recent experience.

### 2020-present - Senior, then Lead engineer @ [PeerWell](https://www.peerwell.co/) (remote, US)

Medical platform for recovering from, preparing for, and preventing musculoskeletal surgeries.

[Key contributions](/retrospective/2021/07/14/year-retrospective.html):

- Speed up **CICD** pipeline **from >1h to ~18min**
- New **microservices**, defining service boundaries following DDD approach
- Big refactors like:
  - Replace problematic queue with **crash-proof eventual consistency**
  - Move **from coffeescript to js** to use best-of-breed tools
- **Partner API** - a pull-only API for automatic integration of corporate systems with PeerWell
- **OAuth2** with PKI-signed JWTs, **A2A** auth schema with client credentials grant
- Introduced **BDD**, **TDD**, **agile**, contract-first **openapi** spec
- Promoted [**continuous delivery**](https://continuousdelivery.com/) and [**trunk based development**](https://trunkbaseddevelopment.com/)
- **Monitoring & alerting**
- **K8s migration** - Refactor apps as per [12factor](https://12factor.net/) for scalability and maintainability (eg: stateless services with externalized config)
- Solved some **hard to diagnose bugs and system issues** involving many software components
- Epics like:
  - **Dashboard 2** (for workerscomp corporate and care team users)
  - **Patients self registration**

Tech: js/ts, node, cucumber, docker, k8s, mongo, jenkins, datadog.

### 2017-2020 - Senior, then Principal engineer @ Orwell Group (remote, UK)

Banking core platform.

Key contributions: development of core banking functionalities involving customer data management, payment processing, APIs
microservices overhaul, migrate to k8s...

Tech: java, storm, docker, k8s, cassandra, mariadb, terraform, jenkins, prometheus.

### 2015-2017 - Development team leader @ Acotel / Exceltia (Spain)

B2B, C2B financial integration system and saas.

Key contributions: development team lead, inter-team coordination.

Tech: java, oracle.

## Education

### 2006 - Computer science engineer (Bachelor's degree)
