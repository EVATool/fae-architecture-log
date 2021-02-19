---
type: decision
acronym: conventions-for-rest-uris
title: Conventions for REST URIs
decision_type: must
belongs_to: apis
status: _5_presented
responsible: SBE
deadline: 2021-02-12
history:
    v1:
        date: 2021-02-12
        comment: created initially
---

## Why is there need for such a decision?

All REST APIs in this applications should have a similar structure.

## Additional sources for better understanding the background

* [Inhaltsimpuls Bente: Grundlagen von REST](https://ilias.th-koeln.de/goto.php?target=file_1807406_download&client_id=ILIAS_FH_Koeln)
* zugehörige Video-Mitschnitte in der Knowledge Map

## Viable Options

1. The REST APIs take the following structure: `/aggregate-name-in-plural`
    * e.g. `https://evatool.com/requirements`, `https://evatool.com/stakeholders`
    * there are no URI elements to indicate the subdomain or anything else, like e.g. `/api/...` or `/rest/...`
1. Each subdomain offers only its "own" entities/aggregates. No imported entities are exposed

The second rule means that in a screen where there is e.g. a requirements table and a variants selector, two
different API calls are needed by the client. This, however, is anyway the case, and can therefore be tolerated.

## Alternatives not seriously considered

n/a

## How is this decision evaluated?

No evaluation needed.

 
## Resolution Details

See viable options.

## Reasons for the resolution

Mainly simplicity.
