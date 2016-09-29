---
layout: backlog
title: ADMIN1 Blacklisting
kanCategory: analyse
kanSubCategory: pending
kanAssigned: UKMO
kanBacklog: 41
kanIssue:
kanPullReq:
kanFeature: Integrated catologue
kanRelease: 4.2
kanMetric: 2.1
kanSize: 3
kanPriority: 3
kanRepo:
kanProject:
---
Enhancement ADMIN1: Blacklisting

This task was part of the OpenWISv4/GeoNetworksv3 [work package][WP] assigned to GeoCat in 2015.  The [documentation][doc] produced as part of that work describes the new functionality delivered.

[WP]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Workpackage.pdf
[doc]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Documentation.pdf

The outcome for this feature was:

2015 status: **MO/GeoCat Review**; Percent complete: **90**; Priority: Normal; Questions outstanding: 100% or 90% Done? Pagination?;

Extra info:

A black-listed user is able to browse the catalogue but is not able to download data from OpenWIS nor are their subscriptions fulfilled. Black-listing occurs when a user's data download thresholds have been exceeded within a given period (e.g. 24-hours), or when an administrator deems that a given user has breached the fair-usage policy. A second threshold is defined for each user that is used to trigger delivery of warning to that user indicating their imminent breach of the data download threshold.

GeoNetwork shall be amended to provide a User Administrator with a web-based mechanism to:

  1. blacklist a specific user;
  2. blacklist all users within a specific Group;
  3. revoke blacklisting for a specific user;
  4. revoke blacklisting for all users within a specific Group;
  5. amend the download thresholds for a specific user or for all users within a specific Group; and
  6. review blacklist thresholds and download volumes for the current period for all users or for all users within a specific Group.

The BlacklistService SOAP web-service provides for retrieval and persistence of black-list information.
