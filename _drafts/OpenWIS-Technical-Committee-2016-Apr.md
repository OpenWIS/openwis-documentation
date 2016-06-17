---
layout: default
---
#### OpenWIS Technical Committee - meeting minutes
14th April 2016
###### Agenda
1.  Review the progress of the uplift and other development works since the Seoul meeting. Release of 3.14.4.
2.  Start to plan the work on v4 (review backlog, assign task).
3.  The choice of the target week (and location?) of the Openwis Dev conference.
4.  Other business.

##### 1.  Review the progress of the uplift and other development works since the Seoul meeting. Release of 3.14.4.
1. UKMO PN: OpenWIS version 3.14.5 is in test. Security testing has revealed a few XSS vulnerabilities. There will have to be a few code changes to fix these.
2. UKMO PN: Puppet scripting is underway on Dev.  We haven't started yet on Test or Production.
3. UKMO PN: The Java version on the OpenAM stack is stuck on 7.0.19.
4. NWS MG: We are currently looking into this with OpenAM 12.03 r5.  Should we start a new branch?
5. BoM LM: Yes.
6. NWS MG: The OpenAM scripts built ok.  We need to change the portal code to use the new API. We are also wondering if there have been any schema changes.
7. > A-OWIS-TC-2016-31 UKMO - PN: ask the UKMO OpenAM team if there are any schema changes to worry about.
8. MF RG: We split the RPM build and the configuration into two parts.  The RPM build is complete and is in GitHub; we are still working on the configuration. Yves has tested one configuration but there are more to do before we release it.
9. > A-OWIS-TC-2016-32 MF - RG: Put the configuration script onto GitHub.
10. MF RG: Will we be keeping Java version 7.0.19 for OpenWIS v 3.14?
11. UKMO - PN: We need to make the portals patchable.
12. MF RG: But in v 3.14 or v 3.15; are we changing our earlier decision to use Java 7.0.19?
13. NWS MG: We will continue to work on this issue and aim to release a 3.14.6 patch.
14. > BoM WQ: Ok, so we are agreed, we will release v 3.14.5 with Java 7.0.19 and patch it in a later release.

##### 2.  Start to plan the work on v4 (review backlog, assign task).
1. BoM LM: I've looked at the outstanding issues in GitHub and they roughly fall into those that relate to the portals and those that relate to other components.  Given that we are upgrading GeoNetwork, I propose that we defer portal issues until afterwards.  In the meantime, we could look at issues with the Data Service; there are about 12 of those.
2. We have a lot of the changes for v 4 ready, but we need to sort out the issue with harvesting to be able to test it probably.  We hope to do that in June.
3. > A-OWIS-TC-2016-33 BoM/UKMO - LM/PR: draft a backlog for the next TC.
4. BoM LM: I would like to know who will be available to do development work and who needs help with the development environment.
5. NWS PG: We're still not fully onboard.  We would like to host the Developer Conference this summer and we would appreciate some support in that.
6. BoM LM: Ok, I can help with that.
7. > A-OWIS-TC-2016-34 BoM LM: Provide some developer docs on how to set up the development environment using a combination of vagrant and puppet.
8. UKMO PN: What about Docker?
9. UKMO PR: There is currently more interest in puppet among the association.
10. KMA OL: We tried vagrant and created 3 VMs; we could display the main screen of OpenWIS.  However, we still have some issues with OpenAM.  We would like some documented process to make it work with our SSO machine.
11. BoM LM: The original vagrant design ignored SSO to keep it simple.  I haven't looked at the MF scripts yet, but if that looks viable I'll put something into the docs.
12. KMA OL: Automated would be great but even a manual process would be good.
13. MF RG: We are working on an auto install.  We found a solution for OpenAM to work with a private IP address.  We will do some docs and can give you access to the set up in the cloud. When you run in a vagrant environment, there is a trick to make it work.
14. KMA OL: Good, then we'll have something working in the development environment.
15. NWS MG: So is the OpenAM now automated?
16. MF RG: Yes it is.
17. NWS MG: We opened an issue on GitHub where we suggested an outline for the doc set.
18. BoM LM: Yes, that's Issue #41 under the openwis/deploy repo; we can base the documentation on that.

##### 3.  The choice of the target week (and location?) of the Openwis Dev conference.
1. NWS PG: NWS are intending to host the Dev Con this year, but we still need to confirm that and the date.  Steve Olson is leading on that.
2. MF RG: Can we target a date?
3. NWS MG: We are aiming for the summer but will need to get back with the options.
4. BoM WQ: September might be the best time for most of us.
5. MF RG: Yes, July and August are holiday periods in Europe, so September would be better.
6. NWS MG: Understood.

##### 4. Other business
1. BoM WQ: The date of the next meeting will be 12th May 2016.

###### Participants
- BoM WQ: Australian Bureau of Meteorology, Weiqing Qu  (chair)
- BoM LM: Australian Bureau of Meteorology, Leon Mika
- KMA OL: Korea Meteorological Administration, Okki Lee
- MF RG: Meteo-France, Remy Giraud
- NWS PG: US National Weather Service, Pat Gillis
- NWS MG: US National Weather Service, Marc Giannoni
- UKMO PN: UK Met Office, Paul Nelson
- UKMO PR: UK met Office, Paul Rogers
- UKMO MG: UK Met Office, Martin Gollogly
