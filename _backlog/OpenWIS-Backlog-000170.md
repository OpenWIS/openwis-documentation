---
layout: backlog
title: GeoNetwork Security Requirements
kanCategory: backlog
kanSubCategory:
kanAssigned:
kanBacklog: 170
kanIssue:
kanPullReq:
kanFeature: Security
kanRelease: 4.2
kanMetric:
kanSize:
kanPriority: 6
kanRepo: OpenWIS/openwis
---

### Discussion at Dev Con 2016 Hackathon

DW, SO, LM, MC, PR

How does GN3 match up to the WIS Reqs?

WIS Tech Specs:

- [?] 6 Authentication of a user
- [x] 7 Authorisation of a user role - check
- [x] 4 Maintenance of user identification and role identification
- [ ] 5 Consolidated view of distributed ID and role info. **DW - Really?  Share user data between WIS centres?**

- 6 GN v3
  1. Managed by GN
  2. Others
    - LDAP
    - CAS
    - Shibboleth
  3. SOAP
- 7 Has concept of users, groups and roles (admin, user, editor, user-admin, content reviewer)

DW - v3 has 2 groups:
  - Public
  - Institutional
Would prefer more groups.

LM - discussed 3rd group - DCPC user.



LM - in v3.14 data policies control access to subscriptions/data - need this in v4.  Data policies are stored in the database.  Groups are stored in sec service.

![Whiteboard photo 1]({{ site.baseurl | prepend: site.url }}/assets/GeoNetwork-Sec-Reqs.JPG)
