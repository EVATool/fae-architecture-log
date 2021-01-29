---
type: decision
acronym: dto-pattern
title: >
    A DTO pattern should be used in the APIs
decision_type: should
belongs_to: apis
status: _5_presented
responsible: SBE
deadline: 2021-01-29
history:
    v1:
        date: 2021-01-29
        comment: created initially
---

## Why is there need for such a decision?

If we expose entities over APIs, a uniform architecture helps maintainability.  

## Additional sources for better understanding the background

* [Bente, 2021: Warum Modulith oder Microservice? Inhaltsimpuls FAE](https://ilias.th-koeln.de/goto.php?target=file_1800076_download&client_id=ILIAS_FH_Koeln)

## Viable Options

* Custom-tailored DTO for each UI screen
* no recommendation, each team designs API on its own 


## Alternatives not seriously considered

none


## How is this decision evaluated?

Good practice from literature.

 
## Resolution Details

Recommended pattern can be found in the [EVATool wiki](https://github.com/EVATool/evatool-backend/wiki/APIs).

## Reasons for the resolution

see above, good practice. 



