---
type: decision
acronym: sig-devops-database
title: >
    Choice of database
decision_type: should
belongs_to: devops
status: _2_draft
responsible: MTO;FOB
deadline: 2021-02-12
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v1:
        date: 2021-01-28
        comment: need for decision
---

## Why is there need for such a decision?

There are many different database systems for different purposes. It is therefore important to find a database system that is useful for our project.

## Additional sources for better understanding the background

[Comparing Database Management Systems: MySQL, PostgreSQL, MSSQL Server, MongoDB, Elasticsearch and others](https://www.altexsoft.com/blog/business/comparing-database-management-systems-mysql-postgresql-mssql-server-mongodb-elasticsearch-and-others/).
Here you can find the different open source database-systems and their basic structure e.g. relational and non-relational database-systems.

## Viable Options

* MYSQL 
* PostgreSQL


## Alternatives not seriously considered

* IBM DB2
* Oracle DATABASE
* S4 Hana SAP
  
Commercial database-systems are unsuitable for open source projects.

## How is this decision evaluated?
* Creation of a database and a schema
* Tables migration
* Connect the database to a Spring-Boot project
 
## Resolution Details

(If the resolation cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)


## Reasons for the resolution

(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)

