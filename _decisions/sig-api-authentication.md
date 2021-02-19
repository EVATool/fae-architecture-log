---
type: decision
acronym: sig-api-authentication
title: >
    Access security through REST-API authentication methods
decision_type: must
belongs_to: apis
status: _5_presented
todos:
    - please add a How-To for our specific project to the wiki
responsible: MTO
deadline: 2021-02-19
implemented: false
history:
    v1:
        date: 2021-01-12
        comment: created initially
    v2:
        date: 2021-01-14
        comment: edit need for decision
    v3:
        date: 2021-01-15
        comment: added "Viable Options", added "Alternatives not seriously considered, edit "How is this decision
         evaluated?"
    v4:
        date: 2021-01-22
        comment: added "Resolution Details" and "Reasons for the resolution"
    v5:
        date: 2021-01-29
        comment: edit "Resolution Details"
    v6:
        date: 2021-02-02
        comment: context adjusted
    v7:
        date: 2021-02-04
        comment: edit Reasons for the resolution



---

## Why is there need for such a decision?

In the computer and internet environment, authentication ensures that the identity of a user can be proven and verified against a system. This could prevent unauthorized access to the API. 
This decision is necessary so that only the requests made by the client to the API is allowed.

To better validate this decision we need to take a closer look at aspects such as access control and rights assignment.
In an environment with multiple users, administration is required. The administration must ensure that no unauthorized persons have access to the API and must also ensure that new users can be created and managed.
In the following scenarios are listed to understand why such a management is needed:
- The user account is created by an administrator, or the account is to be created by a person himself via a registration form.
- The user must be logged in to use the API. Roles are used to control read and write access.
- The user must be able to manage his account, such as changing the password.
- A role manage is needed to allow areas of the API only for the respective role.


## Additional sources for better understanding the background
You can use the sources to provide a little insight on authentication methods.

* [Most Used REST API Authentication Methods](https://blog.restcase.com/4-most-used-rest-api-authentication-methods/)
* [How a RESTful API server reacts to requests. Chapter Authentication](https://www.oreilly.com/content/how-a-restful-api-server-reacts-to-requests/)
* [RFC: 6749, The OAuth 2.0 Authorization Framework](https://www.ietf.org/rfc/rfc6749.txt)
* [About Keycloak](https://www.keycloak.org/about)

## Viable Options

- Self implemented user management
- Identity and access management like keycloak

## Alternatives not seriously considered

- HTTP Authentication
    - Basic Authentication: This method requests the username and password for each API request and the password is hardcoded in the API.

## How is this decision evaluated?

The decision must be guaranteed by a research on the Internet. Important points are, which authentication methods are generally available and which ones are recommended by the Spring-Boot community on the Internet.

Facts for the decision are:
- Security
- Simplicity
- How easy it is to code
- Easy maintenance

## Resolution Details

OAuth 2.0 Protocol Flow

     +--------+                               +---------------+
     |        |--(A)- Authorization Request ->|   Resource    |
     |        |                               |     Owner     |
     |        |<-(B)-- Authorization Grant ---|               |
     |        |                               +---------------+
     |        |
     |        |                               +---------------+
     |        |--(C)-- Authorization Grant -->| Authorization |
     | Client |                               |     Server    |
     |        |<-(D)----- Access Token -------|               |
     |        |                               +---------------+
     |        |
     |        |                               +---------------+
     |        |--(E)----- Access Token ------>|    Resource   |
     |        |                               |     Server    |
     |        |<-(F)--- Protected Resource ---|               |
     +--------+                               +---------------+

Source: [RFC: 6749, The OAuth 2.0 Authorization Framework](https://www.ietf.org/rfc/rfc6749.txt)

- A: The client authorizes itself with username and password.
- B/C: If the input data is correct, a token is requested.
- D: The client gets a time limited access token.
- E: The API can be called by a valid token.
- F: The requested resource is returned by using a valid token.

Additionally, there must be an implementation that returns a fresh token to the logged user after the current token expires.

There are two ways to implement access control and rights assignment.
Self-implementation: In this case, the management of access control and rights assignment is completely self programmed.
- Controllers are needed to manage the rights of the users.
- Controllers are needed to create and manage users.
- A database for the user administration must be created.
- Passwords have to be secured by security measures like hashing.
- Personal data must be secured.

The second option is via an Identity and Access Management solution. Identity and Access Management solution aimed at modern applications and services. It makes it easy to secure applications and services (APIs) with little to no code.
In addition to this, this solution offers many interfaces e.g. to social logins.
For the most part, there is configuration overhead with this solution. The implementation effort mentioned in the previous paragraph is omitted.
- Roles and rights must be created.
- The connection between these services and the project must be established. 
- The roles for the individual URIs must be stored in the controllers, e.g. in Spring via annotations.

[Here](https://github.com/EVATool/evatool-backend/wiki/Keycloak-Identity-and-Access-Management) you can find a tutorial on how to integrate Keycloak into a Spring application.

## Reasons for the resolution

Based on a thorough research on the Internet and by comparing completed or running projects, an Identity and Access Management solution is a beneficial solution.
The service requires a small configuration effort to connect it to a Spring application.
[Keycloack](https://www.keycloak.org/) is free, open source and there is currently no better solution.




