---
layout: backlog
title: ADMIN6 Browse subscriptions
kanCategory: develop
kanSubCategory: in-progress
kanAssigned: UKMO
kanBacklog: 49
kanIssue:
kanPullReq:
kanFeature: Integrated catologue
kanRelease: 4.1
kanMetric: 5.2
kanSize: 3
kanPriority: 3
kanRepo:
---
Enhancement ADMIN6: Browse subscriptions

This task was part of the OpenWISv4/GeoNetworksv3 [work package][WP] assigned to GeoCat in 2015.  The [documentation][doc] produced as part of that work describes the new functionality delivered.

[WP]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Workpackage.pdf
[doc]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Documentation.pdf

The outcome for this feature was:

2015 status: **MO/GeoCat Review**; Percent complete: **80**; Priority: Normal; Questions outstanding: Is this 100% Done or 80% Done? No bulk edit actions?;

Extra info:

GeoNetwork shall be amended to provide a User Administrator with a web-based mechanism to:

  1. browse the subscriptions for all users or users within a specific Group; and
  2. suspend and reactivate specific subscriptions.

The SubscriptionService SOAP web-service provides for retrieval and persistence of the subscription objects.
