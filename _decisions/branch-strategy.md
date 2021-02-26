---
type: decision
acronym: branch-strategy
title: >
    Branch strategy during development
decision_type: must
belongs_to: devops
status: _5_presented
responsible: TZA;JSP;AKO    
deadline: 2021-01-29
history:
    v1:
        date: 2021-01-22
        comment: created initially
    v2:
        date: 2021-01-22
        comment: quick resolution
---

## Why is there need for such a decision?

All domain-teams have to agree on rules regarding the shared git-environment to avoid conflicts
and assign responsibilities during each step.

## Additional sources for better understanding the background


## Viable Options

* One branch per sub-domain vs. master-only
    * No convention enforced within a sub-domain
         
* main-branch + dev-branch + domain-branches
    * Each group merges into dev-branch once a feature is done
    * dev-branch gets merged into master once tests are successful on github as well

## Alternatives not seriously considered

* Pull-Requests
    * Next group responds to request
    * All requests get merged fridays

Pull-Requests are too much effort with sub-domain teams that would have to synchronize their work.

## How is this decision evaluated?

The decision is based on a discussion and an analysis of possible problems during testing and merging. 
 
## Resolution Details

* Domain-branches would be a useful feature because they follow the project structure.
* Each team merges theirs features into dev-branch themselves. 
    This requires a definition of done (e.g. successful Maven tests).
* dev-branch + master-branch
    * dev-branch gets merged into master once tests are successful on github as well.

See also: [Rules regarding Git-Merge](./git-merge-rules)

## Reasons for the resolution

Reasons are given in the resolution details.

