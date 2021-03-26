---
layout: page
title: Projects
permalink: /projects/
---

Content summary:

- [Recent work](#recent-work)
  - [PeerWell](#peerwell)
    - [Medical programs v2 - Content management and delivery](#medical-programs-v2---content-management-and-delivery)
    - [Identity management - OAuth2 server](#identity-management---oauth2-server)
    - [Partner API](#partner-api)
    - [Dashboard v2](#dashboard-v2)
  - [Personal](#personal)
- [Previous work](#previous-work)
  - [Orwell Group](#orwell-group)
  - [Evolution Invest](#evolution-invest)
  - [Enel Group](#enel-group)
  - [Acotel](#acotel)

## Recent work

### PeerWell

See <https://www.peerwell.co/>

#### Medical programs v2 - Content management and delivery

New system for creating and publishing medical programs and define rules for content delivery to patients.

- Enable medical content authors to create medical programs, including phases, modules, cards, and delivery rules.
- Content delivery logic: compute what patients get in their mobile apps, following rules including event (eg: surgery) dates, assessment results, theme variability, etc.
- API:
  - Enable patient-interaction service to get all info needed for actual in a pull-only, pure-function model.
  - Enable author portal content management.
  - OAuth2 (JWT).

Tech: typescript, node, cucumber, jest, docker, k8s, oauth2, jwt, mongodb, express, nestjs, mongoose, jenkins.

#### Identity management - OAuth2 server

OAuth2-capable authentication and authorization server, as platform-wide identity-management system.

- API:
  - `POST /token` endpoint that returns a signed JWT bearer token (following OAuth2 delegated authentication model) including role, that other services can use to verify authentication & authorization by just checking signature and claims contained in token (no per-authentication call to auth server needed).

Tech: javascript, node, cucumber, mocha, docker, k8s, oauth2, jwt, mongodb, express, jenkins.

#### Partner API

Integrate Partner systems with PeerWell in an automated way.

- Enroll, track and manage patients as they progress through PeerWell medical programs until recovery.
- Get valuable medical and compliance data collected in the process, to help the care team take better decisions.
- Register the decisions to release patients when recovered.

Tech: javascript, node, cucumber, mocha, docker, k8s, oauth2, jwt, mongodb, express, jenkins.

#### Dashboard v2

Backoffice portal and API overhaul for partner users and admins.

Tech: javascript, node, react, redux, mocha.

### Personal

[kanban board](https://bs-kanban-board.herokuapp.com/), [web RPG (in construction)](https://github.com/terracota-p/bs-tabletop-rpg).

Tech: typescript, javascript, node, express, react, redux, mongodb, REST, JWT auth.

## Previous work

### Orwell Group

- API products and Integration tests.
- Registration, Product, Contract, Customer, Payments, AML and other microservices.
- Payments service for FPS, CHAPS, internal account transfers – common interface for payment initiation, indexing and searching (REST, solr, kafka, java, spring boot, storm, cucumber).
- PSD2 / OpenBanking PISP and ASPSP solutions, OAuth2 (REST, apigee API Gateway, lambdas, java, node, integrations with PingID and AWS Cognito).
- Distributed payment gateway network: communication using REST, gossip protocol and reactive streams for payment distribution, data exchange, and discovery (spring boot, kafka, rocksdb).

Tech: java, javascript, node, cucumber, REST, apigee, AWS API Gateway, k8s, spring boot, mariadb, cassandra, kafka-streams, CI/CD.

### Evolution Invest

- Infrastructure as code: CICD, EKS, application-supporting environments.

Tech: terraform, ansible, packer, python, AWS, jenkins, jira, artifactory, k8s.

### Enel Group

- E2Bank Enel-to-Bank customized integration product
  - Global implementation project E4E
  - Full SAP to E2Bank migration
  - Redefinition of all banking flows (payments, statements, direct debits)
  - Architecture definition, analysis, version planning, dev team lead.

Tech: java ecosystem, oracle DB.

### Acotel

- SB Enterprise-to-Bank integration product for Service Bureau (SaaS) and in-house deployment
  - From inception to several years in production: architecture definition, analysis, version planning, dev team lead
  - Integrations for big clients like Abertis Autopistas, Iberdrola, Iberdrola USA, Grifols, Puig, Desigual...

Tech: java ecosystem, oracle DB.
