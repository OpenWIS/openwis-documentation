---
layout: backlog
title: v4 ACC - AAC1 SAML2 authentication
kanCategory: test
kanSubCategory: pending
kanAssigned: UKMO
kanBacklog: 55
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
Enhancement AAC1: SAML2 authentication.

Update - GT email - 2017-02-28:
I just wanted to let you know that I merged a couple of PRs that allow OpenWIS4 to have proper SSO through OpenAM, using the email address as agreed.
I have also modified the "save user" and "update user" services to validate that the email provided doesn't already exist in the database (emails must be unique as discussed).

I just want to remind you that the user operations (add, update, delete) are not propagated from OpenWIS to OpenAM.
Modifications to one of them might require manual intervention to the other.

PRs #5, #35, #36

---

Update - scrum - 2017-01-17: GT has set up the direct Spring to OpenAM config and is currently debugging.

This is related to Kanban item 62 - Delegation of management of Users and Groups to GeoNetwork, in that these are alternatives.  Some organisations will want SSO whereas some will want a local OpenWIS authN and authZ.  Once they have decided on a method then they will likely stick with it.

---

Update - scrum - 2017-01-10: GT will set up a SAML2 provider PoC using a direct Spring to OpenAM set up (we currently have no interest in using CAS or Shibboleth).

---

Update - scrum - 2016-11-17: GT - Not Tested in new v4.0 as part of Kanban 81. v4 - Refactoring to improve modularity.
Not tested in GeoCat version either.

GT will set up a SAML2 provider and test as a PoC (GeoCat were using Shibboleth).

---

This task was part of the OpenWISv4/GeoNetworksv3 [work package][WP] assigned to GeoCat in 2015.  The [documentation][doc] produced as part of that work describes the new functionality delivered.

[WP]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Workpackage.pdf
[doc]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Documentation.pdf

The outcome for this feature was:

2015 status: **MO/GeoCat Review**; Percent complete: **90**; Priority: Normal; Questions outstanding: Looks like this is available by a config change - but how far did we go with AAC1/2/3?;

Extra info: Blocks Backlog 56 and Backlog 57.

Q: About the SAML authentication: is it a lazy session creation or is it a forced authentication endpoint? This means: are we going to display the portal to non-logged users or SAML will force authentication every time a user tries to reach the portal?

A: We need to be able to support Guest (non-authenticated) users.

Q: On AAC2 we will link existing users with users coming from SAML. How do we link both? By username or by some other complex operation?

A: I envisaged using the SAML2 Identity provided by the SAML IdP? Please advise what you consider to be most appropriate. In hindsight, I can see that it may not be feasible to assign existing to GeoNetwork users to a SAML2 Identity if it requires the username to be identical in both GeoNetwork and SAML IdP. Requirement AAC3 (creation of new users using a SAML2 Identity) will be the primary mechanism used. AAC2 is included for completeness (there may be occasion where we want to migrate users to different authentication - but these would be very rare). Please advise if AAC2 significantly increases implementation complexity. If this is the case, then AAC2 would be deferred.

Q: On AAC2 you also talk about an LDAP: is it a read only LDAP? Privileges and group association will be stored on LDAP or only user profile attributes like email?

A: The LDAP referenced in requirement AAC2 relates to one of the standard authentication mechanisms already implemented in GeoNetwork. From reading the user and administration guides, I inferred that GeoNetwork can delegate authentication to an LDAP server - and in such cases, user attributes may be provided by that server. In contrast, the case of the proposed SAML2 authentication, the SAML IdP does not provide any user attributes (only the identity). Given the response to the previous question, wherein I stated that the migration of existing users from one authentication mechanism to another is likely to be a very rare occurrence, if requirement AAC2 adds significant implementation complexity because of the constraints of needing to migrate user information (etc.), we may simply choose to defer requirement AAC2.
