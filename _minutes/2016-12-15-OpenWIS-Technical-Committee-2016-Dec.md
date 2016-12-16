---
layout: page
title: OpenWIS Technical Committee 2016 December
---

#### 15th December 2016 - WebEx - meeting minutes

---

1. **Status of the current development (e.g integration of OpenWIS UI with GeoNetwork, new build with Maven 3 etc)**
	0. Presentation by George: [Fork based to Overlay based](https://github.com/OpenWIS/openwis4/wiki/Fork-based%20To%20Overlay-based)
	1. RG - Does this plug-in architecture allow you to change the UI?
	2. GT - Yes, it is easy to plug-in to the UI.
	3. NM - Core GeoNetwork is not designed to be pluggable, so there is not just one simple way to plug-in, you have to plug-in in a few different ways.  We will provide simple examples of how to use each method, such as: how to add a new button.
	4. NM - Core GeoNetwork is currently on version 3.2.0; if they ship version 3.2.1 tomorrow, we just change a single line in OpenWIS 4 to reference the new GeoNetwork 3.2.1 and we can ship it with GeoNetwork version 3.2.1.
	5. GT - If the GeoNetwork architecture changes in a big way, then it would be a lot of effort on our part, but this way we are as independent as we can be.  Also, if people are already using Core GeoNetwork then they could easily use an OpenWIS plug-in; they don't have to take the whole of OpenWIS.
	6. NM - We will work with developers on small changes to show how the new plug-in architecture is used.
	7. WQ - We are ok with this approach, we have talked about plug and play since the meeting in Melbourne.
	8. WQ - Is plugging OpenWIS into GeoNetwork different to plugging GeoNetwork into OpenWIS?
	9. GT - We plug OpenWIS into GeoNetwork because there are a lot of good features in GeoNetwork we want.  We can add our own features and also remove features.
	10. WQ - How does the plug-in approach work technically?
	11. GT - We take the core GeoNetwork files and we add Javascript that injects our code into the GeoNetwork application.
	12. PR - The [technical details](https://github.com/OpenWIS/openwis4/wiki/Developing-OpenWIS-v4-functionality) are documented on the wiki.
	13. WQ - What about something like the Security Services, which are complicated?  Does core GeoNetwork have its own authorization and authentication?
	14. NM - We are currently working with the Spring based security scheme used in GeoNetwork and establishing a SAML2 link.  We will be able to choose to use the built-in GeoNetwork security or our own external provider.
	15. GT - I am currently working on integrating [CAS](https://en.wikipedia.org/wiki/Central_Authentication_Service). If it works with core GeoNetwork we will not need to modify OpenAM.
	16. NM - So the question will be whether we use the core GeoNetwork internal security or OpenAM etc.
	17. DW - So each organisation should investigate these options and choose which one suits them.
	18. GT - And if CAS works, we will not be required to change this aspect of core GeoNetwork, but we could choose to.
	19. RG - The architecture looks fine, but do we need something to be changed on core GeoNetwork to do our plug-ins?
	20. NM - No.  We have already done the integration to core GeoNetwork v 3.2.0.
	21. GT - And when the next stable release comes out, v3.4.0 say, we will move our plug-ins to that version.
	22. RG - Do we depend on them to provide the integration points?
	23. NM - No, we identify the points where we want to inject our code.  Only if they make a major change would we need to update our injection logic.
	24. WQ - So we already have a version to play with?
	25. NM - Yes.
	26. WQ - So in this version, are we using our method of downloading metadata or the default core GeoNetwork method?
	27. GT - We are using our subscription method, but we could choose to use either.
	28. NM - We want to test it and decide which methods to choose.
	29. GT - [This version](https://github.com/OpenWIS/openwis4/tree/develop) is available on GitHub.
	30. NM - We are preparing 2 VMs for you to play with:
		- A vanilla core GeoNetwork v 3.2.0
		- A plug-in integration of OpenWIS4 and core GeoNetwork v 3.2.0.

	31. NM - I will send the links out on the TC mail list and then you can compare them.
	32. WQ - Ok, so everyone should have a play around.
	33. OL - We seem to have two parallel lines of development on v3 and v4.  Will we be integrating 3.14.7 functions, for example Data Services, into OpenWIS v4?
	34. NM - We have already.  We took everything from OpenWIS v3: Data Services, JBOSS, etc.  We only changed the UI, so OpenWIS v4 is using the 3.14.7 code.  And if someone, say, fixes a bug in 3.14, we will move that to OpenWIS v4 as well.
	35. WQ - 3.14 is the current operational version but we will only do maintenance changes to it from now on.
	36. OL - We should be able to run the OpenWISv4 in a Vagrant environment.
	37. GT - There is already an all-in-one Vagrant package on GitHub that you can try out.
	38. NM - We also plan to provide a multi-box Vagrant package too.
	39. PR - So, we need feedback.
	40. DW - Yes, feedback on which parts of GeoNetwork we should keep, there are some new features, and which parts to we should overlay with our plug-ins.
	41. PR - We should aim to have collected this information in time for discussion at the Toulouse meeting.
	42. WQ - Two VMs?  Will we be able to see them side by side?
	43. NM - Yes, the VMs will be on the internet so you will be able to access both at the same time and directly compare core GeoNetwork versus OpenWIS4.
	44. WQ - Ok, we look forward to you publishing the URLs.
	45. PR - We should take this opportunity to make further improvements to our development process.  We have been improving our collaboration, but we mostly tend to take tasks away and work on them within each of our organisations.  As we work on features for OpenWIS4 together, we could collaborate even more closely and more directly share the work on each feature by having developers from more than one organisation working on each feature.  This will help us share the knowledge about how to apply the plug-in approach effectively.  I am working up a proposal for how this could work that I will share for discussion by the end of January.
	46. ACT-OWIS-TC-2016-58:Action: PR - Share proposal on development process improvements by end of January. OWIS-ACT
	47. OL - It is ok to look at GeoNetwork and new requirements, but remember that OpenWIS is based on WMO requirements.
	48. PR - Yes it is and I am taking that into account, I'm calling that aspect WIS 1.0 compliance, because now we have emerging WIS 2.0 requirements moving onto the agenda.  I propose that we further develop our automated testing to make sure we can always verify and demonstrate that OpenWIS remains compliant, as well as test new requirements are ready for acceptance.

2. **Development tasks (backlogs) and who can do what**

	1. WQ - I guess we have just talked about what we should do next.
	2. PR - Yes, so if everyone could review OpenWIS v4.0 and provide the feedback as GitHub Issues within the OpenWIS4 repository, that would be good.
	3. WQ - Ok, so that's an action on everybody, say by the beginning of February.
	4. ACT-OWIS-TC-2016-59:Action: All - review OpenWIS v4.0 and provide the feedback as GitHub Issues within the OpenWIS4 repository. OWIS-ACT
	5. ACT-OWIS-TC-2016-60:Action: PR - Add a Kanban task for this review. OWIS-ACT

3. **AOB**

	1. OL - I am getting a build failure with 3.14.7 on the new version of Ubuntu; a new Vagrant issue.  I havne't raised a GitHub issue for it yet, it may just be my environment.
	2. SO - What are the dates for the March meeting in Toulouse?
	3. WQ - Week beginning 20th March.
	4. SO - Ah, so that clashes with the OGC TC in Delft.
	5. WQ - Ok, raise it with Remy Giraud.
	6. SO - Ok.

4. **Date of next meeting**

	1. WQ - So I will call the next TC meeting for early February 2017.

---

#### Participants

- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM], Chair
- LM - Leon Mika, Bureau of Meteorology, Australia [BoM]
- YW - Yang Wang, Bureau of Meteorology, Australia [BoM]
- OL - Okki Lee, Korea Meteorological Administration, Republic of Korea [KMA]
- HL - Hyekyoung Lee, Korea Meteorological Administration, Republic of Korea [KMA]
- SD - Sungsoo Do, Korea Meteorological Administration, Republic of Korea [KMA]
- MC - Michael Claudon, Meteo France, France [MF]
- RG - Remy Gibault, Meteo France International, France [MFI]
- SO - Steve Olson, National Weather Service, USA [NWS], Vice-Chair
- MG - Marc Giannoni, National Weather Service, USA [NWS]
- DJ - Duncan Jeffrey, Met Office, UK [UKMO]
- DW - Dominic Woollatt, Met Office, UK [UKMO]
- JO - Julie Oakley, Met Office, UK [UKMO]
- PR - Paul Rogers, Met Office, UK [UKMO]
- NM - Nassos Michas, European Dynamics, Greece [UKMO]
- GT - Giorgos Tryantafyllidis, European Dynamics, Greece [UKMO]
- DP - Dimitris Papadeas, European Dynamics, Greece [UKMO]
