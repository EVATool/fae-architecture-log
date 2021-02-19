---
type: decision
acronym: API Code Framework
title: >
    Web MVC with manual link
decision_type: should
belongs_to: apis
status: _5_presented
responsible: JSP
deadline: 2021-02-12
history:
    v1:
        date: 2021-01-30
        comment: created initially
    v2:
        date: 2021-02-05
        comment: update deadline
    v3:
        date: 2021-02-07
        comment: decide decision
---

## Why is there need for such a decision?


It should be indicated whether an automatically generated URL is normally used for the subdomains or a manually generated URL.
The reason is that it would be better if everyone was using the same thing so that a new user would understand each controller the same way.

## Additional sources for better understanding the background

You can find a poc in followed [gitProject](https://github.com/EVATool/evatool-poc) under module "SpingData_vs_ManualLink".


## Viable Options

+ Spring Data Rest
+ Web MVC with manual link

## How is this decision evaluated?

The decision is evaluated by a proof of concapt and the aspect that you need a controller to implement DTO-classes with Spring Data Rest.

 
## Resolution Details

The resolution is that the teams should generate manual Links and not use Spring Data Rest.


## Reasons for the resolution

The reason for this is that you need a controller in order to realize DTO classes.
So if you must have a controller in this project case, you can diractly use the manual Link generation.
It's better to read and for new users good to understand the URI for REST.



