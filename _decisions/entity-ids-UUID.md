---
type: decision
acronym: entity-ids-uuid
title: >
    UUIDs are to be used for Entity IDs (PKs and API IDs)
decision_type: must
belongs_to: apis
status: _5_presented
responsible: SBE
deadline: 2021-01-29
history:
    v1:
        date: 2021-01-22
        comment: created initially
    v2:
        date: 2021-01-29
        comment: ready to present        
---

## Why is there need for such a decision?

If we expose entities over APIs and events, a uniform way of dealing with IDs is very helpful.  

## Additional sources for better understanding the background

* [Harrison (2017): UUID or GUID as Primary Keys? Be Careful!](https://tomharrisonjr.com/uuid-or-guid-as-primary-keys-be-careful-7b2aa3dcb439)
* [Sikkema (2009): JPA implementation patterns: Using UUIDs as primary keys](https://xebia.com/blog/jpa-implementation-patterns-using-uuids-as-primary-keys/)
* [Vimberg (2018): Using UUID on Spring Data JPA Entities   ](https://jivimberg.io/blog/2018/11/05/using-uuid-on-spring-data-jpa-entities/)
* [An argument in favour of using even Value Objects](https://buildplease.com/pages/vo-ids/)

## Viable Options

1. DB-generated IDs for PKs and for API exposure
1. UUID for PKs and for API exposure
1. "Double" approach: DB-generated IDs for PKs, UUID for API exposure


## Alternatives not seriously considered

none


## How is this decision evaluated?

Architectural considerations, experience from earlier projects. 

 
## Resolution Details

We will use UUID for PKs and for API exposure (option 2).

## Reasons for the resolution

The problem with DB-generated IDs (option 1) is that you expose a "technical" ID to the outside world. Technical
means: It has been generated outside your active control, and it might be subject to change if you decide to 
migrate to another form of persistence. By exposing it via API, you make it quasi-permanent, since clients 
can hang on to the URLs. (See also the sources listed above.)

Usage of UUIDs (option 2) is a viable and pragmatic way out of this dilemma. Harrison (2017, see above) makes the 
point that one needs to be aware of possible performance concerns, and proposes a "double" approach (option 3): an 
"internal" generated ID, which is performance-efficient for SQL databases, and a UUID for external exposure. 

However, experience from earlier projects (see [Projektbörse Prox](prox.innovation-hub.de)) and considerations 
about the expected load make this argument seem nectlectable. Therefore, the pure UUID solution seems appropriate.

