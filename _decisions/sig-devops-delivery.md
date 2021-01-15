---
type: decision
acronym: sig-devops-delivery
title: >
    Application delivery - Tool Chain for Build Pipeline
decision_type: must
belongs_to: devops
status: _1_open
responsible: TZA
deadline: 2021-02-05
history:
    v1:
        date: 2021-01-13
        comment: created initially
    v2: 
        date: 2021-01-15
        comment: added responsible person, but it can be only temporary; First explanation of "Why is there need for such a decision?"
    v3: 
        date: 2021-01-15
        comment: viable options added; deadline updated; changed title
---


## Why is there need for such a decision?

The application need to be delivered on to some sort of server.
This delivery process should be automated.
It can be achieved using various pipeline tools.
It must be investigated which of the tools can be used easily and quickly for the project

(Please explain in 1-2 sentences why this is necessary to decide, and why it is a decision on the respective level
must / should / team)

### Questions and others

    Delivery: build -> test -> deploy -> run

* How to build? (see sig-devops-buildtools)
* How to test? (see sig-devops-testing-automation)
* How to deploy?
* How to run?

## Additional sources for better understanding the background

(Please list some sources where a reader can get a better understanding of the topic at hand)


## Viable Options

* Github-Actions
* Jenkins-Server
* Github-Actions + Deployment server


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

(If the resolation cannot be explained in 1-2 sentences, usually this section would contain a link to some
documentation in the Github wiki.)


## Reasons for the resolution

(Please explain in 1-2 sentences, why you ultimately opted for this resolution, and not for an alternative one.)

