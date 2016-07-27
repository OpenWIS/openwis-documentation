---
layout: page
title: OpenWIS Technical Committee Apr 2016
---
## 14th April 2016 - teleconference - meeting minutes
---
1. Review the progress of the uplift and other development works since the Seoul meeting. Release of 3.14.4.
	1. PN - OpenWIS version 3.14.5 is in test. Security testing has revealed a few XSS vulnerabilities. There will have to be a few code changes to fix these.
	2. PN - Puppet scripting is underway on Dev.  We haven't started yet on Test or Production.
	3. PN - The Java version on the OpenAM stack is stuck on 7.0.19.
	4. MGi - We are currently looking into this with OpenAM 12.03 r5.  Should we start a new branch?
	5. LM - Yes.
	6. MGi - The OpenAM scripts built ok.  We need to change the portal code to use the new API. We are also wondering if there have been any schema changes.
	7. A-OWIS-TC-2016-31: PN - ask the UKMO OpenAM team if there are any schema changes to worry about. OWIS-A
	8. RG - We split the RPM build and the configuration into two parts.  The RPM build is complete and is in GitHub; we are still working on the configuration. Yves has tested one configuration but there are more to do before we release it.
	9. A-OWIS-TC-2016-32: RG - Put the configuration script onto GitHub. OWIS-A
	10. RG - Will we be keeping Java version 7.0.19 for OpenWIS v 3.14?
	11. PN - We need to make the portals patchable.
	12. RG - But in v 3.14 or v 3.15; are we changing our earlier decision to use Java 7.0.19?
	13. MGi - We will continue to work on this issue and aim to release a 3.14.6 patch.
	14. WQ - _Ok, so we are agreed, we will release v 3.14.5 with Java 7.0.19 and patch it in a later release._
2. Start to plan the work on v4 (review backlog, assign task).
	1. LM - I've looked at the outstanding issues in GitHub and they roughly fall into those that relate to the portals and those that relate to other components.  Given that we are upgrading GeoNetwork, I propose that we defer portal issues until afterwards.  In the meantime, we could look at issues with the Data Service; there are about 12 of those.
	2. PR - We have a lot of the changes for v 4 ready, but we need to sort out the issue with harvesting to be able to test it properly.  We hope to do that in June.
	3. A-OWIS-TC-2016-33: LM/PR - draft a backlog for the next TC. OWIS-A
	4. LM - I would like to know who will be available to do development work and who needs help with the development environment.
	5. PG - We're still not fully onboard.  We would like to host the Developer Conference this summer and we would appreciate some support in that.
	6. LM - Ok, I can help with that.
	7. A-OWIS-TC-2016-34: LM - Provide some developer docs on how to set up the development environment using a combination of vagrant and puppet. OWIS-A
	8. PN - What about Docker?
	9. PR - There is currently more interest in _puppet_ among the association.
	10. OL - We tried vagrant and created 3 VMs; we could display the main screen of OpenWIS.  However, we still have some issues with OpenAM.  We would like some documented process to make it work with our SSO machine.
	11. LM - The original vagrant design ignored SSO to keep it simple.  I haven't looked at the MF scripts yet, but if that looks viable I'll put something into the docs.
	12. OL - Automated would be great but even a manual process would be good.
	13. RG - We are working on an auto install.  We found a solution for OpenAM to work with a private IP address.  We will do some docs and can give you access to the set up in the cloud. When you run in a vagrant environment, there is a trick to make it work.
	14. OL - Good, then we'll have something working in the development environment.
	15. MGo - So is the OpenAM now automated?
	16. RG - Yes it is.
	17. MGi - We opened an issue on GitHub where we suggested an outline for the doc set.
	18. LM - Yes, that's Issue #41 under the openwis/deploy repo; we can base the documentation on that.
3. The choice of the target week (and location?) of the OpenWIS Developer conference.
	1. PG - NWS are intending to host the Dev Con this year, but we still need to confirm that and the date.  Steve Olson is leading on that.
	2. RG - Can we target a date?
	3. MGi - We are aiming for the summer but will need to get back with the options.
	4. WQ - September might be the best time for most of us.
	5. RG - Yes, July and August are holiday periods in Europe, so September would be better.
	6. MGi - Understood.
4. Other business
	1. WQ - The date of the next meeting will be 12th May 2016.

---

#### Participants
- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM], TC Chair
- LM - Leon Mika, Bureau of Meteorology, Australia [BoM]
- OL - Okki Lee, Korea Meteorological Administration, Republic of Korea [KMA]
- RG - Remy Giraud, Meteo France, France [MF]
- PN - Paul Nelson, Met Office, UK [UKMO]
- PR - Paul Rogers, Met Office, UK [UKMO]
- MGo - Martin Gollogly, SCISYS, UK [UKMO]
- PG - Patrick Gillis, National Weather Service, USA [NWS]
- MGi - Marc Giannoni, National Weather Service, USA [NWS]
