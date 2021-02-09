---
type: decision
acronym: sig-devops-delivery
title: >
    Application delivery - Tool Chain for Build Pipeline
decision_type: must
belongs_to: devops
status: _2_draft
todos: 
responsible: TZA, HBU
deadline: 2021-02-15
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v2: 
        date: 2021-01-15
        comment: added responsible person, but it can be only temporary; First explanation of "Why is there need for such a decision?"
    v3: 
        date: 2021-01-15
        comment: viable options added; deadline updated; changed title
    v4:
        date: 2021-02-09
        comment: added TODOs and cleaned up.
---

## Why is there need for such a decision?

The application needs to be delivered to a server in order to be availble.
This delivery process will be automated and will continuously deploy the newest version of the project to the server.
UID is providing a remote server.

The decision `devops-testing-automation` was a short-term solution to enable testing automation earlier in the project.

### Questions and others

TODO:
    Delivery: build -> test -> deploy -> run TODO: compile -> test -> build -> deploy -> run?

TODO:
* How to build? (see sig-devops-buildtools)
* How to test? (see sig-devops-testing-automation)
* How to deploy?
* How to run?

## Additional sources for better understanding the background

TODO:
(Please list some sources where a reader can get a better understanding of the topic at hand)

## Viable Options

- Execute the whole pipeline on the server
- Execute all steps that can run on GitHub (with GitHub Actions) on GitHub and deploy to the server and run the application

## Alternatives not seriously considered

- Execute some portion on GitHub and the rest on the server

## How is this decision evaluated?

- The solution should fit well into existing solutions
- It must be free (except the remote server)
- It should be resistant to changes happening in the project

TODO:
(**Before** you start working in this, please write down how you will evaluate this decision, and plan to 
come to a resolution. 
It is  **not sufficient** to perform a brief Google search, and then write  the "result" down. Any decision must
**always** be based on a thorough evaluation - if possible hands-on, i.e. by coding a brief proof-of-concept.
if this doesn't apply, then some other means of proper research must be given here - e.g. an evaluation of 
the most relevant literature or IT community sources.)

## Resolution Details

TODO: Wiki link...

TODO:
(If the resolation cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)

## Reasons for the resolution

TODO:
(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)
