---
type: decision
acronym: sig-eventing-pattern
title: >
    Communication Pattern
decision_type: must
belongs_to: eventing
status: _2_draft
todos:
    - how would you plan a PoC to evaluate? 
responsible: KRU;DUZ
deadline: 2021-02-05
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v2:
        date: 2021-01-15
        comment: added reason for decision and possible options
    v3:
        date: 2021-01-22
        comment: added "how is this decision evaluated" & changed status
---

## Why is there need for such a decision?

The system is based on a modulith design-pattern and all subsystems should communicate with each other asynchronously.

## Additional sources for better understanding the background

* [Sebastian Gauder - Eventing Presentation](https://www.doag.org/formes/pubfiles/9948769/2018-NN-Sebastian_Gauder-Eventing_mit_Apache_Kafka__Haben_ist_besser_als_Brauchen-Praesentation.pdf)
* Sieben Weggabelungen - Wegweiser im DDD-Dschungel (Stefan Bente, et al)
* [What do you mean by “Event-Driven”?](https://martinfowler.com/articles/201701-event-driven.html)

## Viable Options

* Communication-Patterns
    * "Full-Payload"    - Event carried state Transfer
    * "ID-Only"         - Event Notification
    * "Delta-Only"      - Event Sourcing

## Alternatives not seriously considered

* Synchronous Communication
    * Not applicable for eventing
    * Not wanted in this system

## How is this decision evaluated?

* The decision which pattern will be used, is based on the results of the two decisions made of the eventing solution and the domain research process. 
* The "event notification" pattern won't be used, since it can be estimated that the total payload will be very manageable.
 
## Resolution Details

<!---
(If the resolation cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)
--->

## Reasons for the resolution

<!---
(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)
--->
