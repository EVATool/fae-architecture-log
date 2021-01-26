---
type: decision
acronym: devops-testing-automation
title: >
    Testing Automation with GitHub Actions
decision_type: must
belongs_to: devops
status: _5_presented
responsible: HBU
deadline: 2021-01-22
todos:
history:
    v1:
        date: 2021-01-10
        comment: created initially
    v2:
        date: 2021-01-13
        comment: fixed the table and links
    v3:
        date: 2021-01-13
        comment: Added evaluation details
    v4:
        date: 2021-01-13
        comment: added one question
    v5:
        date: 2021-01-15
        comment: Refined decision and changed deadline
    v6: 
        date: 2021-01-22
        comment: status updated
    v7:
        date: 2021-01-22
        comment: refined options and solution
---

## Why is there need for such a decision?

How the code is tested *must* be decided early in order to guarantee a unified and efficient way to ensure quality. 
Automating tests is necessary when many developers are collaborating and are changing the code regulary.

This descision is a short-term decision that will feed into the later delivery and build toolchain descision.

## Additional sources for better understanding the background

- [Software Testing](https://en.wikipedia.org/wiki/Software_testing)
- [Types of Tests](https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing)
- [Automated Testing](https://en.wikipedia.org/wiki/Test_automation)
- [Blog about Automated and Manual Testing](https://www.perfecto.io/blog/automated-testing-vs-manual-testing-vs-continuous-testing)
- [GitHub Actions](https://docs.github.com/en/free-pro-team@latest/actions)
- [GitHub Action Pricing](https://docs.github.com/en/github/setting-up-and-managing-billing-and-payments-on-github/about-billing-for-github-actions)
- [Google Cloud](https://cloud.google.com/solutions/devops/devops-tech-test-automation)

## Viable Options

- GitHub Actions: GitHub Actions run when events on GitHub are fired (push, pull_request, etc.) and can be used for automated testing.
- Cloud-based Service: A third-party tool that runs tests on a dedicated server and returns their results.

## Alternatives not seriously considered

- None

## How is this decision evaluated?

The solution should be free of charge and have many resources in order to increase efficiency when working with it.
It is also desirable when the solution can be used for more than just testing but automation in general.
Additionally, a solution that fits into existing contraints is better due to easier integration.


| Criteria | GitHub Actions | Jenkins (Server) |
|:-:|:-:|:-:|
| Project (FAE) | GitHub already given as source control<br>The project might be put on hold for a few months at a time. In this time the free version of GitHub can still be used | Not integrated into source control |
| Price | Free<br>Java code can be tested on linux (best price).<br>Only 2000 worker minutes per month when free | Server costs money (rent, electricity)<br>Initial Setup over head<br>Continuous cost |
| Setup | Well known, many resources and existing actions | Jenkins has good resources |
| Availability | Might become temporarily unavailable; robust due to owner (Microsoft) | Might temporarily become unavailable |
| Support | Well known, many resources | Well known, many resources |
| Testing | Automated | Automated |
| Pipeline Integration | Integrates with other GitHub Actions<br>GitHub Events:<br>- delete<br>- release<br>- deployment<br>- check_run<br>- push<br>- pull_request<br>- …<br>GitHub Actions can execute arbitrary code and deliver output to a server (when delivering later on) | Depending on scope of service might not be competitive to GitHub |
| Verdict | Fits into existing parameters<br>Billing can be turned on and off according to project needs<br>Best automation and pipeline integration | Probably will cost money (continuously)<br>Inferior to GitHub in terms of project needs |


Using GitHub Actions requires something like Maven.

## Resolution Details

[Wiki article](https://github.com/EVATool/evatool-backend/wiki/DevOps-Testing-Automation-with-GitHub-Actions)

GitHub Actions can do much more than just automating testing. They will be used to extend the build tool chain
and automation in the project. GitHub Actions do not require a dedicated, self-managed build server and the testing results
are shown next to the pushed commit.

A third-party service was not tested. Setting up a server would cost money. They might be faster than GitHub Actions,
but this is not an option due to the nature of this project. 2000 minutes per month will probably suffice for this project
(if not, the paid version of GitHub Actions can be used - if the paid version is no longer required, it can be made 
free again).

GitHub Actions can deploy (send) their output to a third party server (a GitHub Action can execute arbitrary code).

Testing GitHub Actions:
- tested with Maven (tests in IDE and GitHub Action are the same, executed with maven command)
- there are many resources
- testing when pushing has been tested
- tests run on linux machines and are executed with workers on GitHub (take some time)
- tests will show as completed or failed in commit after they finished
- tests were deliberately made to [fail](https://github.com/EVATool/evatool-backend/commit/778701438ea4561a196e56ba5979425827217a56)
- tests [passed](https://github.com/EVATool/evatool-backend/commit/8c74f36e9c2acf4b752ee79654b229207767af68)

## Reasons for the resolution

Choosing an automated testing setup is a long term descision. It will cost some resources initially but will
save time and increase efficiency.
