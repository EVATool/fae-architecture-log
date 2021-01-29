---
type: decision
acronym: single-repo-development
title: >
    Development model is "Single Repo" / "Single Spring Project" in the evatool-backend Repository
decision_type: must
belongs_to: devops
status: _2_draft
todos: 
    - brief description in the wiki?
    - link to branching rules  
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
        comment: updated deadline
    v4: 
        date: 2021-01-23
        comment: decide decision
    v5: 
        date: 2021-01-29
        comment: done todos
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

The decision is based on a discussion and the decision for the branching-stratagy (both was decided at the same day).

 
## Resolution Details

It was decide to use a root src-folder, but a modules-folder with a src-folder for every sub-domain.
* the root src-folder is only use for classes that every sub-domain use. 
Nobody of the sub-domains can be a owner of that class.
* every sub-domain have a folder in the modules-folder. This sub-domains have there own src-,
test-,resource-folder and an indiviual .pom with the projact as parent.

## Reasons for the resolution

The root src-folder with modules-folder is more like the modulith system as the one src-folder with packages
for every sub-domain. For this reason, the sub-domains are more encapsulated from each other.

[wiki](https://github.com/EVATool/evatool-backend/wiki/Repo-structure)

[branching-rules](https://evatool.github.io/fae-architecture-log/decisions/branching-strategy.html)