---
layout: backlog
title: v4 - Refactoring to improve modularity
kanCategory: develop
kanSubCategory: in-progress
kanAssigned: UKMO
kanBacklog: 81
kanIssue:
kanPullReq:
kanFeature: Quality software
kanRelease: 4.1
kanMetric: 1.2
kanSize: 13
kanPriority: 1
kanRepo:
kanProject:
---
Refactoring to improve the modularity of the system architecture. LM - Important but needs to be done with care to avoid a blowout of complexity. Est. just a guess as I'm not sure of the scope of this work.

PR - The initial scope should at least improve the way OpenWIS code interfaces with GeoNetwork code.

GT is documenting his investigation of the options [here](https://github.com/NMichas/openwis-draft-analysis/wiki/Enhancing-GeoNetwork-UI)

### Scrum update 2016-10-11

George has made a change to Angular JS that allows OpenWIS components to be integrated with GeoNetwork in a modular way, without now needing the addition of tags to the IDs in the GeoNetwork UI.  George will now go on to integrate the outstanding changes on the Kanban Board into GeoNetwork using this technique.
