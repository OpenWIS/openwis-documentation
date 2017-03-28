---
layout: backlog
title: v4 RET - DDS1 Download offer
kanCategory: analyse
kanSubCategory: in-progress
kanAssigned: UKMO
kanBacklog: 77
kanIssue:
kanPullReq:
kanFeature: Retrieval
kanRelease: 4.0
kanMetric: 5.2
kanSize: 3
kanPriority: 4
kanRepo: OpenWIS/openwis4
kanProject:
---
Enhancement DDS1: Download offer.

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

GeoNetwork shall be amended such that, when the conditions outlined below are met, a user is presented with the opportunity to download or subscribe to the dataset described by the metadata record they are viewing.

The user may subscribe to the dataset under the following conditions:

1. The user has the necessary download permissions for the dataset
2. The dataset is managed by the OpenWIS Data Service (either cache or a local data service)- as determined via attributes from the summary record within the Product Metadata Table1.

A 'subscribe' option shall be provided by the portal enabling a new subscription to be requested (see enhancement DDS2 below).

Furthermore, the user may download or request immediate delivery of the dataset if the following conditions are also met:

3. The user is not blacklisted 2(e.g. they have not already exceeded their daily download threshold)
4. Data product instances are currently available3.

Options 'deliver' (see enhancement DDS3 below) and 'download' (see enhancement DDS4 below) shall be provided by the portal.
