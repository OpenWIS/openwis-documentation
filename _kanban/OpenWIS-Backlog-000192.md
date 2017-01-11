---
layout: backlog
title: v3 - 3.14 Operational Deployment Packages
kanCategory: develop
kanSubCategory: in-progress
kanAssigned: DP
kanBacklog: 192
kanIssue:
kanPullReq:
kanFeature:
kanRelease: 3.14
kanMetric: 2
kanSize: 3
kanPriority: 3
kanRepo: OpenWIS/openwis
kanProject:
---

Ensure that stable 3.14 packages are available for maintenance activities, as configured in full operational deployment with all the supported middleware services (eg: OpenAM).

This requires:

1. Fixes to some shell scripts
2. Fixes to some pom files
3. Corrections/improvements to the installation manual
4. Confirmation that the package still also works with vagrant.

Packages should be available for both v 3.14.5 (currently operational at UKMO) and v 3.14.7 (currently operational at NWS).  This will require a point release v 3.14.5.1 and either a v 3.14.7.1 or a v 3.14.8 (TBD).
