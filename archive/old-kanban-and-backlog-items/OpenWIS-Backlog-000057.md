---
layout: backlog
title: v4 ACC - AAC3 New user with SAML Identity
kanCategory: test
kanSubCategory: pending
kanAssigned: UKMO
kanBacklog: 57
kanIssue:
kanPullReq: 35
kanFeature: Access
kanRelease: 4.0
kanMetric: 3.2
kanSize: 5
kanPriority: 2
kanRepo: OpenWIS/openwis4
kanProject:
---
Enhancement AAC3: New user with SAML Identity.

Update - GT email - 2017-02-28:
I just wanted to let you know that I merged a couple of PRs that allow OpenWIS4 to have proper SSO through OpenAM, using the email address as agreed.
I have also modified the "save user" and "update user" services to validate that the email provided doesn't already exist in the database (emails must be unique as discussed).

I just want to remind you that the user operations (add, update, delete) are not propagated from OpenWIS to OpenAM.
Modifications to one of them might require manual intervention to the other.

PRs #5, #35, #36

---


Update - scrum - 2016-11-17: GT - Not Tested in new v4.0 as part of Kanban 81. v4 - Refactoring to improve modularity.
Not tested in GeoCat version either.

GT will set up a SAML2 provider and test as a PoC (GeoCat were using Shibboleth).

---

This task was part of the OpenWISv4/GeoNetworksv3 [work package][WP] assigned to GeoCat in 2015.  The [documentation][doc] produced as part of that work describes the new functionality delivered.

[WP]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Workpackage.pdf
[doc]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Documentation.pdf

The outcome for this feature was:

2015 status: **MO/GeoCat Review**; Percent complete: **90**; Priority: Normal; Questions outstanding: nil;

Extra info: Blocked by Backlog 55.
