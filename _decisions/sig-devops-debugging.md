---
type: decision
acronym: sig-devops-debugging
title: Local Debugging using Docker
decision_type: should
belongs_to: devops
status: _5_presented
responsible: TZA
deadline: 2021-02-19
todos:
history:
    v1:
        date: 2021-02-05
        comment: created initially
    v2:
        date: 2021-02-19
        comment: added decision info
---

## Why is there need for such a decision?

The development team must be able to debug the code.
Both with the help of the embedded application server (local)
and in the development software landscape (remote / dev-server)

## Additional sources for better understanding the background

None.

## Viable Options

* embedded spring boot tomcat only
* remote dev application\
  (The application runs on a remote server in a dedicated Dev-Docker container) 

## Alternatives not seriously considered

None.

## How is this decision evaluated?

* Simplicity of the setup
* How well the demands of development are met
* Needs of the project at the moment

 
## Resolution Details

Debugging with IntelliJ features, and the embedded Spring Boot Tomcat
is an easy way to go at the moment.

See [Wiki](https://github.com/EVATool/evatool-backend/wiki/Debugging)

## Reasons for the resolution

In the course of the project no debugging on a remote instance was necessary until now,
but this decision can be re-evaluated in the future.
