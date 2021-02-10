---
type: decision
acronym: sig-devops-delivery
title: >
    Application delivery - Tool Chain for Build Pipeline
decision_type: must
belongs_to: devops
status: _2_draft
todos:
    - implement and test PoC with GitHub-Actions
    - research Jenkins-Server solution
    - get access to server from UID (with SSH)
    - try to use personal machines as a public available server 
    - create wiki
responsible: TZA;HBU
deadline: 2021-02-19
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
---

## Why is there need for such a decision?

The application needs to be delivered to a server in order to be available.
This delivery process will be automated and will continuously deploy the newest version of the project to the server.
Each new version of application will be created as a docker image.
Then it should be transferred to server and run as a docker container. 
UID is providing a remote server.

The decision `devops-testing-automation` was a short-term solution to enable testing automation earlier in the project.

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

### Questions and others (temporary)

* How to build? (see sig-devops-buildtools)
* How to test? (see sig-devops-testing-automation)
* How to deploy? (see sig-devops-container)
* How to run? (see sig-devops-container)

## Viable Options

- Realize build pipeline using GitHub Actions (Execute all steps that can run on GitHub on GitHub and deploy to the server + run the application)
- Realize build pipeline using Jenkins (Execute the whole pipeline on the server with Jenkins)

## Alternatives not seriously considered

- Execute some portion (compile + test) on GitHub and the rest (build + deploy) on the server

## How is this decision evaluated?

- The solution should fit well into existing solutions
- It must be free (except the remote server)
- It should be resistant to changes happening in the project
- The open source nature of the project should not be put in jeopardy

TODO: add more criteria

## Resolution Details

[Wiki](https://github.com/EVATool/evatool-backend/wiki/DevOps-Delivery)

TODO: make CI work with UID server...

Advantages of using GitHub Actions:
- Free
- No need to worry about infrastructure and scaling/running it
- GitHub is well known for open source projects (repo staying on GitHub)
- GitHub Actions can be run locally and in the cloud
- No installation/setup required
- No extra plugins that need to be kept up to date
- Asynchronous, no concurrency (multiple independant workflows possible, workflow diagram)
- GitHub Actions are a series of cloud-based docker runs (easy to run and debug)
- There is a GitHub Action for ever GitHub event
- The actions themself exist as yaml files and can be shared/reused like normal code
- GitHub Actions are tightly intertwined with the source control on GitHub itself
- Access to GitHub API (cross-repo update of code, automated pull requests etc.)
- Easily shared and used via GitHub Marketplace
- Deployment: App is stopped -> new docker image is loaded -> docker image is started again (maybe 15 seconds down time?) and no other down time or workload on the server
- What is in 5/10/20 years? Can UID still provide the server?
- Bigger community, more releases of new actions onto the marketplace
- Even if paid, cheaper than Jenkins on server
- Requires less testing than Jenkins

Advantages of Jenkins on the remote server:
- Independant of GitHub (Microsoft)
- Plugins are available for cashing support

## Reasons for the resolution

The open source nature of GitHub and the nature of the project make GitHub Actions the far more superior solution.
The initial setup and running costs of Jenkins do not fit the project.
