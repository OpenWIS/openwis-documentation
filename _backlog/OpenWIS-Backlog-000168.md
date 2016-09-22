---
layout: backlog
title: OpenWIS User Rights
kanCategory: backlog
kanSubCategory:
kanAssigned:
kanBacklog: 168
kanIssue: 
kanPullReq:
kanFeature: Security
kanRelease: 4.1
kanMetric: 4.2
kanSize:
kanPriority: 3
kanRepo: OpenWIS/openwis
---
OpenWIS 3.14 suffered a bug which allowed users to change properties of other users.

Task #48:

    > [HIGH] ensure that a user can only update their own user profile (administration caveats apply); URL hacking enables a user to modify the profile of another user. Comes with GeoNetwork trunk; UKMO to verify

Confirm that this is not ocurring in OpenWIS 4 (i.e. GeoNetworks 3).