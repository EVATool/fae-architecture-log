---
type: decision
acronym: sig-api-database-configuration-dev-prod
title: > 
    Configuration database state dev and prod
decision_type: must
belongs_to: apis
status: _5_presented
responsible: MTO;FOB
deadline: 2021-03-02
todos: 
    - options Docker vs. dual database (MySql + H2)
    - it would be strong benefit if someone could clone the repo and get started right away (with H2)
    - trial implementation needed
history:
    v1:
        date: 2021-02-12
        comment: created initially

---

## Why is there need for such a decision?
Due to our different branches (Dev and Prod) two different databases might be needed! Due to the different databases, different configurations are needed.

## Additional sources for better understanding the background
[MySQL](https://www.mysql.com/de/)

[H2](https://www.h2database.com/html/main.html)

[DB config](https://evatool.github.io/fae-architecture-log/decisions/sig-api-database.html)

[Dual DB config](https://riptutorial.com/spring-boot/example/21856/dev-and-prod-environment-using-different-datasources)

## Viable Options
Dual DB (MYSQL and H2)

Docker image 
## Alternatives not seriously considered


## How is this decision evaluated?
This decision depends on the database.

## Resolution Details
We will use dual databases. The effort to containerize the databases with Docker would calculate the time frame for this decision. Since familiarization with Docker is necessary. 

## Reasons for the resolution
We will use teo different application.prop. [WIKI](https://github.com/EVATool/evatool-backend/wiki/Database-Configuration)


