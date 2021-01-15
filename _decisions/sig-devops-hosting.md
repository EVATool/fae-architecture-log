---
type: decision
acronym: sig-devops-hosting
title: >
    Choice of Hosting provider
decision_type: must
belongs_to: devops
status: _1_open
responsible: 
deadline: 2021-01-22
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v2:
        date: 2021-01-13
        comment: changed the deadline; added one aspect
---

## Important aspects of the decision

* The solution must be proprietary

---



## Why is there need for such a decision?

(Please explain in 1-2 sentences why this is necessary to decide, and why it is a decision on the respective level
must / should / team)

## Additional sources for better understanding the background

(Please list some sources where a reader can get a better understanding of the topic at hand)


## Viable Options

(Please list those options that you seriously consider as a possible solution. Simple bulleted list with a brief 
1-sentence explanation is sufficient.)


## Alternatives not seriously considered

(Here comes a list of alternatives that you can exclude right away, without an in-depth evaluation. Format: 
Simple bulleted list with a brief 1-sentence explanation is sufficient.)



## How is this decision evaluated?

(**Before** you start working in this, please write down how you will evaluate this decision, and plan to 
come to a resolution. 
It is  **not sufficient** to perform a brief Google search, and then write  the "result" down. Any decision must
**always** be based on a thorough evaluation - if possible hands-on, i.e. by coding a brief proof-of-concept.
if this doesn't apply, then some other means of proper research must be given here - e.g. an evaluation of 
the most relevant literature or IT community sources.) 

 
## Resolution Details


### Server prices

| Provider | Servertype | RAM (GB) | SSD (GB) | Price* (€) | Price** (€) | Note |
|---|---|---|---|---|---|---|
| Strato | V-Server | 32 | 800 | 17 | 11,5 | |
| IONOS (1&1) | V-Server | 24 | 240 | 36 | 27 | |
| Strato | Dedicated Server | 32 | 960 | 70 | 57,75 | + 39 € for setting up; basic - no addons |
| IONOS (1&1) | Dedicated Server | 32 | 480 | 70 |  | no Backup |
| DigitalOcean | V-Server | 16 | 320 | 80 $ | | |
| Azure | V-Server | 32 | 200 | 67 $ | | |

    * per month
    ** per month with 1 year contract

(If the resolation cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)


## Reasons for the resolution

(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)

