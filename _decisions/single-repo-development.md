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
todos: 
    - please adapt the text (decision now covers only the repo, not the project structure)
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
---

## Why is there need for such a decision?

This decision is important, because it will decide which project structure will be. 


## Viable Options

* single src-folder with packages for every sub-domain
* one root src-folder with a modules-folder which have src-folders for every sub-domain.


## Alternatives not seriously considered

* one repo for every sub-domain (multi-repo), was ruled out as too complex, since we deploy in one piece 
    (see [Modulith decision](./modulith))


## How is this decision evaluated?

The decision is based on a discussion, and the decision for the branching-strategy (both was decided at the same day).

 
## Resolution Details

It was decided to use a root src-folder, but a modules-folder with a src-folder for every sub-domain.
* the root src-folder is only use for classes that every sub-domain use. 
Nobody of the sub-domains can be an owners of those classes.
* every sub-domain have a folder in the modules-folder. This sub-domains have own src-,
test-,resource-folder and an individual .pom file with the project as parent.

## Reasons for the resolution

The root src-folder with modules-folder is more like the modulith system as the one src-folder with packages
for every sub-domain. For this reason, the sub-domains are more encapsulated from each other.

[wiki](https://github.com/EVATool/evatool-backend/wiki/Repo-structure)

[branching-rules](https://evatool.github.io/fae-architecture-log/decisions/branching-strategy.html)
