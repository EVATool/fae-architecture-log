---
type: decision
acronym: sig-devops-container
title: >
    Containerization - application hosting  
decision_type: must
belongs_to: devops
status: _1_open
responsible: TZA
deadline: 2021-02-05
history:
    v1:
        date: 2021-01-12
        comment: created initially
    v2:
        date: 2021-01-13
        comment: changed the deadline; added questions
---

## Why is there need for such a decision?

The application needs to be hosted. There are several ways to do this.
The application can be run on a physical server.
It can be packaged in a container or run in a virtual machine.
All of these approaches have their own advantages and disadvantages.
These have to be weighed up.

(Please explain in 1-2 sentences why this is necessary to decide, and why it is a decision on the respective level
must / should / team)

## Additional sources for better understanding the background
[Application containerization](https://searchitoperations.techtarget.com/definition/application-containerization-app-containerization)

[Containers vs. virtual machines (microsoft)](https://docs.microsoft.com/en-us/virtualization/windowscontainers/about/containers-vs-vm)

[Containers vs VMs (redhat)](https://www.redhat.com/en/topics/containers/containers-vs-vms)

[Deploy Your Spring Boot App the Right Way](https://developer.okta.com/blog/2019/12/03/spring-boot-deploy-options) 

[Deploying Spring Boot Applications (1)](https://spring.io/blog/2014/03/07/deploying-spring-boot-applications)

[Deploying Spring Boot Applications (2 - docs)](https://docs.spring.io/spring-boot/docs/current/reference/html/deployment.html)

(Please list some sources where a reader can get a better understanding of the topic at hand)


## Viable Options

(Please list those options that you seriously consider as a possible solution. Simple bulleted list with a brief 
1-sentence explanation is sufficient.)


## Alternatives not seriously considered

(Here comes a list of alternatives that you can exclude right away, without an in-depth evaluation. Format: 
Simple bulleted list with a brief 1-sentence explanation is sufficient.)





## How is this decision evaluated?

(**Before** you start working in this, please write down how you will evaluate this decision, and plan to 
come to a resolution. 
It is  **not sufficient** to perform a brief Google search, and then write  the "result" down. Any decision must
**always** be based on a thorough evaluation - if possible hands-on, i.e. by coding a brief proof-of-concept.
if this doesn't apply, then some other means of proper research must be given here - e.g. an evaluation of 
the most relevant literature or IT community sources.) 



### Questions

* Why to use containers for EVATool?

* Compare docker vs. VM?
    * What tasks should I try on both of them?! Which aspects are important for decision?

          - Workflow (what is easier)
          - Application delivery: build -> test -> deploy -> run
          - Updates delivery (Scenario: Hotfix)

  first TODOs:
    * "Hello World"-Spring-Boot application with one very simple REST API
    * Create VM (some sort of Linux) on a local machine (using VirtualBox)
    * Find a way to deliver the application on VM

* Do hosting platforms offer support for containers?
* Do hosting-platforms provide some frameworks for containerization?
* Do hosting-platforms have complete container-solutions?


* EVATool: Would it be a Web-Site or App or what?
    * In FAE we will build a sand-alone Spring-Application (with Spring Boot)
    
    
 
## Resolution Details

(If the resolation cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)


## Reasons for the resolution

(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)

