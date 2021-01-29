---
type: decision
acronym: preferred-way-of-synchronous-communication
title: >
    The preferred way of synchronous communication between modules are api calls
decision_type: must
belongs_to: apis
status: _5_presented
responsible: JLÜ
deadline: 2021-01-29
history:
    v1:
        date: 2021-01-15
        comment: created initially
    v2:
        date: 2021-01-29
        comment: filled out
---

## Why is there need for such a decision?

Sometimes synchronous calls between APIs are necessary. Therefore, a decision dealing this issue is required. All APIs 
must use the same way of synchronous communication.

## Additional sources for better understanding the background

[Sync vs async](https://dzone.com/articles/patterns-for-microservices-sync-vs-async)

[Methods of Communication](https://blog.logrocket.com/methods-for-microservice-communication/)

[Synchrone Kommunikation Rest](https://entwickler.de/leseproben/rest-synchron-579868798.html)

## Viable Options

* Api calls


## Alternatives not seriously considered

No other alternatives are seriously considered.


## How is this decision evaluated?

To take this decision some research has to be done. No other evaluation is required.

 
## Resolution Details

In oder to make synchronous calls the domains must call the API. The API should already offer all required cases of synchronous calls.
If it is not the case, the API has to implement it.

## Reasons for the resolution

Synchronous Calls should not be used. However sometimes they are necessary. Because the APIs should already cover all cases 
of synchronous communication, the resolution is fairly simple.

