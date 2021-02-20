---
type: decision
acronym: logging
title: >
    Logging Strategy
decision_type: must
belongs_to: devops
status: _5_presented
responsible: JSP
deadline: 2021-02-19
implemented: partially
todos:
    - enhance logging style to "GET /uri"
    - a bit more detailed description for the logging
history:
    v1:
        date: 2021-02-13
        comment: created initially
---

## Why is there need for such a decision?

In case of problems at the production, it is importend to find informations about the scenario to resolve it at a local system.
For that a good logging strategy is important.

## Additional sources for better understanding the background

[wiki](https://github.com/EVATool/evatool-backend/wiki/logging).

## How is this decision evaluated?

There is not a really evaluated. It was choosen by the default which spring give you.

 
## Resolution Details

Please read the [wiki](https://github.com/EVATool/evatool-backend/wiki/logging) page for the explained structure with example.

