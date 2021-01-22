---
type: decision
acronym: devops-api-testing
title: >
    API Testing
decision_type: must
status: _1_open
responsible: HBU
deadline: 2021-01-29
todos: 
    - status is not "open" anymore, as there is already some content
    - please make the options more concrete in terms of technologies / tools used
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v2:
        date: 2021-01-15
        comment: filled out until evaluation
---

## Why is there need for such a decision?

API calls must be tested like any other runnable code in a project.

## Additional sources for better understanding the background

(Please list some sources where a reader can get a better understanding of the topic at hand)

## Viable Options

- Mocking: Mocking the API calls.
- Hosting: Hosting a dummy server and testing API calls on that server.

## Alternatives not seriously considered

- Program test: Testing the API by running the program.

## How has this decision been evaluated?

The options will be scrutinized in regard to:
- Amount of resources/documentation
- Easy of usage
- Cost (must be free)
- How well they fit into existing parameters (automation, easier integration, less overhead)

 
## Resolution Details



(If the resolation cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)

## Reasons for the resolution



(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)
