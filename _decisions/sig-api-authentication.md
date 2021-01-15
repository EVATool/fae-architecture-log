---
type: decision
acronym: sig-api-authentication
title: >
    Access security through REST-API authentication methods
decision_type: must
status: _1_open
responsible: MTO
deadline: 2021-01-22
history:
    v1:
        date: 2021-01-12
        comment: created initially
    v2:
        date: 2021-01-14
        comment: edit need for decision
---

## Why is there need for such a decision?

In the computer and Internet environment, authentication ensures that the identity of a user can be proven and verified against a system. This could prevent unauthorized access to the API.

This decision is necessary so that only the requests made by the client to the API is allowed.
## Additional sources for better understanding the background
You can use the sources to provide a little insight on authentication methods.

[Most Used REST API Authentication Methods](https://blog.restcase.com/4-most-used-rest-api-authentication-methods/)

[How a RESTful API server reacts to requests. Chapter Authentication](https://www.oreilly.com/content/how-a-restful-api-server-reacts-to-requests/)


## How is this decision evaluated?

The decision must be guaranteed by a research on the Internet. Important points are, which authentication methods are generally available and which ones are recommended by the Spring-Boot community on the Internet.

By prototyping or designing two or more authentication methods in Java-Spring-Boot we try to make a decision.
Facts for the decision are:
- Security
- Simplicity
- How easy it is to code

## Resolution Details

(If the resolation cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)


## Reasons for the resolution

(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)

