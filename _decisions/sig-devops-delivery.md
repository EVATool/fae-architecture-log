---
type: decision
acronym: sig-devops-delivery
title: >
    Application delivery - Tool Chain for Build Pipeline
decision_type: must
belongs_to: devops
status: _2_draft
todos: 
responsible: TZA, HBU
deadline: 2021-02-15
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
---

## Why is there need for such a decision?

The application needs to be delivered to a server in order to be availble.
This delivery process will be automated and will continuously deploy the newest version of the project to the server.
UID is providing a remote server.

The decision `devops-testing-automation` was a short-term solution to enable testing automation earlier in the project.

## Additional sources for better understanding the background

- [GitHub Actions - Features](https://github.com/features/actions)
- [GitHub Actions - Documentation](https://docs.github.com/en/actions)
- [GitHub Actions - Workflow Syntax](https://docs.github.com/en/actions/reference/workflow-syntax-for-github-actions)
- [Jenkins website](https://www.jenkins.io/)
- [Run GitHub Actions locally](https://github.com/nektos/act)
- [GitHub vs Jenkins - Blog on bitsrc](https://blog.bitsrc.io/github-actions-or-jenkins-making-the-right-choice-for-you-9ac774684c8)
- [GitHub vs Jenkins - Blog on medium](https://medium.com/swlh/will-github-actions-kill-off-jenkins-f85e614bb8d3)

## Viable Options

- Execute the whole pipeline on the server with Jenkins
- Execute all steps that can run on GitHub (with GitHub Actions) on GitHub and deploy to the server + run the application

## Alternatives not seriously considered

- Execute some portion (compile + test) on GitHub and the rest (build + deploy) on the server

## How is this decision evaluated?

- The solution should fit well into existing solutions
- It must be free (except the remote server)
- It should be resistant to changes happening in the project
- The open source nature of the project should not be put in jeopardy

## Resolution Details

TODO: make CI work with UID server...
TODO: Wiki link...

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
