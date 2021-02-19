---
type: decision
acronym: conventions-for-rest-return-codes
title: Conventions for REST return codes and error handling
decision_type: must
belongs_to: apis
status: _5_presented
responsible: JLÜ
deadline: 2021-02-19
todos: 
        - 404 needs to be covered in wiki (automatically if the URI is not there, if entity not there, then we need to
         throw)
        - explain 405 as "method is not allowed", as e.g. "DELETE /requirements". Needs not to be implemented by the
            developer.  
        - 422 for all kind of semantic errors in the dto
        - 400 for generic client 
        - 403 is thrown by keycloak
        - 409 we don't need currently (conflict), might come in the future
        - 204 is not used (use 200 or 201 instead)
history:
    v1:
        date: 2021-02-12
        comment: created initially
---

## Why is there need for such a decision?

This should be uniform across the REST APIs.

## Additional sources for better understanding the background

* [Inhaltsimpuls Bente: Grundlagen von REST](https://ilias.th-koeln.de/goto.php?target=file_1807406_download&client_id=ILIAS_FH_Koeln)
* zugehörige Video-Mitschnitte in der Knowledge Map

## Viable Options

n/a

## Alternatives not seriously considered

n/a

## How is this decision evaluated?

No evaluation needed.

 
## Resolution Details

The resolution details can be found in the [wiki](https://github.com/EVATool/evatool-backend/wiki/httpreturncodes)

## Reasons for the resolution

n/a
