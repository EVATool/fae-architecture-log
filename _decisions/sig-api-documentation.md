---
type: decision
acronym: sig-api-Documentation 
title: >
    API-Documentation
decision_type: must
belongs_to: apis
status: _2_draft
todos:
responsible: FOB
deadline: 2021-02-05
history:
    v1:
        date: 2021-01-13
        comment: created initially
---

## Why is there need for such a decision?
The API-documentation describes the entire
API. The goal is to automatically document all API endpoints. This is achieved by using an API-Documentation tool, which will help to generate an easy API documentation source.
In this way it will be easier to understand the API endpoints. This decision depends on the API style!

All teams must use the same tool to prevent differential API-documentations syntax.

## Additional sources for better understanding the background

* [Open API](https://entwickler.de/online/development/einstieg-in-openapi-v3-579830417.html)
* [Code first vs. API first](https://apisyouwonthate.com/blog/api-design-first-vs-code-first)
* [Swagger UI](https://swagger.io/tools/swagger-ui/)
* [RAML](https://raml.org/)
* [GraphQL](https://nordicapis.com/graphql-documentation-generators-explorers-and-tools/)
* [Spring Rest Docu](https://spring.io/projects/spring-restdocs)

## Viable Options

* Swagger UI
* RAML with Spring Rest Docs
* GraphQL

## Alternatives not seriously considered

* Postman, not Open Source
* API Blueprint not for Java available 

## How is this decision evaluated?

The evaluation is a result of implemented respective tools!

when Rest is select as "sig-api-style" decision, then we will use Swaager or RAML with Spring Rest Docs. If GraphQL is chosen, so we will use the GraphQL Documentation Generator!
 
## Resolution Details

(If the resolation cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)


## Reasons for the resolution

(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)

