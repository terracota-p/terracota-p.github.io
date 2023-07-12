---
layout: post
title: "My preferred development process"
date: 2023-07-12
categories: SDLC
---

In my experience, this is a nice and lean development process.

- Related to [CICD, continuous delivery](/sdlc/2023/06/30/cicd.html) (previous article).
- Based on agile (scrum), BDD, continuous delivery, trunk-based development; as described below.

## Definition of ready

A story is ready to be included in the sprint if it complies with:

- Acceptance criteria:
  - Written in description, agreed between PO and devs.
  - Scenarios: how would an end-user test the story once done? Examples.
    - Ideally, written and agreed as a BDD spec (that requires the PO to write them in the first place); if not possible to fully do it at this point, complete it later on (see below).
- Team-reviewed in planning/grooming session:
  - Split into smaller stories if needed.
  - Estimated.
    - Proposed alternative: no-estimates (ie: count the number of stories/tasks completed in a sprint on average).

Once ready, stories are planned and then the sprint is started (in the sprint planning meeting).

## Build

Steps taken by devs for building a story that was committed into the sprint:

- Acceptance tests (BDD scenarios):
  - Write them early when the story is started (before any other work, as they drive what is built).
  - Share them with PO, agree.
- Analysis, design:
  - Draft what needs to be done, break down the story into subtasks.
  - Write a very light design document if needed (ie: if the solution has pros and cons or is sufficiently complex), at this point or further down the build phase:
    - Aim is to share with the dev team relevant design decisions, and collectively select the best options.
- Build:
  - For each subtask.
  - BDD - Automate acceptance tests:
    - API: acceptance tests (with [cucumber](https://cucumber.io/ "https://cucumber.io/") for example).
    - Frontend: E2E tests (with [cypress](https://www.cypress.io/ "https://www.cypress.io/") for example).
  - PR reviews:
    - Test evidence in staging.
      - Feature branch automatically deployed by CICD.
      - Acceptance tests green.
  - Merge:
    - To main branch.
- Done:
  - Test evidence in staging.
    - Main branch automatically deployed by CICD.
    - Acceptance tests green.
  - Notify PO.
  - Ready in staging to (optionally) be tested outside the dev team.

## Definition of done

A story is complete (from the dev standpoint) if it complies with:

- Acceptance tests:
  - Written in the story, agreed between PO and devs.
  - [BDD](https://en.wikipedia.org/wiki/Behavior-driven_development):
    - Scenarios:
      - Executable specifications.
      - How an end-user would test the system to prove it’s working as expected once the story is done.
      - Written using [Given-When-Then](https://en.wikipedia.org/wiki/Given-When-Then) semi-structure.
  - Alternative: agreeing on acceptance tests could be considered part of the “definition of ready”, and done before adding a story to the sprint.
    - This would be more ideal, but would require PO (rather than the dev) writing them in the first place.
- Deployed to staging.
- Merged to main branch (all changed apps).
- Test evidence for the acceptance tests in staging:
  - Automated (if possible) or manual (for parts that could not be automated or require double-check).
- PO notified:
  - Mention in story comment that the story is done.
  - Alternatively, marking the story “CLOSED” can be used as a notification, when PO is reporter or watcher in the story.

### Releasable

A **done story** (or parts of it that have been merged) is **releasable** at any time.

- Note this is an application of [optimistic locking](https://en.wikipedia.org/wiki/Optimistic_concurrency_control), based on:
  - Trust between PO and devs.
  - Automated testing (including no-regression).
  - Usage of feature branches when needed (to not activate a feature in prod until desired, even if the code is deployed).
  - Backwards compatibility: always avoid breaking changes, for independence between apps and preventing bugs.

## Acceptance

As per “definition of done” section, implicit acceptance can be considered after PO is notified.

Explicit - In sprint review meeting, completed stories are:

- Demonstrated (show attached test evidence or live demo).
- Accepted or rejected (reopened) by PO.
- Sprint closed.

## Release (deploy to prod)

[Continuous Delivery](https://continuousdelivery.com/): release as frequently as possible.

> get changes into production, \[…\] _safely_ and _quickly_ in a _sustainable_ way

All code in main branch is considered releasable at any time.

Can be done either:

- Routinely:
  - Once per sprint, deploy to prod all apps changed since last deployment to prod.
- On demand:
  - When convenient for any reason (eg: bugfix or anything else).

Only code versions marked as accepted in staging (acceptance / E2E tests green in CICD) can be deployed to prod.

- Enforced in deploy to prod pipelines.
