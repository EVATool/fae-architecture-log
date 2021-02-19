---
type: decision
acronym: sig-api-uristyle
title: >
    The Uri style is lower camel case
decision_type: must
belongs_to: apis
status: _5_presented
responsible: JLÜ
deadline: 2021-02-19
history:
    v1:
        date: 2021-02-12
        comment: created initially
---

## Why is there need for such a decision?

To have an identical style to access resources a unified URI style is needed. 

## Additional sources for better understanding the background

[Rest Api Style](https://entwickler.de/online/web/restful-api-design-intro-579826380.html)
[URI Style](https://blog.restcase.com/5-basic-rest-api-design-guidelines/)

## Viable Options

* CamelCase
* spinal-case


## Alternatives not seriously considered

* snake_case



## How is this decision evaluated?

This is a no-brainer, because it is only a decision based on the most like URI case.

 
## Resolution Details

The URI case is the lowerCamelCase. 

## Reasons for the resolution

Most of the people know how the CamelCase works and are familiar with it. Moreover, it is a very common URI Style.

