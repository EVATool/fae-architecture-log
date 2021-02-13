---
type: decision
acronym: sig-api-style
title: >
    API Style is REST Level 3  
decision_type: must
belongs_to: apis
status: _5_presented
responsible: JLÜ;JSP
deadline: 2021-02-12
todos:
    
history:
    v1:
        date: 2021-01-11
        comment: created initially
    v2:
        date: 2021-01-12
        comment: update responsibility
    v3:
        date: 2021-01-12
        comment: need for decision
    v4:
        date: 2021-01-12
        comment: sources and evaluation
    v5: 
        date: 2021-01-22
        comment: updated deadline    
    v6:
        date: 2021-01-28
        comment: add Resolution
    v7:
        date: 2021-02-12
        comment: state back to 4, how-to needed
---

## Why is there need for such a decision?

The Api-Style defines the way users  can access the provided resources. The Goal should be that all APIs can be accessed the same way, so the Client/User does 
not need different ways to access. Moreover, by using the same api style it will be easier to extend the functionality of the api. In addition to that it will be easier
to understand. 

All Teams must use the same style to reach this goal.

## Additional sources for better understanding the background

* [Differences between SOAP and REST](https://rapidapi.com/blog/types-of-apis/)
* [GraphQL](https://graphql.org/)
* [REST Levels](https://blog.restcase.com/4-maturity-levels-of-rest-api-design/)
* [Building a GraphQL API - video](https://www.youtube.com/watch?v=bRnu7xvU1_Y)
* [REST, SOAP or GraphQl](https://da-14.com/blog/ultimate-guide-api-architecture-rest-soap-or-graphql#:~:text=SOAP%20is%20a%20protocol%2C%20REST,basic%20functions%20%E2%80%93%20GET%20and%20POST.&text=GraphQL%20leverages%20requests%20of%20two,and%20mutations%20changing%20the%20data)


## Viable Options

- REST level 2 
- REST level 3
- GraphQL



## Alternatives not seriously considered

- Soap : not considered because it produces a lot of Overhead due to XML syntax 
- gRPC : not considered because it is made for realtime use cases, which is not required here


## How is this decision evaluated?
To take the decision, research is necessary. Therefore, the differences between the different API-Styles have to be evaluated.
It is important that after the research, the preferred styles are implemented as prototype to compare them directly and get familiar with those styles.
In specific the domain of the requirements is going to be implemented. As a first prototype basic methods are going to be implemented:

- get all : returns all Objects
- get for id : returns one Object by id
- create : creates a new object
- update : updates an existing object


With the results of the research a decision based on facts and experience can be taken.

Different aspects are going to be relevant for
the decision:
- Usability
- an existing documentation of the protocol
- standards  
- does it fulfill all relevant aspects needed for the communication between backend and frontend
- Safety of the protocol


 
## Resolution Details

The Decision is that Rest must be used as api style. In specific Rest level 3 must be used.
An example of how to implement can be found in the PoC [Rest Level 3](https://github.com/EVATool/evatool-poc/tree/main/RestLv3).


## Reasons for the resolution

The Explanation of the resolution can be found in the [wiki](https://github.com/EVATool/evatool-backend/wiki/ApiStyle).
