---
type: decision
acronym: sig-api-data_format
title: >
    JSON vs XML
decision_type: must
status: _4_stakeholder_checked
responsible: JLÜ;JSP
deadline: 2021-01-22
history:
    v1:
        date: 2021-01-11
        comment: created initially
    v2:
        date: 2021-01-12
        comment: rename
    v3:
        date: 2021-01-12
        comment: update responsibility
    v4:
        date: 2021-01-12
        comment: need for decision and sources
    v5:
        date: 2021-01-12
        comment: evaluation
    v6: 
        date: 2021-01-14
        comment: update status and update decision
---

## Why is there need for such a decision?

Based on the Api style the different data representations are easier to implement. 

## Additional sources for better understanding the background

[Differences between JSON and XML](https://rapidapi.com/blog/types-of-apis/)

[JSON](https://www.json.org/json-de.html)

[XML](https://wiki.selfhtml.org/wiki/XML)

## How is this decision evaluated?

The Used Api-Style ist the main reason for choosing XML or JSON. After the decision for the api style has been taken, both data formats
are going to be tested with the style. on behalf of that a decision can be taken, considering speed, usability etc.


 
## Resolution Details

Due to the api styles which are considerd (REST and GraphQL) it is reasonable to use JSON format. Both styles are made to work 
with JSON or to handle JSON-Data.


## Reasons for the resolution
 
Both api styles are not made to use XML format.


