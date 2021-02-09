---
type: decision
acronym: sig-devops-source-code-quality
title: >
    Tools and rulessets for code quality
decision_type: must
belongs_to: devops
status: _2_draft
responsible: MHA
deadline: 2021-02-12
history:
    v1:
        date: 2021-01-21
        comment: created initially
    v2:
        date: 2021-01-21
        comment: added background information
    v3:
        date: 2021-02-04
        comment: added way of evaluation
    v4:
        date: 2021-02-07
        comment: resolution details/reasons for the resolution added
---

## Why is there need for such a decision?

Tools and rulessets for code quality leads to a improvement of the overall code of the project. With this it's more 
easy for multiple team members to understand code changes. It's also possible to ensure that the design is consistent 
with existing code, attempt to catch security problems early and get feedback on design approaches. The overall "bug-searching-work"
will reduce, which leads to more time for the overall development.

All teams must focus on one code-quality-tool or rulesset.

## Additional sources for better understanding the background

- [What is Code Quality? And How to improve Code Quality](https://www.perforce.com/blog/sca/what-code-quality-and-how-improve-code-quality)
- [What is Static Analysis? And What Is Static Code Analysis?](https://www.perforce.com/blog/sca/what-static-analysis)
- [Why Source Code Quality Is Crucial in Software Product Development](https://www.rabitse.com/blog/why-source-code-quality-is-crucial/)
- [Top 5 Open-Source and Commercial Secure Code Review Tools](https://resources.infosecinstitute.com/topic/top-5-open-source-and-commercial-secure-code-review-tools/)
- [SonarCloud](https://sonarcloud.io/)
- [SonarQube](https://www.sonarqube.org/)
- [SonarQube Documentation + SonarLint](https://docs.sonarqube.org/latest/)


## Viable Options
#### Manual Rulessets
- Over-the-shoulder-code-review (fast project-integration, useful and fast results)
- Pair programming (fast project-integration, useful and fast results)
- Peer-reviews (fast project-integration, useful and fast results)
  
Further information on specific [wiki](https://github.com/EVATool/evatool-backend/wiki/Tools-and-Rulessets-for-Source-Code-Quality) page.
  
#### Automatic Tools- and Rulessets
- Find Bugs (IDE plugin)
- Check Style (IDE plugin)
- SonarQube
    - Sonar Lint (Local Analysis IDE plugin)
    - SonarCloud (Free Open Source static code analysis cloud (quality profiles, git repository analysis, dashboard, workflows
      etc.))
    - SonarQube (Equals to SonarCloud, must be installed on own server, much effort, few advantages)

Further information on specific [wiki](https://github.com/EVATool/evatool-backend/wiki/Tools-and-Rulessets-for-Source-Code-Quality) page.

## Alternatives not seriously considered

There are many **medium/high-priced commercial** or just to laborious code-quality-tools, which can't be used in this project:
- Helix Core
- Klocwork
- Upsource
- Gerrit (Positive: connectable with git, negative: check of every single commit, just too old)  
- ...

## How is this decision evaluated?

First, the manual as well as the automatic methods will be compared. Consider a decision here, the mentioned tools of the 
choosen method (manual / automatic) will be compared. This comparison will be based on a practical procedure. This includes 
some basic "bad-code", which will be analyzed with this tools. The best performing tool / rulesset will be choosen for this decision.
 
## Resolution Details

The manual methods mentioned before are suitable for the normal developer's everyday life, however, not as a main procedure
for ensuring source-code-quality. For this reason, they were not considered further for this decision.

The general focus instead was more on the automatic code-quality tools with their rulessets. Here, the previously 
mentioned code-quality tools were tested with the help of a deliberately poorly written code. The results can be seen on the [wiki](https://github.com/EVATool/evatool-backend/wiki/Tools-and-Rulessets-for-Source-Code-Quality) 
page.

It turned out that SonarLint is much more accurate and compact than the other tools, which ultimately led to the decision 
in favor of SonarLint.

## Reasons for the resolution

The advantage that SonarLint can also be extended with a cloud extension (SonarQube / SonarCloud) led to the final decision 
in favor of the source-code-quality tool SonarLint. However, it must be mentioned here that an implementation of a cloud-based 
extension (SonarQube / SonarCloud) would not be worthwhile for the remaining time of this project.



