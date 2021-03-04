---
type: decision
acronym: devops-event-testing
title: >
    Event Testing
decision_type: must
belongs_to: devops
status: _5_presented
todos: 
responsible: HBU
deadline: 2021-01-29
implemented: partially
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v2:
        date: 2021-01-15
        comment: filled out until evaluation
    v3:
        date: 2021-01-26
        comment: finished temporary draft
    v4:
        date: 2021-01-27
        comment: Completed decision and added link to finished wiki
---

## Why is there need for such a decision?

Events must be tested like any other runnable code in a project.

## Additional sources for better understanding the background

- [Spring Events Documentation](https://docs.spring.io/spring-integration/docs/current/reference/html/event.html)
- [Spring Events Implementation](https://www.baeldung.com/spring-events)
- [Spring Testing - Application Events](https://docs.spring.io/spring-framework/docs/current/reference/html/testing.html#testcontext-application-events)

## Viable Options

- Spring event Testing

## Alternatives not seriously considered

- None

## How has this decision been evaluated?

The candidates will be evaluated by:
- How easy testing is for the developer
- How practical the implementation is
- How they fit into existing testing schemas
- The price of the solution

## Resolution Details

[Wiki article](https://github.com/EVATool/evatool-backend/wiki/DevOps-Event-Testing)

Mocking the firing and processing of events allows the code to be easily tested locally. It puts the test in a format (unit tests) where
they can be run in the existing framework using GitHub Actions on GitHub. It does not change the existing procedure of testing the code.
It is also free of charge when using the free version of GitHub Actions (see testing automation).

The testing on a live server would require a running dedicated and managed server. Production wants to implement such a server soon, but every 
developer might want to test their code locally so immediately see what is wrong with the code. Deploying a test build on the server does not 
fit into the existing testing solution of using GitHub Actions. The server costs money to run and maintain.

## Reasons for the resolution

Using GitHub Actions is suitable for this project. It will also be more elegant to integrate this solution into the final build pipeline, 
because the testing step is clearly defined and done.


