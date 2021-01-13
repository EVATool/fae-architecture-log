---
type: decision
acronym: devops-testing-automation
title: >
    Testing Automation
decision_type: must
status: _1_open
responsible: HBU
deadline: 2021-01-22
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
---

### Questions [only temporary chapter]

* Can Github-Actions build the application and deploy it on to some host (server)?

## Why is there need for such a decision?

How the code is tested *must* be decided early in order to guarantee a unified and efficient way to ensure quality. 
Automating tests is necessary when many developers are collaborating and are changing the code regulary.

## Additional sources for better understanding the background

- [Software Testing](https://en.wikipedia.org/wiki/Software_testing)
- [Types of Tests](https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing)
- [Automated Testing](https://en.wikipedia.org/wiki/Test_automation)
- [Blog about Automated and Manual Testing](https://www.perfecto.io/blog/automated-testing-vs-manual-testing-vs-continuous-testing)
- [GitHub Actions](https://docs.github.com/en/free-pro-team@latest/actions)
- [Google Cloud](https://cloud.google.com/solutions/devops/devops-tech-test-automation)

## How is this decision evaluated?

The solution must be free and have many resources in order to increase efficiency when working with it.
It is also desirable when the solution can be used for more than just testing but automation in general.
Additionally, a solution that fits into existing contraints is better due to easier integration.

There are three candidates:
- GitHub Actions
- Cloud-based Service
- Manual Tests

| Criteria | GitHub Actions | Cloud-based | Manual Tests |  |
|-----|-----|-----|-----|-----|
| Project (FAE) | GitHub already given as source control | Not integrated into source control | Not integrated into source control |  |
| Acquisition | Free<br>Less computational power due to no cost | Might cost money if very powerful, but not powerful enough if free<br>Even if free and OK, using GitHub would be more sound | Might cost money if very powerful |  |
| Setup | Well known, many resources and existing actions | Might not be as well known, less resources | Most IDEs have integrated Tests or have plugins + well known IDEs have good resources |  |
| Availability | Might become temporarily unavailable, but robust due to owner (Microsoft) | Might temporarily become unavailable<br>Robust if paid | Robust, Cannot become unavailable |  |
| Support | Well known, many resources | Good support if paid | A lot of good IDEs are free and have many resources |  |
| Testing | Automated | Automated | Not automated |  |
| Pipeline Integration | Integrates with other GitHub Actions<br>GitHub Events:<br>- delete<br>- release<br>- deployment<br>- check_run<br>- push<br>- pull_request<br>- ... | Depending on scope of service might not be competitive to GitHub | Does not support as many CI/CD Tools like GitHub<br>For example, Visual Studio does but costs money |  |
| Verdict | Fits into existing parameters<br>Best automation and pipeline integration | Probably will cost money<br>Inferior to GitHub in terms of integration and reputation | Good but lacks automation and pipeline integration |  |

Using GitHub Actions requires something like Maven.

## Resolution Details

Manual testing was only considered to show the superiority of automated testing.

GitHub Actions can do much more than just automating testing. They will be used to extend the build tool chain
and automating in the project.

Testing GitHub Actions:
- there are many resources
- testing and building when committing has been tested
- tests run on linux machines and are executed with workers on GitHub
- tests will show as completed or failed in commit after they finished

## Reasons for the resolution

Choosing an automated testing setup is a long term descision. It will cost some resources initially but will
save time and increase efficiency. Manual testing is tedious and a third party cloud based service would either
add running costs to the project or be not as easy and good as GitHub Actions.
