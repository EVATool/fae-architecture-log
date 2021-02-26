---
type: decision
acronym: team-impact-domain-model
title: >
    Domain model for team "Impact"  
decision_type: team
belongs_to: impact
status: _3_team_agreed
responsible: HBU;TZA 
deadline: 2021-01-29
history:
    v1:
        date: 2021-01-08
        comment: created initially
    v2:
        date: 2021-01-27
        comment: moved a documentation to wiki
    v3:
        date: 2021-01-28
        comment: removed reasons for the resolution
    v4:
        date: 2021-02-09
        comment: updated the status
---

## Why is there need for such a decision?

Before implementation start, some basic research on the domain should be done.
We should identify main objects of the domain.
In addition, the relationships between these objects are also very important.

## Additional sources for better understanding the background

[Evans, E. (2015). Domain-Driven Design Reference—Definitions and Pattern Summaries. Domain Language, Inc. [Ev15]](http://domainlanguage.com/wp-content/uploads/2016/05/DDD_Reference_2015-03.pdf)

**Domain model** a system of abstractions that describes selected aspects of a domain and can be used to solve problems related to that domain. [Ev15]

Draw from the model the terminology used in the design and the basic assignment of responsibilities.
The code becomes an expression of the model, so a change to the code may be a change to the model.
Its effect must ripple through the rest of the project’s activities accordingly. [Ev15]

### Links
* [Domain model](https://en.wikipedia.org/wiki/Domain_model)
* [What is a Domain Model](https://stackoverflow.com/questions/1863537/what-is-a-domain-model)
* [A Brief Introduction to Domain Modeling](https://olegchursin.medium.com/a-brief-introduction-to-domain-modeling-862a30b38353)
* [Softwaretechnik 1 (ST1)](https://www.archi-lab.io/display/public/ST1#ST1-ScriptzurVeranstaltung)

## Viable Options

* conceptual data model (germ.: Fachliches Datenmodell)
* logical data model (germ.: Logisches Datenmodell)

## Resolution Details

For this decision, the domain model was created in two steps:

* First, with the help of the existing
  [wireframes](https://lsw4em.axshare.com/#id=wvfe6y&p=website) and the
  [Excel file](https://github.com/Archi-Lab/elsi-by-design-excel/),
  the main objects of the domain and their relationships were identified.
  These were the basics for creating a
  [conceptual data model](https://en.wikipedia.org/wiki/Conceptual_schema).
  
* Then more details like attributes and association directions were added.
  In addition, it was determined which objects represent an entity.
  These were the basics for creating a
  [logical data model](https://en.wikipedia.org/wiki/Logical_schema)

### [Impact Wiki](https://github.com/EVATool/evatool-backend/wiki/Impact)

---
