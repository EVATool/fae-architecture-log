---
layout: default
---

# Documentation

This page contains some rudimentary documentation for the decision process used in FAE for
the EVATool prototype.


## Decision Types

These are the decision types used in the architectural decision process.

| Symbol | Type | Explanation |
|-----|-----|-----|
| <img src="{{ site.url }}{{ '/assets/error-4-24.png' | relative_url }}" alt="Error"> | Error | There are __errors__ in the decision description; please fix immediately. |
| <img src="{{ site.url }}{{ '/assets/clipboard-4-24.png' | relative_url }}" alt="Todos"> | Todo | There are __todos__ in the decision; must be fixed before closing. |
| <img class=_0_neutral src="{{ site.url }}{{ '/assets/letter-m-16.png' | relative_url }}" alt="Must"> | Must | A decision (principle, solution, technology etc.) that is binding for **all** teams. Icon color indicates decision status (see tables below).  | 
| <img class=_0_neutral src="{{ site.url }}{{ '/assets/letter-s-16.png' | relative_url }}" alt="Must"> | Should | A decision that is a **recommendation** for all teams, e.g. a technology that seemingly works well; teams can still deviate if they have good reasons to do so. Deviations must be reasoned by a team decision (see below).  Icon color indicates decision status (see tables below).   | 
| <img class=_0_neutral src="{{ site.url }}{{ '/assets/letter-t-16.png' | relative_url }}" alt="Team"> | Team | Team decision; can be taken without consulting anyone outside the team.  Icon color indicates decision status (see tables below). | 



## Possible Status for "Must" and "Should"

"Must" and "Should" decisions can go through the following status (explained for "Must", but "Should" has the same
 status names and color codes).

| Symbol | Keyword in Decision Log | Status | Explanation |
|-----|-----|-----|-----|
| <img class=_1_open src="{{ site.url }}{{ '/assets/letter-m-16.png' | relative_url }}" alt="open"> | _1_open | Open | An open decision has been created, but no resolution is available yet | 
| <img class=_2_draft src="{{ site.url }}{{ '/assets/letter-m-16.png' | relative_url }}" alt="draft"> | _2_draft | Draft | A resolution is available and documented, but there has not yet been a discussion about it. | 
| <img class=_3_sig_agreed src="{{ site.url }}{{ '/assets/letter-m-16.png' | relative_url }}" alt="draft"> | _3_sig_agreed | Agreed in SIG | The resolution has been discussed and agreed upon in the SIG to which the decision belongs. | 
| <img class=_4_stakeholder_checked src="{{ site.url }}{{ '/assets/letter-m-16.png' | relative_url }}" alt="draft"> | _4_stakeholder_checked | Checked with Stakeholders | The resolution has been checked with the stakeholders (Prof. Bente, UID) for quality of reasoning and documentation, and possible side effects. There are no objections (otherwise the decision would go back to draft state). | 
| <img class=_5_presented src="{{ site.url }}{{ '/assets/letter-m-16.png' | relative_url }}" alt="draft"> | _5_presented | Presented to FAE Course | The resolution has been presented, explained, and discussed with the whole course (on a Friday meeting). There are no major objections (otherwise the decision would go back to draft state).  | 



## Possible Status for "Team"

"Team" decisions have a simpler scheme, as no one outside the team needs to consent.

| Symbol | Keyword in Decision Log | Status | Explanation |
|-----|-----|-----|-----|
| <img class=_1_open src="{{ site.url }}{{ '/assets/letter-t-16.png' | relative_url }}" alt="open"> | _1_open | Open | An open decision has been created, but no resolution is available yet | 
| <img class=_2_draft src="{{ site.url }}{{ '/assets/letter-t-16.png' | relative_url }}" alt="draft"> | _2_draft | Draft | A resolution is available and documented, but there has not yet been a discussion in the team about it. | 
| <img class=_3_team_agreed src="{{ site.url }}{{ '/assets/letter-t-16.png' | relative_url }}" alt="draft"> | _3_team_agreed | Agreed in Team | The resolution has been discussed and agreed upon in the team. |