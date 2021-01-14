---
type: decision
acronym: sig-api-style
title: >
    API-Style  
decision_type: must
status: _1_open
responsible: JLÜ;JSP
deadline: 2021-01-22
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
---

## Why is there need for such a decision?

The Api-Style defines the way users  can access the provided resources. The Goal should be that all APIs can be accessed the same way, so the Client/User does 
not need different ways to access. Moreover, by using the same api style it will be easier to extend the functionality of the api. In addition to that it will be easier
to understand. 

All Teams must use the same style to reach this goal.

## Additional sources for better understanding the background

[Differences between SOAP and REST](https://rapidapi.com/blog/types-of-apis/)

[GraphQL](https://graphql.org/)

[REST Levels](https://blog.restcase.com/4-maturity-levels-of-rest-api-design/)

[Building a GraphQL API - video](https://www.youtube.com/watch?v=bRnu7xvU1_Y)

[REST, SOAP or GraphQl](https://da-14.com/blog/ultimate-guide-api-architecture-rest-soap-or-graphql#:~:text=SOAP%20is%20a%20protocol%2C%20REST,basic%20functions%20%E2%80%93%20GET%20and%20POST.&text=GraphQL%20leverages%20requests%20of%20two,and%20mutations%20changing%20the%20data)



## How is this decision evaluated?
To take the decision, research is necessary. Therefore, the differences between the different API-Styles have to be evaluated.
It is important that after the research, the preferred styles are implemented as prototype to compare them directly and get familiar with those styles.
With the results of the research a decision based on facts and experience can be taken.

Different aspects are going to be relevant for
the decision:
- Usability 
- Safety of the protocol
- does it fulfill all relevant aspects needed for the communication between backend and frontend 
- existing documentation of the protocol


 
## Resolution Details

(If the resolation cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)


## Reasons for the resolution

(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)

