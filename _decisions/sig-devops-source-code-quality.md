---
type: decision
acronym: sig-devops-source-code-quality
title: >
    Tools and rulessets for code quality
decision_type: must
belongs_to: devops
status: _2_draft
responsible: MHA
deadline: 2021-01-29
todos:
    - deadline realistic & doable?
    - what is your way of evaluation?
history:
    v1:
        date: 2021-01-21
        comment: created initially
    v2:
        date: 2021-01-21
        comment: added background information
---

## Why is there need for such a decision?

Tools and rulessets for code quality leads to a improvement of the overall code of the project. With this it's more 
easy for multiple team members to understand code changes. It's also possible to ensure that the design is consistent 
with existing code, attempt to catch security problems early and get feedback on design approaches.

All teams must focus on one code-quality-tool or rulesset.

## Additional sources for better understanding the background

- [What is Code Quality? And How to improve Code Quality](https://www.perforce.com/blog/sca/what-code-quality-and-how-improve-code-quality)
- [What is Static Analysis? And What Is Static Code Analysis?](https://www.perforce.com/blog/sca/what-static-analysis)
- [Why Source Code Quality Is Crucial in Software Product Development](https://www.rabitse.com/blog/why-source-code-quality-is-crucial/)
- [Top 5 Open-Source and Commercial Secure Code Review Tools](https://resources.infosecinstitute.com/topic/top-5-open-source-and-commercial-secure-code-review-tools/)


## Viable Options

- Over-the-shoulder-code-review (fast project-integration, useful and fast results)
- Pair programming (fast project-integration, useful and fast results)
- Gerrit (Open source, easy to use, useful features)

## Alternatives not seriously considered

There are many medium/high-priced commercial code-quality-tools, which can't be used in this project. Three of them are for
example:
- Helix Core
- Klocwork
- Upsource

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

