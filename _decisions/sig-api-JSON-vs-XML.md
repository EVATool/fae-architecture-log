---
type: decision
acronym: sig-api-data_format
title: >
    JSON
decision_type: must
belongs_to: apis
status: _5_presented
todos:
    
responsible: JLÜ;JSP
deadline: 2021-01-15
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
    v7: 
        date: 2021-01-15
        comment: decision made
---

## Why is there need for such a decision?

Based on the Api style the different data representations are easier to implement. 

## Additional sources for better understanding the background

* [Differences between JSON and XML](https://rapidapi.com/blog/types-of-apis/)
* [JSON](https://www.json.org/json-de.html)
* [XML](https://wiki.selfhtml.org/wiki/XML)

## Viable Options

- JSON

## Alternatives not seriously considered

-XML : GraphQL does not support XML syntax. Moreover XML is not as flexible.

## How is this decision evaluated?

The Used Api-Style ist the main reason for choosing XML or JSON. After the decision for the api style has been taken, both data formats
are going to be tested with the style. on behalf of that a decision can be taken, considering speed, usability etc.


 
## Resolution Details

Resolution Details can be found on the [Wiki Page](https://github.com/EVATool/evatool-backend/wiki/JsonXMl).


## Reasons for the resolution
 
Both considered api styles are not made to use XML format.


