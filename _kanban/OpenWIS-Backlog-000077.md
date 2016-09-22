---
layout: backlog
title: DDS1 Download offer
kanCategory: analyse
kanSubCategory: pending
kanAssigned: UKMO
kanBacklog: 77
kanIssue:
kanPullReq:
kanFeature: Integrated catalogue
kanRelease: 4.2
kanMetric: 5.2
kanSize: 3
kanPriority: 4
kanRepo:
kanProject:
---
Enhancement DDS1: Download offer

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
