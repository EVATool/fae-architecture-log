---
type: decision
acronym: sig-eventing-communication-pattern
title: >
    Communication pattern for events is "Full-Payload" 
decision_type: must
belongs_to: eventing
status: _5_presented
todos:
responsible: KRU;DUZ
deadline: 2021-02-05
todos:
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
    v4:
        date: 2021-02-03
        comment: added resolution details and reasons
    v4:
        date: 2021-02-03
        comment: checked by stakeholder
    v5: 
        date: 2021-02-05
        comment: presented
    v6:
        date: 2021-02-19
        comment: completed todos
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

* The decision which pattern will be used, is based on the results of the two decisions made of the "Eventing Solution", and the domain research process. 
* The "event notification" pattern won't be used, since it can be estimated that the total payload will be very manageable.
 
## Resolution Details

We choose the pattern "Full-Payload" (Event carried state Transfer) for the internal communication, between the components.

General Information and an Example can be found in the [wiki](https://github.com/EVATool/evatool-backend/wiki/Communication-Pattern-is-Full-Payload).

## Reasons for the resolution

The main reason behind the decision was that the current solution "Spring Eventing" can't provide the other two communication-pattern.
In addition, the expected data throughput of this project isn't extensive enough that the "Delta-only" (Event Sourcing) pattern is needed.