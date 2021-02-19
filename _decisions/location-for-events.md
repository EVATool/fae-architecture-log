---
type: decision
acronym: location-for-events
title: >
    Events need to be defined in module global
decision_type: must
belongs_to: eventing
status: _2_draft
responsible: JLÜ
deadline: 2021-02-19
history:
    v1:
        date: 2021-01-08
        comment: created initially
    v2:
        date: 2021-02-19
        comment: add link to wiki
---

## Why is there need for such a decision?

Events used by the domains need to be visible for the other domains. In order to achieve this, a not domain specific structure
has to handle the events. 

## Additional sources for better understanding the background

n/a


## Viable Options

* add a global module to store the events  


## Alternatives not seriously considered

n/a



## How is this decision evaluated?

n/a
 
## Resolution Details

how to use and to store the events can be found in the [wiki](https://github.com/EVATool/evatool-backend/wiki/eventstructure).


## Reasons for the resolution

