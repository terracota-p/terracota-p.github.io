---
layout: page
title: Projects
permalink: /projects/
---

Content:

- [Recent work](#recent-work)
  - [Bardavon](#bardavon)
    - [Prevention](#prevention)
  - [Personal - 2023](#personal---2023)
  - [PeerWell](#peerwell)
    - [PeerWell Health](#peerwell-health)
    - [Medical programs v2 - Content management and delivery](#medical-programs-v2---content-management-and-delivery)
    - [Identity management - OAuth2 server](#identity-management---oauth2-server)
    - [Partner API](#partner-api)
    - [Dashboard v2](#dashboard-v2)
  - [Personal - 2021](#personal---2021)
- [Previous work](#previous-work)
  - [Orwell Group](#orwell-group)
  - [Enel Group](#enel-group)
  - [Acotel](#acotel)

## Recent work

### Bardavon

See <https://www.bardavon.com/>

#### Prevention

Workplace injury prevention remarkable undertakings:

- Prevention kiosk app
- New dashboard combining data from task assessments and movement reports
- Rebrand Preventure apps to Bardavon, redesign
- Care Management Portal (inherited) go-live
- Monitoring & alerting
- SOC2 audit

Tech; ts, c#, python, react, remix (SSR), kotlin, android, flutter, github actions, tf, postgresql, mongodb, google cloud run, aws lambdas.

### Personal - 2023

[Svelte playground](https://github.com/terracota-p/val-birthday).

Tech: ts, svelte, css, vercel-kv.

### PeerWell

See <https://www.peerwell.co/>

Tech: ts, js, node, cucumber, jest, mocha, docker, k8s, REST, oauth2, jwt, mongodb, express, nestjs, mongoose, react, redux, jenkins.

#### PeerWell Health

Features to support establishing PeerWell health provider in California, including:

- Patients self-registration, uploading insurance card pics
- EHR integration: sync patients information with _Athena_ Electronic Health Records APIs
- Extend patients management: switch program, partner

#### Medical programs v2 - Content management and delivery

New system for creating and publishing medical programs and define rules for content delivery to patients.

- Enable medical content authors to create medical programs, including phases, modules, cards, and delivery rules.
- Content delivery logic: compute what patients get in their mobile apps, following rules including event (eg: surgery) dates, assessment results, theme variability, etc.
- API:
  - Enable patient-interaction service to get all info needed for actual in a pull-only, pure-function model.
  - Enable author portal content management.
  - OAuth2 (JWT).

#### Identity management - OAuth2 server

OAuth2-capable authentication and authorization server, as platform-wide identity-management system.

- API:
  - `POST /token` endpoint that returns a signed JWT bearer token (following OAuth2 delegated authentication model) including role, that other services can use to verify authentication & authorization by just checking signature and claims contained in token (no per-authentication call to auth server needed).

#### Partner API

Integrate Partner systems with PeerWell in an automated way.

- Enroll, track and manage patients as they progress through PeerWell medical programs until recovery.
- Get valuable medical and compliance data collected in the process, to help the care team take better decisions.
- Register the decisions to release patients when recovered.

#### Dashboard v2

Backoffice portal and API overhaul for partner users and admins.

### Personal - 2021

[kanban board](https://bs-kanban-board.herokuapp.com/), [web RPG (in construction)](https://github.com/terracota-p/bs-tabletop-rpg).

Tech: ts, js, node, express, react, redux, mongodb, REST, jwt.

## Previous work

### Orwell Group

Banking platform:

- In-team and across-teams software engineering lead.
- Registration, Product, Contract, Customer, Payments, AML and other microservices.
- Refactor from a [ball of mud](https://en.wikipedia.org/wiki/Big_ball_of_mud) (entangled microservices hell) to loosely coupled microservices.
- Payments service for FPS, CHAPS, internal account transfers – common interface for payment initiation, indexing and searching.
- PSD2 / OpenBanking PISP and ASPSP solutions, OAuth2 (integrations with PingID and AWS Cognito).
- Distributed payment gateway network: communication using REST, gossip protocol and reactive streams for payment distribution, data exchange, and discovery.
- Infrastructure as code: CICD, EKS, application-supporting environments.

Tech: java, js, node, cucumber, REST, apigee, k8s, AWS, AWS API Gateway, AWS lambdas, spring boot, mariadb, cassandra, kafka, kafka-streams, CICD, solr, storm, jenkins, artifactory.

### Enel Group

E2Bank - Enel-to-Bank customized financial integration product:

- Architecture definition, analysis, version planning, dev team lead.
- Global implementation project E4E.
- Full SAP to E2Bank migration.
- Redefinition of all banking flows (payments, statements, direct debits).

Tech: java ecosystem, oracle DB.

### Acotel

SB - Enterprise-to-Bank financial integration product for Service Bureau (SaaS) and in-house deployment:

- From inception to several years in production: architecture definition, analysis, version planning, dev team lead.
- Integrations for big clients like Abertis Autopistas, Iberdrola, Iberdrola USA, Grifols, Puig, Desigual...

Tech: java ecosystem, oracle DB.
