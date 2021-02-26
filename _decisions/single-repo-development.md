---
type: decision
acronym: single-repo-development
title: >
    Development model is "Single Repo"
decision_type: must
belongs_to: devops
status: _5_presented
responsible: JSP;SBE
deadline: 2021-01-29
history:
    v1:
        date: 2021-01-15
        comment: created initially
    v2: 
        date: 2021-01-22
        comment: scope enhanced (includes also branching rules)
    v3: 
        date: 2021-01-22
        comment: updated the deadline
    v4: 
        date: 2021-01-23
        comment: decide decision
    v5: 
        date: 2021-01-29
        comment: done todos
    v6: 
        date: 2021-02-19
        comment: rename decision
    v7: 
        date: 2021-02-19
        comment: corrected text   
---

## Why is there need for such a decision?

This decision is important, because it will decide how the project will store in git. 


## Viable Options

* single repo
* one repo for every sub-domain (multi-repo)

## How is this decision evaluated?

The decision is based on a history of the project structure.
 
## Resolution Details

There will be one repo for the whole project at [git](https://github.com/EVATool/evatool-backend/).

## Reasons for the resolution

To understand this decision it is good to know the project structure
[project structure](https://evatool.github.io/fae-architecture-log/decisions/single-project-folder.html)
with his history.
The fact that there is only one src folder with domain packages eliminates the need for a multi-repo.

[branching-rules](https://evatool.github.io/fae-architecture-log/decisions/branching-strategy.html)
