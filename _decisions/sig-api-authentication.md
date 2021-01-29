---
type: decision
acronym: sig-api-authentication
title: >
    Access security through REST-API authentication methods
decision_type: must
belongs_to: apis
status: _2_draft
todos:
responsible: MTO
deadline: 2021-02-05
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

---

## Why is there need for such a decision?

In the computer and Internet environment, authentication ensures that the identity of a user can be proven and verified against a system. This could prevent unauthorized access to the API.

This decision is necessary so that only the requests made by the client to the API is allowed.
## Additional sources for better understanding the background
You can use the sources to provide a little insight on authentication methods.

* [Most Used REST API Authentication Methods](https://blog.restcase.com/4-most-used-rest-api-authentication-methods/)
* [How a RESTful API server reacts to requests. Chapter Authentication](https://www.oreilly.com/content/how-a-restful-api-server-reacts-to-requests/)
* [RFC: 6749, The OAuth 2.0 Authorization Framework](https://www.ietf.org/rfc/rfc6749.txt)

## Viable Options

- HTTP Authentication
- Auth0
- OAuth (2.0)
- OpenID Connect



## Alternatives not seriously considered

- HTTP Authentication
 - Basic Authentication: This method requests the username and password for each API request.
 - Bearer Authentication: This method wants to have a predefined token for each API request. The token is set in the header when the request is made. The token may not be set dynamically and it is written statically in the code.
- OpenID Connect: For OpenID Connect an external service provider is needed, this method would go beyond the scope of this project.

## How is this decision evaluated?

The decision must be guaranteed by a research on the Internet. Important points are, which authentication methods are generally available and which ones are recommended by the Spring-Boot community on the Internet.

By prototyping or designing two or more authentication methods in Java-Spring-Boot we try to make a decision.
Facts for the decision are:
- Security
- Simplicity
- How easy it is to code


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
## Reasons for the resolution

In the SIG API group, a decision was made with the help of the three facts.
OAuth2 is a modern and secure way to authenticate users. The abstract representation in RFC6749 makes this method very easy to understand. A quick to understand program code example is provided by [koushikkothagal](https://github.com/koushikkothagal/spring-security-jwt). An understanding of Java and OOP is required.
The OAuth (2.0) method was defined for authentication.


