---
type: decision
acronym: single-project-folder
title: >
    Single module project
decision_type: must
belongs_to: devops
status: _5_presented
responsible: JSP
deadline: 2021-02-19
history:
    v1:
        date: 2021-02-19
        comment: created initially
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

The decision is changed after a discussion that resulted from problems initially choosing a root source folder with a module folder containing source folders for each subdomain.
 
## Resolution Details

It was decided to use a root src-folder, but packages for every sub-domain.
* the root src-folder is only starting the application with a main-class. 
* every sub-domain have a folder in the root src-folder. 

## Reasons for the resolution

The root src-folder with modules-folder is more like the modulith system as the one src-folder with packages
for every sub-domain. First we used this structure, but become problems with spring-configurations. So it was decided to use only one src-folder
with a package structure for every domain.

[wiki](https://github.com/EVATool/evatool-backend/wiki/Repo-structure)

[branching-rules](https://evatool.github.io/fae-architecture-log/decisions/branching-strategy.html)
