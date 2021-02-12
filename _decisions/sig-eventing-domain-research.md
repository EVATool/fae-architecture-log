---
type: decision
acronym: sig-eventing-domain-research
title: >
    Research method to define the domain is Domain Story Telling
decision_type: should
belongs_to: eventing
status: _5_presented
todos:
responsible: KRU;DUZ
deadline: 2021-01-29
history:
    v1:
        date: 2021-01-15
        comment: created initially
    v2:
        date: 2021-01-19
        comment: added sources
    v3:
        date: 2021-01-20
        comment: added not considered alternatives
    v4:
        date: 2021-01-22
        comment: added how this decision will be evaluated and changed the title
    v5:
        date: 2021-01-27
        comment: added resolution details and reasons for the resolution
    v6:
        date: 2021-01-27
        comment: presented
---

## Why is there need for such a decision?

Decision is required for a unified understanding of domains and process flows.


## Additional sources for better understanding the background

* [Event-Storming](https://www.knowis.com/de/blog/die-event-storming-methode-einsatz-im-projektalltag)
    * [Further information about Event Storming by the Creator Alberto Brandolini](https://blog.avanscoperta.it/2014/02/12/introducing-event-storming/)
    * [Full post here](http://ziobrando.blogspot.com/2013/11/introducing-event-storming.html)
* [Domain-Storytelling](https://domainstorytelling.org/)
    * [Further information](https://www.informatik-aktuell.de/management-und-recht/projektmanagement/fachliche-anforderungen-in-der-softwareentwicklung-wie-domain-storytelling-entwickler-und-fachexperten-zusammenbringt.html)


## Viable Options

* Event-Storming
* Event-Storytelling
* Domain-Storytelling


## Alternatives not seriously considered

* Mindmapping
    * Too simple for a proper Domain research
* Brainstorming
    * Could lead to overload


## How is this decision evaluated?

The decision needs to be evaluated by research. Usually the workshops would take place on site.
Therefore, it must also be evaluated whether the methods can be carried out online.
Finally, a tool is needed that supports collaborative online work.


## Resolution Details

We decided to use Domain Storytelling because it is best suited for domain modeling on remote. See further details
in 'Reasons for the resolution'.


## Reasons for the resolution

Event-Storytelling will be excluded because it is not applicable for domain research.
That method will be used for Events in reallife, not Server-Events. See [Event-Storytelling](https://wearesparks.com/blog/event-storytelling).

Event-Storming would be a great opportunity to create a Big Picture. But it is hard to handle online.
From experience we can say that this method won't work out well this way. Also Alberto Brandolini, the creator of
Event-Storming, wrote an article about remote Event-Storming, see [Remote EventStorming](https://blog.avanscoperta.it/2020/03/26/remote-eventstorming/).
He rejects the creation of a big picture on remote, because too much of the value would be lost.

