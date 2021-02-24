---
type: decision
acronym: sig-api-Documentation 
title: API-Documentation is done using Swagger
decision_type: must
belongs_to: apis
status: _5_presented
todos:
responsible: FOB
deadline: 2021-02-12
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v2:
        date: 2021-01-13
        comment: update responsibility
    v3:
        date: 2021-01-13
        comment: need for decision
    v4:
        date: 2021-01-13
        comment: sources and evaluation
    v5: 
        date: 2021-01-23
        comment: updated deadline    
    v6:
        date: 2021-02-01
        comment: add Resolution
    v7:    
        date: 2021-02-12
        comment: back to 4, to be presented again with how-to
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
* [Spring Rest Docu](https://spring.io/projects/spring-restdocs)

## Viable Options

* Swagger UI
* Spring Rest Docs
* GraphQL

## Alternatives not seriously considered

* Postman, not Open Source
* API Blueprint not for Java available 

## How is this decision evaluated?

The evaluation is a result of implemented respective tools!

when Rest is select as "sig-api-style" decision, then we will use Swaager or Spring Rest Docs. If GraphQL is chosen, so we will use the GraphQL Documentation Generator!
 
## Resolution Details

Our team is using the tool Swagger. Swagger offers an library for our Spring-Boot Application. The tool automatically documentates API-endpoints. Therefore the documentation maintenance is heavly reduced. No further knowledge is needed, since the handling of tool is basic and easy.  

## Reasons for the resolution
* Automatically documentated API-endpoints
* Executable methods
* No further programming skill is needed
* Assistant tool with high usability 

[wiki](https://github.com/EVATool/evatool-backend/wiki/Swagger-Docu)

Mainly we choosed this resoution due to its large offers of transparent informations in contrast to Spring Rest Docs and its JSON-format.

For our code documentation, each team will need to use at least the following annotations:
@Api(description = "txt") and @ApiOperation (value = "txt")

@Api should describe the respective rest-controller class with one sentence.

@ApiOperation should describe the respective method in the rest-controller class with a record. 

More informations: [Swagger Docs](https://docs.swagger.io/swagger-core/current/apidocs/)

