---
type: decision
acronym: package-structure-according-to-ddd
title: >
    The package structure should reflect the DDD layer architecture  
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

It is useful that all teams (sub-domains) use a similar package structure. This makes further development by 
other teams easier, as there is a uniform package structure throughout the whole code base. 

## Additional sources for better understanding the background

* [Schichtenarchitektur nach DDD (Domain & Application Layer), Inhaltsimpuls Bente](https://ilias.th-koeln.de/goto.php?target=file_1800070_download&client_id=ILIAS_FH_Koeln)
* Evans, E. (2003) ("blue book"). Domain-Driven Design: Tackling Complexity in the Heart of Software 
    (1 edition). Addison-Wesley Professional.


## Viable Options

The package structure should reflect the DDD layers as described in the sources above. 


## Alternatives not seriously considered

None.


## How is this decision evaluated?

Just common sense. 

 
## Resolution Details

The packages for each sub-domain should reflect two main layers: 
1. Application Layer
    * "This layer is kept thin. It does not contain business rules or knowledge, but only coordinates tasks and 
        delegates work to collaborations of domain objects in the next layer down." (Evans)
    * Concepts located here: 
        * Controller (REST, GraphQL, …)
        * Application Service (encapsulates workflows like creation and query of entities, transformation from DTO 
            from/to entities)
        * DTO (Data Transfer Object)
2. Domain Layer
    * "Responsible for representing concepts of the business, information about the business situation, and business 
        rules. State that reflects the business situation is controlled and used here, even though the technical 
        details of storing it are delegated to the infrastructure." (Evans)
    * Concepts located here:          
        * Entity
        * Repository
        * Aggregate
        * Value Object


## Reasons for the resolution

Compliance with design approach.

