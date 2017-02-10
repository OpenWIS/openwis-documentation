---
layout: backlog
title: v4 RET - UI1 Subscription management
kanCategory: test
kanSubCategory: pending
kanAssigned: UKMO
kanBacklog: 54
kanIssue:
kanPullReq:
kanFeature: Retrieval
kanRelease: 4.0
kanMetric: 5.2
kanSize: 3
kanPriority: 2
kanRepo: OpenWIS/openwis4
kanProject:
---
Enhancement UI1: Subscription management.

Update - scrum - 2016-11-17: GT - Migrated into new v4.0 as part of Kanban 81. v4 - Refactoring to improve modularity.

---

This task was part of the OpenWISv4/GeoNetworksv3 [work package][WP] assigned to GeoCat in 2015.  The [documentation][doc] produced as part of that work describes the new functionality delivered.

[WP]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Workpackage.pdf
[doc]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Documentation.pdf

The outcome for this feature was:

2015 status: **MO/GeoCat Review**; Percent complete: **100**; Priority: Normal; Questions outstanding: In the manual, does 'redirect the user to the Users and Groups section of the admin console' really mean that, or just that identical functionality exists in the User Portal and Admin Portal?;

Extra info:

GeoNetwork shall be amended to provide users with a web-based mechanism to review and manage (create, update and delete) their subscriptions for routine delivery of data.
The SubscriptionService SOAP web-service provides for retrieval and persistence of the subscription objects.
