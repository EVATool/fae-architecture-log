---
type: decision
acronym: async-over-sync
title: >
    Asynchronous over synchronous communication for all sub-domains
decision_type: must
belongs_to: eventing
status: _5_presented
responsible: SBE
deadline: 2021-01-29
history:
    v1:
        date: 2021-01-15
        comment: created initially
    v2:
        date: 2021-01-15
        comment: Modulith style presented to the whole group as a motivation        
---

## Why is there need for such a decision?

This is a fundamental architecture style choice, influencing the whole development process.

## Additional sources for better understanding the background

* [Bente, 2021: Warum Modulith oder Microservice? Inhaltsimpuls FAE](https://ilias.th-koeln.de/goto.php?target=file_1800076_download&client_id=ILIAS_FH_Koeln)

## Viable Options

* Async over sync
* no async communication, all synchronous calls


## Alternatives not seriously considered

-


## How is this decision evaluated?

Based on the choice for the general architecture style.

 
## Resolution Details

See [architecture style description](https://github.com/EVATool/evatool-backend/wiki/Architecture-Style). 

## Reasons for the resolution

Is a direct consequence from the [Modulith decision](./modulith).  

