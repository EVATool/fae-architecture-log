---
type: decision
acronym: sig-devops-buildtools
title: >
    Build-tools (maven vs. gradle)  
decision_type: must
status: _1_open
responsible: MHA
deadline: 2021-01-22
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v2:
        date: 2021-01-13
        comment: updated need for decision and sources
---

## Why is there need for such a decision?

Build tools like ant, maven and gradle are used to help in build automation. Build automation will help to automate a variety of tasks like compiling source code, converting into binary code, managing dependencies, running automated tests and deployment to production systems. This decision will focus on maven and gradle only.

All teams must use the same build tool to avoid inconsistency.

## Additional sources for better understanding the background

- [(Ant) vs. Maven vs. Gradle](https://www.baeldung.com/ant-maven-gradle)
- [Maven vs. Gradle](https://gradle.org/maven-vs-gradle/)
- [Maven vs. Gradle performance](https://gradle.org/gradle-vs-maven-performance/)
- [Spreadshirt-Developer who switched back to Maven](https://phauer.com/2018/moving-back-from-gradle-to-maven/)
- [Maven core guide](https://www.baeldung.com/maven)
- [Comparing Maven and Gradle buid-file-size](https://miro.medium.com/max/2676/1*JFMnZ7hLx94LlZ6p-29PbA.png)

## How is this decision evaluated?

(**Before** you start working in this, please write down how you will evaluate this decision, and plan to 
come to a resolution. 
It is  **not sufficient** to perform a brief Google search, and then write  the "result" down. Any decision must
**always** be based on a thorough evaluation - if possible hands-on, i.e. by coding a brief proof-of-concept.
if this doesn't apply, then some other means of proper research must be given here - e.g. an evaluation of 
the most relevant literature or IT community sources.) 

## Resolution Details

(If the resolation cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)


## Reasons for the resolution

(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)

