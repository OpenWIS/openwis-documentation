---
layout: backlog
title: v4 - ADMIN2 Browse product metadata table
kanCategory: test
kanSubCategory: pending
kanAssigned: UKMO
kanBacklog: 42
kanIssue:
kanPullReq:
kanFeature: Integrated catalogue
kanRelease: 4.0
kanMetric: 2.1
kanSize: 3
kanPriority: 2
kanRepo: OpenWIS/openwis4
kanProject:
---
Enhancement ADMIN2: Browse product metadata table.

Update - scrum - 2016-11-17: GT - Migrated into new v4.0 as part of Kanban 81. v4 - Refactoring to improve modularity.

---

This task was part of the OpenWISv4/GeoNetworksv3 [work package][WP] assigned to GeoCat in 2015.  The [documentation][doc] produced as part of that work describes the new functionality delivered.

[WP]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Workpackage.pdf
[doc]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Documentation.pdf

The outcome for this feature was:

2015 status: **MO/GeoCat Review**; Percent complete: **70**; Priority: High; Questions outstanding: 100% or 70% Done?;

Extra info:

Geonetwork shall be amended to provide an Administrator with a web based mechanism to:

  1. browse the content of the product metadata table; and
  2. for specific records, override attributes (e.g. dissemination priority) that have been extracted from the associated metadata record in the catalogue.

The ProductMetadataService SOAP web-service provides a mechanism to interact with the product metadata table.
