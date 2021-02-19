---
type: decision
acronym: sig-devops-sonar-quality-gate
title: >
    Definition of Quality Gates in Sonarcloud
decision_type: should
belongs_to: devops
status: _5_presented
responsible: MHA
deadline: 2021-02-19
history:
    v1:
        date: 2021-02-12
        comment: created initially
    v2: 
        date: 2021-02-17
        comment: added way of evaluation / resolution details
---

## Why is there need for such a decision?

We need to define what our quality standards for our project are.

At the moment it is set to a default value.

## Additional sources for better understanding the background

- [Quality Gates](https://sonarcloud.io/documentation/user-guide/quality-gates/)
- [New Code Definition](https://sonarcloud.io/documentation/user-guide/new-code/)
- [Clean as you code](https://sonarcloud.io/documentation/user-guide/clean-as-you-code/)


## Viable Options

- No Quality Gate
- Standard Quality Gate (Sonarway)
- Improved Quality Gate  

Further information on specific [wiki](https://github.com/EVATool/evatool-backend/wiki/Sonarcloud-Quality-Gates) page.


## Alternatives not seriously considered

N/A


## How is this decision evaluated?

A decision is made with the help of the official Sonarcloud documentation.

 
## Resolution Details

The decision was made to use the standard Quality Gate ***Sonarway***. This Quality Gate has been extended by three 
additional conditions, which should analyze the **overall** code.

Further information on specific [wiki](https://github.com/EVATool/evatool-backend/wiki/Sonarcloud-Quality-Gates) page.


## Reasons for the resolution

According to the official documentation, the default ***Sonarway*** Quality Gate is perfectly sufficient. For a better 
overall view, additional *overall* conditions can be added according to the documentation. This step has also been realized 
and can be seen in the [wiki](https://github.com/EVATool/evatool-backend/wiki/Sonarcloud-Quality-Gates).

