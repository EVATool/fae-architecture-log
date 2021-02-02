---
type: decision
acronym: devops-api-testing
title: >
    API Testing
decision_type: must
belongs_to: devops
status: _2_draft
responsible: HBU
deadline: 2021-02-05
todos: 
    - Ask: Decision - conventions for returned http status and error handling?
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v2:
        date: 2021-01-15
        comment: filled out until evaluation
    v3:
        date: 2021-02-02
        comment: finalized decision
---

## Why is there need for such a decision?

API calls must be tested like any other runnable code in a project.

## Additional sources for better understanding the background

- [Wikipedia - Rest](https://en.wikipedia.org/wiki/Representational_state_transfer)
- [Spring Testing - Testing Web](https://spring.io/guides/gs/testing-web/)
- [Spring Boot Testing](https://www.baeldung.com/spring-boot-testing)
- [RESTful API Tutorial](https://restfulapi.net/)

## Viable Options

- Using unit (mocking) and integration tests

## Alternatives not seriously considered

- None

## How has this decision been evaluated?

The options will be scrutinized in regard to:
- Amount of resources/documentation
- Easy of usage
- Cost (must be free)
- How well they fit into existing parameters (automation, easier integration, less overhead)

## Resolution Details

[Wiki article](https://github.com/EVATool/evatool-backend/wiki/DevOps-API-Testing)

## Reasons for the resolution

The given option was the only valid one.

(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)
