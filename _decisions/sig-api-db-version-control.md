---
type: decision
acronym: sig-api-database-version-control
title: >
    Database Version Control
decision_type: must
belongs_to: apis
status: _2_draft
responsible: MTO;FOB
deadline: 2021-02-12
history:
    v1:
        date: 2021-02-06
        comment: created initially

---

## Why is there need for such a decision?
We need a tool that helps us to migrate. Migrations from database systems or individual tables.
We need a version controll for our database.
## Additional sources for better understanding the background

[Liquibase](https://www.liquibase.org/)

[Flyway](https://flywaydb.org/)


## Viable Options

* liquibase
* Flyway


## Alternatives not seriously considered
* IRI NextForm
* DBConvert Studio
* Xplenty

## How is this decision evaluated?
* Tables migration
* Database migration
 
 
## Resolution Details
In the context of our project, we chose Flyway. 
Flyway and Liquibase offer the same functionalities. Whereby Liquibase is a real powerhouse. Flyway is a ligth version and easier to use. Migrations are written with SQL. Liquibase, on the other hand, offers several ways to migrate a database, for example SQL, XML, YAML and more. However, SQL is completely sufficient 

## Reasons for the resolution
We will chose Flyway as version controll tool for our database.


