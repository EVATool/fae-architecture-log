---
type: decision
acronym: location-for-events
title: >
    Events need to be defined in a public package within the domain
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
    v3:
        date: 2021-02-19
        comment: change decision due to change in project structure
---

## Why is there need for such a decision?

Events used by the domains need to be visible for the other domains. In order to achieve this, a not domain specific structure
has to handle the events. 

## Additional sources for better understanding the background

n/a


## Viable Options

* the domain packages include a public package for events


## Alternatives not seriously considered

n/a



## How is this decision evaluated?

n/a
 
## Resolution Details

Due to the change in the project structure a different approach for events is needed.
Instead of having a 'global' module to save  the events. The events now will be stored in the domain specific packages.
This package must be public, so the other domains can access the defined events.



## Reasons for the resolution

n/a
