---
type: decision
acronym: modelling-styleguide
title: >
    Some basic styleguide for domain modelling
decision_type: should
belongs_to: devops
status: _5_presented
responsible: SBE
deadline: 2021-01-29
history:
    v1:
        date: 2021-01-29
        comment: created initially
---

## Why is there need for such a decision?

Domain models need to be maintained and kept up-to-date by teams, as they are an essential part of the documentation. 

## Additional sources for better understanding the background

Various - too many to name here.

## Viable Options

No-brainer, not really a choice between options.  

## Alternatives not seriously considered

None.

## How is this decision evaluated?

Summing up experience and various sources.
 
## Resolution Details

Some basic rules should be followed: 
1. Assocications should be unidirectional. 
    * Bidirectional relationships lead to tight coupling between entities 
        (see [Bente, 2021: Warum unidirektionale Beziehungen im Logischen Datenmodell? Video für ST1](https://www.youtube.com/watch?v=RufBXPTt1SA))
    * The domain model should tell on which side of the relationship the JPA implementation code will be located.
1. Variables used for implementing a relationship don't count as attributes and should not appear in the attribute list.
    * The attributes should be business-related ("fachlich")
    * reference attributes are clear from the associations
1. It is useful to have multiplicities annotated at the associations.    
      

## Reasons for the resolution

Experience and general good practice.
