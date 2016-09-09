---
layout: page
title: OpenWIS Technical Committee 2016 September
---

#### 8th September 2016 - teleconference - meeting minutes

---



1. **Status of preparation for Developers Workshop**
	1. SO - All attendees should have received an email requesting security details - please fax the response asap.
	2. SO - The agenda is on Google - let me know if you need permission to view it.
	3. SO - I have some additional questions, that I emailed ahead:
		1. There could be more than one hackathon activity running at a time, so do we need more than one cloud service?
		2. We will be able to access GitHub etc but not ssh - is that ok?
		3. Does anyone have a presentation they want to send ahead?
	4. DW - What access will we have to a version of GeoNetworks?
	5. PN - I thought we had installed GeoNetworks onto the Proxmox servers?
	6. LM - The portal is on Proxmox, so the core GeoNetwork is running there.
	7. ACT-OWIS-TC-2016-46: LM - Circulate the url of the portal on Proxmox. OWIS-ACT
	8. NM - We could provide access to a running GeoNetwork too, either set-up a server or run it on our PC.
	9. LM - We could have vagrant copies available.
	10. PN - So, we'll have Proxmox and vagrant on laptops.
	11. LM - Are there any presentations anyone would like done by someone else?  Someone mentioned the as-is architecture - I can do that.  The to-be architecture will come up in the subsequent discussion.
	12. PN - Will there be any facilities for remote participation?
	13. SO - We're planning on having Google Hangouts and WebEx, so anyone interested should send me their emails so I can make sure they get the event invites.
	14. WQ - Is there any update to the agenda circulated previously?
	15. SO - No, we're sticking to what we published. The timetable is a little aggressive, but we'll prioritise as we go.
	16. SO - By next week I hope to have the lunch options for day one on the web so you can choose options.  At the event we will choose lunch options a day ahead.
	17. OL - Are you happy that we have answered your original questions?
	18. SO - Yes, thanks.
2. **Status of OpenWIS development**
	1. LM - We are preparing for development of v4.  European Dynamics have started analysing UI changes and are looking at an approach that avoids too many modifications to the core Geonetwork code.  They are also looking at the integration between the components of OpenWIS and the search/index issue.
	2. NM - Yes, we are currently investigating the performance of the harvesting and should have a report within a few days.  The approach we are working on for the UI would enable us to develop OpenWIS as components that plug-in to GeoNetworks.
	3. PN - Are there a lot of work-packages coming for the Data Service?
	4. LM - Been working on a few, like getting the Arquillian tests running again.  There's plenty more to do.
	5. WQ - Ok, good, so we expect to discuss in depth during the Developer Conference.
3. **Collaboration with the GeoNetwork community**
	1. LM - Been having a discussion about how to work with the GeoNetwork community.  The approach emerging from the work European Dynamics are doing involves adding additional hooks into core GeoNetwork as integration points for the plug-in OpenWIS components.  We would develop those hooks and contribute them to the core GeoNetwork for anyone to use.
	2. PR - I had a look at the GeoNetwork mail-lists and they are very active; people raise questions and seem to get answers; there are a few on there we would be interetsted in.  So, we thought we could enter the GeoNetwork community by the front door and get our developers to join the Geonetworks developer mail-list.  We would then ask questions, write code, make pull requests and see how we are welcomed.  There is also a user mail-list, so Dom and others could perhaps join that and post user type questions there.  Anyway, I suggest we start with Leon and the guys from European Dynamics.
	3. ACT-OWIS-TC-2016-47: LM/NM/GT/DP/DG - Join the GeoNetworks developer mail-list. OWIS-ACT
	4. PR - If that doesn't work for us then we'll try our other contacts in that community.
4. **AOB**
	1. **Deployment of 3.14**
		1. PN - We're currently deploying 3.14.5 to production at UKMO and still have a few niggles that we're working through.
		2. PN - We've shared the puppet scripts with NWS and will put them onto GitHub.  Note that they are for a 9 VM RHEL 7 set up, so they will require work to use for a different configuration.
		3. PN - We're doing some further security testing; anything that comes up will probably get raised as an issue for v4.
		4. PN - We intend to patch up to 3.14.6 or 3.14.7, then we will be done with v3 development.
	2. **WMO WIS Monitoring**
		1. WQ - Yang issued an updated python script based on the new spec - it produces a modified JSON file.  Is anybody using it yet?
		2. PN - We're not yet but we expect to on v3.
		3. At CBS on Nov 23rd we will do a demo.  At the last TT-GISC we agreed all centres would provide the JSON files by the beginning of October.
		4. PN - Ok, we'll try to do that.
		5. OL - Have BoM done that yet?
		6. WQ - Yes, yesterday.
		7. PN - Our v3.10 will produce the old JSON and the 3.14 will produce the new JSON.
		8. WQ - We're producing both because we didn't want to break the old WMO dashboard.
		9. OL - So, we just run the python script under cron?
		10. WQ - Yes.
    
WQ - Ok, thanks everybody.  And thanks to Steve for organising the Developer Conference, I hope it is a success.

SO - Thanks, a lot of people have been involved in organising it, I'll mention them at the event.


---

#### Participants

- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM], Chair
- LM - Leon Mika, Bureau of Meteorology, Australia [BoM]
- YW - Yang Wang, Bureau of Meteorology, Australia [BoM]
- OL - Okki Lee, Korea Meteorological Administration, Republic of Korea [KMA]
- HL - Hyekyoung Lee, Korea Meteorological Administration, Republic of Korea [KMA]
- SP - Sungeun Park, Korea Meteorological Administration, Republic of Korea [KMA]
- CSP - Chung Shin Park, Korea Meteorological Administration, Republic of Korea [KMA]
- SO - Steve Olson, National Weather Service, USA [NWS], Vice-Chair
- MGi - Marc Giannoni, National Weather Service, USA [NWS]
- DJ - Duncan Jeffrey, Met Office, UK [UKMO]
- DW - Dominic Woollatt, Met Office, UK [UKMO]
- PN - Paul Nelson, Met Office, UK [UKMO]
- PR - Paul Rogers, Met Office, UK [UKMO]
- NM - Nassos Michas, European Dynamics, Greece [UKMO]
- GT - Giorgos Tryantafyllidis, European Dynamics, Greece [UKMO]
- DG - Dimitris Gianneler, European Dynamics, Greece [UKMO]
- DP - Dimitris Papadeas, European Dynamics, Greece [UKMO]

