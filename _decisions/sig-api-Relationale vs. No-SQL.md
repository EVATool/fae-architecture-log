---
type: decision
acronym: sig-api-database-relational
title: >
    Relational database vs. NO-SQL DB
decision_type: must
belongs_to: apis
status: _5_presented
responsible: MTO;FOB
deadline: 2021-02-12
history:
    v1:
        date: 2021-02-06
        comment: created initially
    v2:
        date: 2021-02-06
        comment: add Resolution
    v3:
        date: 2021-02-12
        comment: Reasons for the resolution
   
---

## Why is there need for such a decision?
The decision about a database depends on the approach. Here two approaches are compared. To achieve this goal, everyone must use the same approach.

## Additional sources for better understanding the background

[NO-SQL DB](https://www.bigdata-insider.de/was-ist-nosql-a-615718/)

[Relational DB](https://www.bigdata-insider.de/was-ist-eine-relationale-datenbank-a-643028/)

[Databases](https://www.geeksforgeeks.org/top-10-open-source-nosql-databases-in-2020/)

## Viable Options
* MYSQL
* POSTGRESQL
* MongoDB

## Alternatives not seriously considered
Oracle NO-SQL

Commercial database-systems are unsuitable for open source projects.

## How is this decision evaluated?

This decision based on the experience and knowledge of the students.

## Resolution Details

Many projects use a Relational DB! We are already use it temporary in the integrated memory database (h2).

## Reasons for the resolution

The project team is familiar with relational databases. It would be an extra effort to learn a new technology (No-SQL). In addition, the integration from the H2 memory database to another e.g. MySql is much easier, because MySql is also a relational database.
