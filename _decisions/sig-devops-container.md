---
type: decision
acronym: sig-devops-container
title: >
    Containerization - application hosting  
decision_type: must
belongs_to: devops
status: _2_draft
responsible: TZA
deadline: 2021-01-29
todos:
    - Create Virtual Machine (VM with Linux) on a local machine (using VirtualBox)
    - Hello World-Spring-Boot application with one very simple REST API
    - Find a way to deliver the application on VM
history:
    v1:
        date: 2021-01-12
        comment: created initially
    v2:
        date: 2021-01-13
        comment: changed the deadline; added questions
    v3:
        date: 2021-01-15
        comment: added "viable options" and decision evaluation steps
    v4: 
        date: 2021-01-22
        comment: moved the questions part up to the "todos" section (makes it better visible)
    v5:
        date: 2021-01-26
        comment: updated todos and removed unnecessary information 

---

## Why is there need for such a decision?

The application needs to be hosted. There are several ways to do this.
The application can be run on a physical server.
It can be packaged in a container or run in a virtual machine.
All of these approaches have their own advantages and disadvantages.
These have to be weighed up.

## Additional sources for better understanding the background

* [Application containerization](https://searchitoperations.techtarget.com/definition/application-containerization-app-containerization)
* [Containers vs. virtual machines (microsoft)](https://docs.microsoft.com/en-us/virtualization/windowscontainers/about/containers-vs-vm)
* [Containers vs VMs (redhat)](https://www.redhat.com/en/topics/containers/containers-vs-vms)
* [Deploy Your Spring Boot App the Right Way](https://developer.okta.com/blog/2019/12/03/spring-boot-deploy-options) 
* [Deploying Spring Boot Applications (1)](https://spring.io/blog/2014/03/07/deploying-spring-boot-applications)
* [Deploying Spring Boot Applications (2 - docs)](https://docs.spring.io/spring-boot/docs/current/reference/html/deployment.html)

## Viable Options

* A virtual machine (with "VirtualBox")
* container (with "docker")

## Alternatives not seriously considered

TODO

(Here comes a list of alternatives that you can exclude right away, without an in-depth evaluation. Format: 
Simple bulleted list with a brief 1-sentence explanation is sufficient.)


## How is this decision evaluated?

First we have to implement two PoCs. One using VM and another one using docker.

Then compare this two options on such aspects as:
* Workflow (what is easier)
* Application delivery: build -> test -> deploy -> run
* Updates delivery (Scenario: Hotfix)
* local debugging

## Resolution Details

TODO

(If the resolution cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)


## Reasons for the resolution

TODO

(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)

