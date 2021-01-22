---
type: decision
acronym: doc-in-github
title: >
    All documentation (apart from the decision log itself) has to be stored in a Github wiki, in repo 
    evatool-backend
decision_type: must
belongs_to: devops
status: _5_presented
responsible: SBE;PKL
deadline: 2021-01-22
todos:
    - Present solution to whole group 
history:
    v1:
        date: 2021-01-08
        comment: created initially
    v2:
        date: 2021-01-09
        comment: added reasoning
                
---

## Why is there need for such a decision?

We need to have one (central!) location for all documentation, since the project is supposed to live on, after
FAE has been finished. 

## Additional sources for better understanding the background

* Github wiki documentation, e.g. [this cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* [Atlassian Confluence](https://www.atlassian.com/de/software/confluence) 
* [Microsoft Teams](https://www.microsoft.com/de-de/microsoft-teams/group-chat-software)


## Viable Options

* Github wiki


## Alternatives not seriously considered

* Confluence
* MS Teams 
* just the README in a Github repo
* other commercial solutions for documentation


## How is this decision evaluated?

Alternatives are fairly obvious (see "additional sources"). Decision criteria is the goal to start an open source
project. Hands-on evaluation is not really needed in this case - using a Github wiki is a no-brainer. It offers
reasonable means for structuring complex content, while being free, and being closely related to our code
repository. 
 
## Resolution Details

Documentation will be stored in the wiki of repo evatool-backend. Its content can be assessed through this link: 
[https://github.com/EVATool/evatool-backend/wiki](https://github.com/EVATool/evatool-backend/wiki)

Wikis in Github are dedicated repos. You can edit in the web interface, but the safer and more comfortable way
is to work locally. Technically, a Github wiki is a seperate repo named the same as the "mother repo", just
with the addition `.wiki`. You can clone it using the following command:  

`git clone https://github.com/EVATool/evatool-backend.wiki.git`

The wiki structure has been initialized. It should be fairly self-explanatory. Feel free to enhance the structure. 


## Reasons for the resolution

In this case, decision is easy. To initiate a proper open source project, the documentation needs to be 
publically accessible. That leaves only Github wiki as a viable option.  

