---
layout: backlog
title: v4 - DDS3 Ad-hoc request for delivery
kanCategory: analyse
kanSubCategory: pending
kanAssigned: UKMO
kanBacklog: 50
kanIssue:
kanPullReq:
kanFeature: Integrated catalogue
kanRelease: 4.0
kanMetric: 5.2
kanSize: 3
kanPriority: 4
kanRepo: OpenWIS/openwis4
kanProject:
---
Enhancement DDS3: Ad-hoc request for delivery.

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

GeoNetwork shall be amended such that a user with the appropriate permissions may request the immediate delivery of data product instances that are currently available from the OpenWIS Data Service; so-called 'ad-hoc' delivery.

The portal will provide a web-based user interface enabling a user to configure their ad-hoc request for the specified dataset; allowing them to specify details of their chosen dissemination channel, how individual data product instances are packaged for delivery and which specific data product instances are required. On completion of the ad-hoc request details, the portal will package the user supplied information and the relevant product metadata record (retrieved via the ProductMetadataService SOAP web-service) into an ad-hoc request object and send it for validation and processing to the OpenWIS Data Service using the createRequest operation from the RequestService SOAP web-service.

_OpenWIS shall notify the relevant Groups that the dataset has been downloaded according to the notify permission defined for the metadata record associated with the dataset that has been requested._
