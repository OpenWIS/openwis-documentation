---
layout: backlog
title: v4 - MM3 Metadata categories and category-based harvesting
kanCategory: develop
kanSubCategory: in-progress
kanAssigned: UKMO
kanBacklog: 46
kanIssue:
kanPullReq:
kanFeature: Integrated catalogue
kanRelease: 4.0
kanMetric: 2.1
kanSize: 3
kanPriority: 3
kanRepo: OpenWIS/openwis4
kanProject:
---
Enhancement MM3: Metadata categories and category-based harvesting.

Update - scrum - 2016-11-17: GT - Migrated into new v4.0 as part on Kanban 81. v4 - Refactoring to improve modularity.
Works in the GeoCat version but not in the GT version: Getting an error when setting category for a group.  GT working on it.

---

This task was part of the OpenWISv4/GeoNetworksv3 [work package][WP] assigned to GeoCat in 2015.  The [documentation][doc] produced as part of that work describes the new functionality delivered.

[WP]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Workpackage.pdf
[doc]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Documentation.pdf

The outcome for this feature was:

2015 status: **MO Test**; Percent complete: **100**; Priority: Normal; Questions outstanding: nil;

Extra info:

In order to provide greater control in the harvesting of metadata between WMO Information System Centres (WIS Centres), OpenWIS provides the facility to group metadata records into named subsets, or categories. Each category of metadata records can be offered for harvesting by a third party as a distinct subset of the total set of metadata records within the OpenWIS catalogue.

GeoNetwork shall be amended such that:

  1. A metadata record may be assigned to a category
  2. Metadata harvesting can be configured for each metadata category; e.g. specific metadata harvesting configurations can be specified for the categories of metadata, enabling OpenWIS to expose named subsets of metadata for harvesting by third parties.
  3. The GeoNetwork role **Administrator** can define new categories.
  4. The GeoNetwork role **Administrator** can modify category assignment of published metadata records1
  5. The GeoNetwork role **User Administrator** can assign the permission to use categories to specific Groups and define a default category for each Group.
  6. The GeoNetwork role **Editor** can assign a metadata record that they have permission to modify to a specific category.

Note that permissions are assumed to cascade in the order: Guest (non-authenticated user), Registered User, Editor, Content Reviewer, User Administrator and Administrator. For example, a user with role Content Reviewer can perform all the actions assigned to a user with role Editor plus a few more.
