---
type: decision
acronym: location-for-events
title: >
    Events need to be defined in a public package within the domain
decision_type: must
belongs_to: eventing
status: _5_presented
responsible: JLÜ
deadline: 2021-02-19
todos:
    
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
    v4: 
        date: 2021-02-19
        comment: update wiki
---

## Why is there need for such a decision?

Events used by the domains need to be visible for the other domains. In order to achieve this, a not domain specific structure
has to handle the events. 

## Additional sources for better understanding the background

n/a


## Viable Options

* the project includes a package global to store events


## Alternatives not seriously considered

n/a



## How is this decision evaluated?

n/a
 
## Resolution Details

Due to the change in the project structure a different approach for events is needed.
The package global will be a package within the application. All domains have to store the events in the subpackage 'event'.

The resolution is described in the [wiki](https://github.com/EVATool/evatool-backend/wiki/eventlocation).



## Reasons for the resolution

n/a
