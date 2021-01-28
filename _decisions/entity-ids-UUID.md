---
type: decision
acronym: entity-ids-uuid
title: >
    UUIDs are to be used for Entity IDs
decision_type: must
belongs_to: apis
status: _2_draft
todos:
    - write description, esp. with link to documentation
    - present to group
responsible: SBE
deadline: 2021-01-29
history:
    v1:
        date: 2021-01-22
        comment: created initially
---

## Why is there need for such a decision?

If we expose entities over APIs and events, a uniform way of dealing with IDs is very helpful.  

## Additional sources for better understanding the background

* [Harrison (2017): UUID or GUID as Primary Keys? Be Careful!](https://tomharrisonjr.com/uuid-or-guid-as-primary-keys-be-careful-7b2aa3dcb439)
* [Sikkema (2009): JPA implementation patterns: Using UUIDs as primary keys](https://xebia.com/blog/jpa-implementation-patterns-using-uuids-as-primary-keys/)
* [Vimberg (2018): Using UUID on Spring Data JPA Entities   ](https://jivimberg.io/blog/2018/11/05/using-uuid-on-spring-data-jpa-entities/)
* [An argument in favour of using even Value Objects](https://buildplease.com/pages/vo-ids/)




## Viable Options

(Please list those options that you seriously consider as a possible solution. Simple bulleted list with a brief 
1-sentence explanation is sufficient.)


## Alternatives not seriously considered

(Here comes a list of alternatives that you can exclude right away, without an in-depth evaluation. Format: 
Simple bulleted list with a brief 1-sentence explanation is sufficient.)



## How is this decision evaluated?

(**Before** you start working in this, please write down how you will evaluate this decision, and plan to 
come to a resolution. 
It is  **not sufficient** to perform a brief Google search, and then write  the "result" down. Any decision must
**always** be based on a thorough evaluation - if possible hands-on, i.e. by coding a brief proof-of-concept.
if this doesn't apply, then some other means of proper research must be given here - e.g. an evaluation of 
the most relevant literature or IT community sources.) 

 
## Resolution Details

(If the resolation cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)


## Reasons for the resolution

(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)

