---
type: decision
acronym: sig-devops-build-pipeline
title: >
    Tool Chain for Build Pipeline - GitHub Actions vs. Jenkins
decision_type: must
belongs_to: devops
status: _5_presented
todos:
responsible: TZA;HBU
deadline: 2021-02-19
implemented: partially
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
    v4:
        date: 2021-02-09
        comment: added TODOs and cleaned up.
    v5:
        date: 2021-02-09
        comment: added new TODOs and some new information
    v6:
        date: 2021-02-12
        comment: Refined evaluation and did TODOs
---

## Why is there need for such a decision?

The application needs to be delivered to a server in order to be available.
This delivery process will be automated and will continuously deploy the newest version of the project to the server.
Each new version of application will be created as a docker image.
Then it should be transferred to server and run as a docker container. 
UID is providing a remote server.

The decision [Testing Automation with GitHub Actions](./sig-devops-testing-automation) was a short-term solution to enable testing automation earlier in the project.

## Additional sources for better understanding the background

- [CI/CD](https://en.wikipedia.org/wiki/CI/CD)
- [Continuous integration](https://en.wikipedia.org/wiki/Continuous_integration)
- [Continuous delivery](https://en.wikipedia.org/wiki/Continuous_delivery)
- [Jenkins (software)](https://en.wikipedia.org/wiki/Jenkins_(software))
- [GitHub Actions - Features](https://github.com/features/actions)
- [GitHub Actions - Documentation](https://docs.github.com/en/actions)
- [GitHub Actions - Workflow Syntax](https://docs.github.com/en/actions/reference/workflow-syntax-for-github-actions)
- [Jenkins website](https://www.jenkins.io/)
- [Run GitHub Actions locally](https://github.com/nektos/act)
- [GitHub vs Jenkins - Blog on bitsrc](https://blog.bitsrc.io/github-actions-or-jenkins-making-the-right-choice-for-you-9ac774684c8)
- [GitHub vs Jenkins - Blog on medium](https://medium.com/swlh/will-github-actions-kill-off-jenkins-f85e614bb8d3)

## Viable Options

- Realize build pipeline using GitHub Actions
    - build
    - test
    - transfer `jar` (deploy) to the server 
    - run the application

- Realize build pipeline using Jenkins (Execute the whole pipeline on the server with Jenkins)

## Alternatives not seriously considered

- Execute some portion (compile + test) on GitHub and the rest (build + deploy) on the server

## How is this decision evaluated?

- The solution should fit well into existing solutions
- It must be free (except the remote server)
- It should be resistant to changes happening in the project
- The open source nature of the project should not be put in jeopardy
- Multiple build jobs concurrently
- Solution must be able to listen to GitHub push event (full automation)

## Resolution Details

[Wiki](https://github.com/EVATool/evatool-backend/wiki/DevOps-Delivery)

Unique features of using GitHub Actions:
- No need to worry about infrastructure and scaling/running it
- GitHub Actions can be run locally and in the cloud
- No installation/setup required (!)
- No extra plugins that need to be kept up to date
- GitHub Actions workflow visualization (job graph)
- There is a GitHub Action for every GitHub event
- Configuration files can be managed in GitHub; no need to manually copy to server in order to build
- GitHub as host for repo as well as build pipeline (centralized)
- Easy access to GitHub API (Jenkins might require token?)
- GitHub Marketplace (over 4000 actions published since GitHub introduced CI tools)

Unique features of Jenkins on the remote server:
- Independent of GitHub (Microsoft)
- Plugins are available for cashing support

Our decision is GitHub Actions

## Reasons for the resolution

The initial setup of Jenkins do not fit the project at the moment and could lead to a time shortage
(This decision could be re-evaluated in the future depending on where the project stands).
The open source nature of GitHub Actions, and the nature of the project make GitHub Actions the far more superior solution.
