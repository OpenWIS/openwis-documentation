---
layout: page
title: OpenWIS Technical Committee 2016 May
minuteOwner: technical
---
## 12th May 2016 - teleconference - meeting minutes
---
1. **Discuss the licensing issue of OpenDJ and its implication.**
	1. WQ - UKMO has raised a question about license for OpenAM/DJ and there has been an email exchange between Remy and others that I circulated earlier.  Are we OK?
	2. DW - That was from our internal accreditors and we have cleared it with them.
	3. MGo - Is there a wider question?  Since we are compiling on Cloudbees and redistributing, do we need to redistribute with a licence?
	4. RG - We provide scripts to generate the RPMs; we shouldn't distribute the RPMs.
	5. MGo - that adds an hour to the build.
	6. RG - OK, let's ask Michael Robbins for legal advice.
	7. ACT-OWIS-TC-2016-38: PR - Ask Michael Robbins for legal advice. OWIS-ACT
	8. RG - We have a small password issue with the current script, so we have asked for an update; but we will send the current script to MG.
	9. LM - could we raise a pull request for the script?
	10. ACT-OWIS-TC-2016-39: MG - Raise a pull request for the script. OWIS-ACT
2. **Review the progress of the development works since last meeting.**
	1. **Release of 3.14.5**
		1. MGo - Version 3.14.5 was released in April, a week after the last TC.  There was an issue with a missing dependency file, but that was sorted once it got added to Cloudbees.
		2. WQ - So, will there be further 3.14.x releases?
		3. MGo - MGi has been working on the downgraded Java JDK 7.19 issue and it looks like it can be resolved by updating the libraries on the portal; it's a work in progress.  This makes it possible to do a yum install.  The changes still need to be merged.
		4. MGi - there is a question about whether to use maven or integrate it directly.
		5. PN - So, are we planning a 3.14.6 release for this?  Also, what about the XSS fixes that LM provided?
		6. MGo - I think there is about 1 to 2 weeks work left on the Java issue.
		7. MGi - I agree, to have it done the correct way and properly tested would be 1 to 2 weeks or more.
		8. WQ - So, there could be a 3.14.6 and a 3.14.7?
		9. LM - the XSS fixes are already merged into Dev, so they are ready for 3.14.6.  The decision is: do we release 3.14.6 with the XSS fixes and then 3.14.7 with the Java JDK/fedlets resolution; OR, do we wait and release them both together in 3.14.6.
		10. RG - they are 2 different issues.
		11. PR - in principle, we should get a patch release out for fixes that are available, so that the community can choose whether to take them based on their local priorities, especially if the time to fix everything is uncertain.
		12. WQ - Ok, so we will release 3.14.6 with the XSS fixed and release 3.14.7 with the fedlet fixes later.
	2. **Status of GeoNetwork integration.**
		1. PR - So, at UKMO, we had GeoCat, the main supporters of GeoNetwork, do a whole bunch of work to adapt GeoNetwork 3 and OpenWIS to each other, under the OpenWIS 4 banner.  Some changes were made to GeoNetwork 3 as contributions to their trunk, while the OpenWIS specific requirements were changed in the OpenWIS code.  GeoCat did a lot of good stuff - they worked in an interactive agile way so we got to tailor things as they went along.  So, we're pretty happy with what they gave us.
		2. PR - Unfortunately, when it came to testing it all together, we couldn't get the harvesting to work.  This wasn't a feature we had been working on, so it took us a while to figure out that there was a fundamental problem with GeoNetwork 3 that couldn't be fixed by tinkering.  We have a theory that the Lucene indexing can't scale to the level required during bulk harvesting, at least as currently implemented; we even have an idea for a solution: implement Solr indexing for GeoNetwork.  But, we need to do more investigation before we choose a way forward and that is what we are intending to do, as soon as we get 3.14 into operations.
		3. RG - Can we make it available now so that we can begin our onboarding?
		4. MGo - I'm not sure it's fit for release in the current state.
		5. DW - OK, but we do need people to look at it and come up with more requirements.
		6. RG - I agree, we want to see what is missing - with the caveat that it is just for a look.
		7. ACT-OWIS-TC-2016-40: MG - Ask the CM Team to open up OpenWIS 4.x so everyone else can take a look. OWIS-ACT
		8. PN - Do we have docs on how to run it etc?
		9. MGo - Needs some work to build the environments; there is something already up on AWS, the only problem with it is the harvesting.
		10. LM - I volunteer to take a look at 4.x.
		11. MGo - There's not a lot of work, maybe a week.
		12. RG - Could we use the cloud servers set up by MF, where it could be a semi-permanent installation and everyone can have a look?
		13. DW - Can we push data to that?
		14. RG - Yes, absolutely.
		15. ACT-OWIS-TC-2016-41: RG - Give MGo/LM access to the MF cloud servers. OWIS-ACT
		16. ACT-OWIS-TC-2016-42: MGo/LM Set up OpenWIS v4 on the MF cloud servers, by the next TC if possible. OWIS-ACT
3. **How everyone set up their development environment (feedback need to assess if anything further need to be done to on-boarding developers).**
	1. OL - we're currently working through the set up of SSO.  We're using the MF scripts and the MGo instructions; some initial hurdles, but we're getting there.
4. **Review the status of Action items from last meeting.**
	1. Remy will share instructions for automatically installing OpenDJ in private network
		1. RG - Done.
	2. Product list of the task in GitHub + list from the TC F2F in Seoul (Leon)
		1. LM - WQ circulated the spreadsheet for comment.
		2. PR - So the OpenWIS v3 issues will remain as issues in GitHub, while the OpenWIS v4 items will be transferred into a Kanban backlog; LM/PR are currently working on that.
	3. Development environment doco (Leon)
		1. LM - the document is available on the GitHub wiki - anyone who wants to view/comment should get the url form LM.
	4. Developer Conference in September(?). Steve to confirm whether US NWS can host of the conference. 
		1. PG/KS - we're working on it - expect an announcement in about a week.

---

#### Participants:
- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM], TC Chair
- LM - Leon Mika, Bureau of Meteorology, Australia [BoM]
- OL - Okki Lee, Korea Meteorological Administration, Republic of Korea [KMA]
- RG - Remy Giraud, Meteo France, France [MF]
- YG - Yves Goupil, Meteo France, France [MF]
- DJ - Duncan Jeffery, Met Office, UK [UKMO]
- DW - Dominic Woollatt, Met Office, UK [UKMO]
- PN - Paul Nelson, Met Office, UK [UKMO]
- PR - Paul Rogers, Met Office, UK [UKMO]
- MGo - Martin Gollogly, SCISYS, UK [UKMO]
- SO - Steve Olson, National Weather Service, USA [NWS]
- PG - Patrick Gillis, National Weather Service, USA [NWS]
- KS - Kari Sheets, National Weather Service, USA [NWS]
- MGi - Marc Giannoni, National Weather Service, USA [NWS]
