---
type: decision
acronym: sig-devops-maven-vs-gradle
title: >
    Maven is used as build tool 
decision_type: must
belongs_to: devops
status: _5_presented
responsible: MHA
deadline: 2021-01-15
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v2:
        date: 2021-01-13
        comment: updated need for decision and sources
    v3:
        date: 2021-01-14
        comment: made decision, added resolution details
    v4:
        date: 2021-01-15
        comment: updated Viable Options and Alternatives
---

## Why is there need for such a decision?

Build tools are used to help in build automation (further documentation details on the specific [wiki](https://github.com/EVATool/evatool-backend/wiki/Build-Tools) 
page). This decision will focus on maven and gradle only.

Based on the given monolithical approach with one single repository as an project, all teams must use the same 
build tool to avoid inconsistency.

## Additional sources for better understanding the background

- [(Ant) vs. Maven vs. Gradle](https://www.baeldung.com/ant-maven-gradle)
- [Maven vs. Gradle](https://gradle.org/maven-vs-gradle/)
- [Maven vs. Gradle performance](https://gradle.org/gradle-vs-maven-performance/)
- [Spreadshirt-Developer who switched back to Maven](https://phauer.com/2018/moving-back-from-gradle-to-maven/)
- [Maven core guide](https://www.baeldung.com/maven)
- [Comparing Maven and Gradle buid-file-size](https://miro.medium.com/max/2676/1*JFMnZ7hLx94LlZ6p-29PbA.png)


## Viable Options

- Maven: XML for build file, standardized project and build file organisation for better understanding the structure of the maven project.
- Gradle: Better performance than maven, simple building, more configurable.

## Alternatives not seriously considered

- Ant: Too much flexibility, requires developers to write all commands by themselves, which leads to huge XML files. Ant is hard to maintain, new build files takes some time to understand and there is no built-in support for dependency management.

## How is this decision evaluated?

First, a general research (theoretical advantages and disadvantages as well as practical examples) for both tools will be initiated. After this process I will compare my personal formed opinion with the opinion of other project participants. 
It has to be mentioned that the overall opinion of the other project participants is weighted higher than mine. Based on this opinions, a final decision will be made.

## Resolution Details

After a more extensive research, I came to the conclusion that maven as a build tool is the optimal choice for this kind of project. This opinion was validated by some project participants and external developer (research) with the same opinion after a short survey.

## Reasons for the resolution

Based on personal opinions and experiences of asked project participants, there is no reason to choose gradle as a build tool.

