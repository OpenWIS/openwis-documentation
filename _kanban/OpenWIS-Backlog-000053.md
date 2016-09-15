---
layout: backlog
title: DDS2 New subscription
kanCategory: analyse
kanSubCategory: pending
kanAssigned: UKMO
kanBacklog: 53
kanIssue:
kanPullReq:
kanFeature: Subscriptions
kanRelease: 4.1
kanMetric: 5.2
kanSize: 3
kanPriority: 4
kanRepo:
---
Enhancement DDS2: New subscription

This task was part of the OpenWISv4/GeoNetworksv3 [work package][WP] assigned to GeoCat in 2015.  The [documentation][doc] produced as part of that work describes the new functionality delivered.

[WP]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Workpackage.pdf
[doc]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Documentation.pdf

The outcome for this feature was:

2015 status: **MO Test**; Percent complete: **100**; Priority: Normal; Questions outstanding: nil;

Extra info:

GeoNetwork shall be amended such that a user with the appropriate permissions may set up a new subscription requesting routine delivery of data products from the OpenWIS Data Service.

The portal will provide a web-based user interface enabling a user to set up their subscription1; allowing them to specify details of their primary and secondary dissemination channels and how individual data product instances are packaged for delivery. On completion of the subscription details, the portal will package the user supplied information and the relevant product metadata record (retrieved via the ProductMetadataService SOAP web-service) into a subscription request object and send it for validation and processing to the OpenWIS Data Service using the createSubscription operation from the SubscriptionService SOAP web-service.

OpenWIS shall notify the relevant Groups that a new subscription has been created according to the notify permission defined for the metadata record associated with the dataset that has been subscribed to.
