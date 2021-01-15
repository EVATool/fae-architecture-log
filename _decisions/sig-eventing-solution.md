---
type: decision
acronym: sig-eventing-solution
title: >
    Comparison between different Event-Streaming Solutions
decision_type: must
belongs_to: eventing
status: _1_open
responsible: AKO
deadline: 2021-01-22
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v2:
        date: 2021-01-15
        comment: added reason for decision and possible options
---

## Why is there need for such a decision?

A multitude of possible eventing solutions exist on the market. While most solutions have very similar
functionality at their core, the different subsystems have to agree to use the same program, to be able to 
communicate well with each other. 

## Additional sources for better understanding the background

* [Sebastian Gauder - Eventing Presentation](https://www.doag.org/formes/pubfiles/9948769/2018-NN-Sebastian_Gauder-Eventing_mit_Apache_Kafka__Haben_ist_besser_als_Brauchen-Praesentation.pdf)
* [Apache Kafka](https://kafka.apache.org/)
* [RabbitMQ](https://www.rabbitmq.com/)
* [Spring Events](https://www.baeldung.com/spring-events)

## Viable Options

* Apache Kafka
    * Market Leader
    * Eventing solution with the highest adoption

* RabbitMQ
    * Lighter Version of Kafka
    * Functional very similar but lacking the in-depth analysis and monitoring tools

* Spring Eventing
    * Rather unknown eventing solution
    * Might be useful to avoid using additional software besides Spring, which we already use 

## Alternatives not seriously considered

* Amazon Kinesis?
* IBM Event Streams / Cloud Pak for integration
* Google Cloud Dataflow

None of these are open-source solutions which would limit us in our own open-source project.
Additionally, all of these are specialized for use in their respective cloud environments or need a paid license.

## How is this decision evaluated?

TODO: Proof of concept
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
