---
type: decision
acronym: sig-api-database
title: >
    MYSQL used as database
decision_type: must
belongs_to: apis
status: _5_presented
responsible: MTO;FOB
deadline: 2021-02-19
implemented: false
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v2:
        date: 2021-01-28
        comment: need for decision
    v3:
        date: 2021-02-12
        comment: edit Resolution Details, todos


---

## Why is there need for such a decision?

There are many database systems for different purposes. It is therefore important to find a database system that is useful for our project.
A database is needed to centrally manage the data. This database allows us to store data persistently.


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

After implementing the concept, the following findings emerged: 

Both database systems behaved the same. There were no noticeable differences. In our opinion, this is more a matter of taste. In the end we decided to use the MySQL databases. Due to our experience with this database, this decision was easy for us. 

[Database table prefix convention.](https://github.com/EVATool/evatool-backend/wiki/Database-table-prefix-convention)

[Setup spring database connection.](https://github.com/EVATool/evatool-backend/wiki/Setup-spring-database-connection)

[Database version controlling with Flyway.](https://github.com/EVATool/evatool-backend/wiki/Database-version-controlling-with-Flyway)

## Reasons for the resolution
Based on personal experiences and testing both systems. The better choice is Mysql.


