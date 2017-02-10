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

Update - scrum - 2017-01-17:

- DP is making good progress with 3.14.7.1 but is expecting to hit the same issues with the final integration of OpenAM that he hit with 3.14.6; this time he will work to fix them.
- DP will continue work with the 3.14.5.1 deployment once LM publishes the virtual box he has been using.

---

Ensure that stable 3.14 packages are available for maintenance activities, as configured in full operational deployment with all the supported middleware services (eg: OpenAM).

This requires:

1. Fixes to some shell scripts
2. Fixes to some pom files
3. Corrections/improvements to the installation manual
4. Confirmation that the package still also works with vagrant.

Packages should be available for both v 3.14.5 (currently operational at UKMO) and v 3.14.7 (currently operational at NWS).  This will require a point release v 3.14.5.1 and, because some artefacts are no-longer available from the Forgerock repo, a v 3.14.7.1.
