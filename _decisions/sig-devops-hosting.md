---
type: decision
acronym: sig-devops-hosting
title: >
    Choice of Hosting provider
decision_type: must
belongs_to: devops
status: _3_sig_agreed
responsible: TZA
deadline: 2021-01-22
todos:
    - to add further resolution details
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v2:
        date: 2021-01-13
        comment: changed the deadline; added one aspect
    v3:
        date: 2021-01-14
        comment: added server prices
    v4:
        date: 2021-01-15
        comment: added responsible person, but it can be only temporary; added "Why-reasons", viable options and evaluation points
    v5:
        date: 2021-01-22
        comment: TODO
---

## Why is there need for such a decision?

The application will provide functionality that should be publicly accessible.
It has to be run by some kind of machine.
These are supposed to be provided somehow.
There are many ways in which this can be done.

## Additional sources for better understanding the background
* [Hosting Spring Boot Standalone and Clustered Java Applications with Jelastic Cloud](https://jelastic.com/blog/hosting-spring-boot-java-applications/)
* [Tutorial: Build a Java Spring Boot web app with Azure App Service on Linux and Azure Cosmos DB](https://docs.microsoft.com/en-us/azure/app-service/tutorial-java-spring-cosmosdb)

(Please list some sources where a reader can get a better understanding of the topic at hand)


## Viable Options

* To rent a server
    * Linux V-Server by [Strato](https://www.strato.de/server/linux-vserver/)
    

* To use some cloud platforms, and the services they offer 
    * [Azure App Service](https://docs.microsoft.com/en-us/azure/app-service/overview-hosting-plans)

    
* To use server provided by [UID](https://www.uid.com) (one of the main Stakeholders)
    * Linux Server


## Alternatives not seriously considered

* To rent a sever provided by big players like Google, Amazon, Microsoft


## How is this decision evaluated?

* Price
* Simplicity of setup
* Vendor lock-in (proprietary solution)
    * A proprietary solution is a hardware or software product or combination of products and services that is tied to a specific vendor, to the exclusion of all other vendors.
* Backup options
 
## Resolution Details

It was decided to use the hosting option from one of the main stakeholders ([UID](https://www.uid.com)).
A Linux server will be provided. The development team should be able to connect and to control the server using SSH (to be verified).

## Reasons for the resolution

The price is one of the most important aspects of the decision.
In this regard, only one viable option has the strongest position.
One of the main stakeholders (UID) is ready to provide a server for free.

(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)

