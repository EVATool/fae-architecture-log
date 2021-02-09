---
type: decision
acronym: sig-devops-delivery
title: >
    Application delivery - Tool Chain for Build Pipeline
decision_type: must
belongs_to: devops
status: _2_draft
todos:
    - implement and test PoC with GitHub-Actions
    - research Jenkins-Server solution
    - get access to server from UID (with SSH)
    - try to use personal machines as a public available server 
    - create wiki
responsible: TZA;HBU
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
    v5:
        date: 2021-02-09
        comment: added new TODOs and some new information
---

## Why is there need for such a decision?

The application needs to be delivered to a server in order to be available.
This delivery process will be automated and will continuously deploy the newest version of the project to the server.
Each new version of application will be created as a docker image.
Then it should be transferred to server and run as a docker container. 
UID is providing a remote server.

The decision `devops-testing-automation` was a short-term solution to enable testing automation earlier in the project.

### Questions and others (temporary)

* How to build? (see sig-devops-buildtools)
* How to test? (see sig-devops-testing-automation)
* How to deploy? (see sig-devops-container)
* How to run? (see sig-devops-container)

## Additional sources for better understanding the background

* [CI/CD](https://en.wikipedia.org/wiki/CI/CD)
* [Continuous integration](https://en.wikipedia.org/wiki/Continuous_integration)
* [Continuous delivery](https://en.wikipedia.org/wiki/Continuous_delivery)
* [GitHub Actions](https://github.com/features/actions)
* [Jenkins (software)](https://en.wikipedia.org/wiki/Jenkins_(software))

## Viable Options

- realize build pipeline using GitHub Actions
- realize build pipeline using Jenkins

## Alternatives not seriously considered

- Execute some portion on GitHub and the rest on the server

## How is this decision evaluated?

- The solution should fit well into existing solutions
- It must be free (except the remote server)
- It should be resistant to changes happening in the project

TODO: add more criteria

## Resolution Details

TODO: Wiki link...

TODO:
(If the resolation cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)

## Reasons for the resolution

TODO:
(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)
