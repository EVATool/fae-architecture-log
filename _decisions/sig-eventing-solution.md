---
type: decision
acronym: sig-eventing-solution
title: >
    Spring eventing is used as Eventing Solution
decision_type: must
belongs_to: eventing
status: _5_presented
todos:
responsible: AKO
deadline: 2021-01-22
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v2:
        date: 2021-01-15
        comment: added reason for decision and possible options
    v3:
        date: 2021-01-22
        comment: added a resolution and resolution details
    v4:
        date: 2021-02-19
        comment: completed todos and added link to wiki
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

After building small proof of concepts, we will evaluate this decision based on the experienced features and issues.
The proof of concepts are designed to be very similar to the actual use case. So in this case:

* Sending and receiving events on a single server
* JSON Strings as payload
* No additional monitoring features
 
## Resolution Details

We recommend **Spring Eventing** as a solid default, since it is already included in the spring-web libraries we already use.
RabbitMQ presents a viable alternative, should the need arise for a broker based eventing solution 
(docker container highly recommended). 

General Information and Code Examples can be found in the [wiki](https://github.com/EVATool/evatool-backend/wiki/Spring-Eventing).

## Reasons for the resolution

Spring Eventing and RabbitMQ are both good solutions for this project. Both provide everything we need with only a 
few additional features as overhead. Kafka on the other hand provides a huge amount of tools for analysing and 
monitoring event traffic, which might be useful in a huge microservice landscape, but is way too heavy for a small 
project such as this.
