---
layout: backlog
title: v4 - DDS2 New subscription
kanCategory: analyse
kanSubCategory: in-progress
kanAssigned: UKMO
kanBacklog: 53
kanIssue:
kanPullReq:
kanFeature: Subscriptions
kanRelease: 4.0
kanMetric: 5.2
kanSize: 3
kanPriority: 4
kanRepo: OpenWIS/openwis4
kanProject:
---
Enhancement DDS2: New subscription.

Update - scrum - 2017-01-17: LM and GT will investigate what metadata characteristics, or other system properties, need to be set to activate the data download features DDS1, DDS2, DDS3 and DDS4 (Kanban items 77, 53, 50 and 79 respectively).

---

Update - scrum - 2016-11-17: GT - Migrated into new v4.0 as part of Kanban 81. v4 - Refactoring to improve modularity.

The migrated version only shows the 'subscribe' action in the sample entries of the Search screen. It is possible that the metadata itself needs to have specific characteristics in order for the 'Deliver' and 'Download' actions to become available.  **Further investigation is required.**

Furthermore, it is very important to point out that GN v3.2.0 appears to feature its own download mechanism.  This shows a Download button in the UI but not in the same place as OpenWIS.  It is possible that OpenWIS would like to integrate this functionality into its own delivery methods.

---

This task was part of the OpenWISv4/GeoNetworksv3 [work package][WP] assigned to GeoCat in 2015.  The [documentation][doc] produced as part of that work describes the new functionality delivered.

[WP]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Workpackage.pdf
[doc]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Documentation.pdf

The outcome for this feature was:

2015 status: **MO Test**; Percent complete: **100**; Priority: Normal; Questions outstanding: nil;

Extra info:

GeoNetwork shall be amended such that a user with the appropriate permissions may set up a new subscription requesting routine delivery of data products from the OpenWIS Data Service.

The portal will provide a web-based user interface enabling a user to set up their subscription1; allowing them to specify details of their primary and secondary dissemination channels and how individual data product instances are packaged for delivery. On completion of the subscription details, the portal will package the user supplied information and the relevant product metadata record (retrieved via the ProductMetadataService SOAP web-service) into a subscription request object and send it for validation and processing to the OpenWIS Data Service using the createSubscription operation from the SubscriptionService SOAP web-service.

OpenWIS shall notify the relevant Groups that a new subscription has been created according to the notify permission defined for the metadata record associated with the dataset that has been subscribed to.
