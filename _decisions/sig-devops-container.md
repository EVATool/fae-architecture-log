---
type: decision
acronym: sig-devops-container
title: >
    Containerization - VM vs. Docker  
decision_type: must
belongs_to: devops
status: _5_presented
responsible: TZA
deadline: 2021-02-05
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
    v6:
        date: 2021-02-05
        comment: added resolution details and reasons for resolution
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
* [Topical Guide on Docker / Spring Boot Docker](https://spring.io/guides/topicals/spring-boot-docker)
* [Getting Started / Spring Boot with Docker](https://spring.io/guides/gs/spring-boot-docker/)

## Viable Options

* A virtual machine (with "VirtualBox")
* container (with "docker")

## Alternatives not seriously considered

None

## How is this decision evaluated?

First we have to implement two PoCs. One using VM and another one using docker.

Then compare this two options on such aspects as:
* Installation 
* Configuration
* Lightweight
* Input from main Stakeholder (UID)
* Proprietary solution  
* Workflow (what is easier)
* Application delivery: build -> test -> deploy -> run
* Updates delivery (Scenario: Hotfix)
* local debugging

## Resolution Details

It was decided that the docker technology is better suited to the project.

Most of the explanations for the individual resolution details can be found in the [wiki](https://github.com/EVATool/evatool-backend/wiki/VM-vs-Docker-PoC).

**Installation**\
The installation of the solutions on the basis of both VM and Docker are at a similar level of complexity.

**Configuration**
* The flexibility of the solution with VM is very high, but this creates a large overhead\
  The level of complexity for the configuration of VM is very high and hard to master
* Using docker is the configuration a lot easier and better to understand\
  The necessary information is easier to find and there is more of it in contrast to VM\
  

**Lightweight**
* The VM brings a lot of overhead with it because it practically simulates a real machine
* The Docker containers can be made as small as you can imagine

**Input from main Stakeholder (UID)**
* The server used in the project will be a Microsoft Windows machine
  (update: Linux Server)

**Proprietary solution**
* Both VM and Docker solutions are more or less platform independent (but the VM has more overhead)

**Workflow**\
The workflow is simpler when using Docker because it is easier to understand  

**Application delivery**\
Deployment is very similar in complexity

**Updates delivery**\
Not considered

**Debugging**\
See decision [Debugging](https://github.com/EVATool/evatool-backend/wiki/Debugging)

## Reasons for the resolution

* Better understanding
* Lightweight
* Flexibility
