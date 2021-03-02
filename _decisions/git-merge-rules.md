---
type: decision
acronym: git-merge-rules
title: >
    Rules regarding Git-Merge (Merge-Workflow)
decision_type: should
belongs_to: devops
status: _5_presented
responsible: TZA    
deadline: 2021-03-02
history:
    v1:
        date: 2021-02-26
        comment: created initially
---

## Why is there need for such a decision?

The development teams should agree on a workflow for merging new developed code at first
into a `dev` branch and then into `main`. This workflow should prevent numerous errors that
can emerge during a merge. The main goal of this is that no non-working state ends up in the `main` branch.

## Additional sources for better understanding the background
n/a

## Viable Options
n/a

## Alternatives not seriously considered
n/a

## How is this decision evaluated?

The decision is based on a discussion and an analysis of possible problems during testing and merging.
 
## Resolution Details

Wiki: [Merge-Workflow for Git](https://github.com/EVATool/evatool-backend/wiki/DevOps-Merge-Workflow)

## Reasons for the resolution

Experience and general good practice.

