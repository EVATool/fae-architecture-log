---
type: decision
acronym: sig-api-Documentation 
title: >
    API-Documentation
decision_type: must
belongs_to: apis
status: _1_open
responsible: FOB
deadline: 2021-01-29
history:
    v1:
        date: 2021-01-15
        comment: created initially
---

## Why is there need for such a decision?
The API-Documentation describes the entire
API. The goal should be that all API Endpoints be automatically documented. Moreover, by using the same API-Documentation Tool. That will be easier to generate the API Docu.
In addition to that, it will be easier to understand API Endpoints.

All Teams must use the same API-Documentation Tool to reach this goal.

## Additional sources for better understanding the background

[Open API](https://entwickler.de/online/development/einstieg-in-openapi-v3-579830417.html)

[Swagger UI](https://swagger.io/tools/swagger-ui/)

[RAML](https://raml.org/)

[GraphQL](https://nordicapis.com/graphql-documentation-generators-explorers-and-tools/)

[Spring Rest Docu](https://spring.io/projects/spring-restdocs)

## Viable Options
Swagger UI

RAML with Spring Rest Docs

GraphQL

## Alternatives not seriously considered

Postman, not Open Source

API Blueprint not for Java available 

## How is this decision evaluated?

Einfach Implementieren!

 
## Resolution Details

(If the resolation cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)


## Reasons for the resolution

(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)

