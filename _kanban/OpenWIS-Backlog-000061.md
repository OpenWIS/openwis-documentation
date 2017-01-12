---
layout: backlog
title: v4 - Fix v4.0 harvesting
kanCategory: design
kanSubCategory: pending
kanAssigned: UKMO
kanBacklog: 61
kanIssue:
kanPullReq:
kanFeature: Integrated catalogue
kanRelease: 4.2
kanMetric: 2
kanSize:
kanPriority: 1
kanRepo: OpenWIS/openwis4
kanProject:
---
Analyse, design, develop and implement solutions to current issues that v4.0 has with metadata harvesting and indexing scalability.

NM is documenting his performance investigations [here](https://github.com/NMichas/openwis-draft-analysis/wiki/Harvesting-performance-investigation)

### Scrum update 2016-10-11

Nassos has completed his investigation and shown evidence about where performance improvements could be made.  For OpenWIS v4, the suggested solution is to separate the http request from the indexing process so that each can be separately tuned for performance.  Nassos has also shown a PoC that demonstrates an asynchronous message based architecture that improves performance considerably; this would be a candidate architecture for v5.
