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

* [Liquibase](https://www.liquibase.org/)
*   [Flyway](https://flywaydb.org/)


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

Developing with feature branches:
To avoid problems with a database versioning with multiple branches, the versioning number is time-stamped.

Example for our project:
V_<span style="color:#ffb42b">3</span>_<span style="color:#2b76ff">13</span> _<span style="color:#6cbd1f">145</span> _<span style="color:#b42bff">2020_07_08_11_10</span> __<span style="color:#2bffcf">fix_column_lengths</span>.sql

- <span style="color:#ffb42b">The first digits (3) means the major release.</span> 
- <span style="color:#2b76ff">The second digits (13) means minor changes.</span> 
- <span style="color:#6cbd1f">The third digits (145) means the patches or mere bug fixes.</span> 
- <span style="color:#b42bff">The further digits are part of the timestamp. Format: Year_Month_Day_Hour_Minute.</span> 
- <span style="color:#2bffcf">At the end of the description a comment of the version is needed.</span>

You can read here the meaning of the [version naming](https://flywaydb.org/documentation/concepts/migrations.html#naming). 



"This will prevent version number conflicts from happening (I’m assuming including hours and minutes suffices for this) but creates another problem: versions will not be guaranteed to be merged back to master in order.

That means that Flyway could run against a database to apply a migration like above, but then in a later release finds that there’s now a new migration 2017.7.6.12.12 that hasn’t been applied yet but has a version that’s lower than the latest migration that has been applied already.

By default Flyway will consider this an error and your migration will fail. However, you can simply tell Flyway that this is all expected and that it should simply execute all migrations that haven’t been applied yet by setting its **outOfOrder** property to true."

Source [Come Fly With Me: Flyway usage patterns part I](https://blog.trifork.com/2018/08/17/come-fly-with-me-flyway-usage-patterns-part-i/)

## Reasons for the resolution
We chose Flyway as version control tool for our database.


