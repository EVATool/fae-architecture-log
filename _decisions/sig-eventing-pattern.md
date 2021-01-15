---
type: decision
acronym: sig-eventing-pattern
title: >
    Communication Pattern
decision_type: must
belongs_to: eventing
status: _1_open
responsible: KRU;DUZ
deadline: 2021-02-05
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v2:
        date: 2021-01-15
        comment: added reason for decision and possible options
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

* Depending on chosen eventing solution and real payloads which are not yet defined
* TODO: Proof of concept and further research

<!---
(**Before** you start working in this, please write down how you will evaluate this decision, and plan to 
come to a resolution. 
It is  **not sufficient** to perform a brief Google search, and then write  the "result" down. Any decision must
**always** be based on a thorough evaluation - if possible hands-on, i.e. by coding a brief proof-of-concept.
if this doesn't apply, then some other means of proper research must be given here - e.g. an evaluation of 
the most relevant literature or IT community sources.) 
--->
 
 
## Resolution Details

<!---
(If the resolation cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)
--->

## Reasons for the resolution

<!---
(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)
--->
