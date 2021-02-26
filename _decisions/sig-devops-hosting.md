---
type: decision
acronym: sig-devops-hosting
title: >
    Choice of Hosting provider
decision_type: must
belongs_to: devops
status: _5_presented
responsible: TZA
deadline: 2021-01-22
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
        comment: added resolution, details and reasons
---

## Why is there need for such a decision?

The application will provide functionality that should be publicly accessible.
It has to be run by some kind of machine.
These are supposed to be provided somehow.
There are many ways in which this can be done.

## Additional sources for better understanding the background
* [Hosting Spring Boot Standalone and Clustered Java Applications with Jelastic Cloud](https://jelastic.com/blog/hosting-spring-boot-java-applications/)
* [Tutorial: Build a Java Spring Boot web app with Azure App Service on Linux and Azure Cosmos DB](https://docs.microsoft.com/en-us/azure/app-service/tutorial-java-spring-cosmosdb)

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
A Linux server will be provided. The development team should be able to connect and to control the server using SSH.

## Reasons for the resolution

The price is one of the most important aspects of the decision.
In this regard, only one viable option has the strongest position.
One of the main stakeholders (UID) is ready to provide a server for free.

The setup of Strato's servers in comparison to UID should be very similar. (not checked in practice)\
As can be seen from the sources, setting up an application on a cloud platform has its own complexity. (not checked in practice)

In addition, the cloud platform solution would also be vendor lock-in (proprietary solution)

Backups come with extra price by rented solutions.
