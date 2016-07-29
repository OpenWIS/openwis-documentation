---
layout: page
title: OpenWIS Technical Committee 2016 July
---

## 7th July 2016 - teleconference - meeting minutes
---
1. **OpenWIS 3.14**
	1. **Update to the patchable version of Java that Martin and Marc are working on for the portals and OpenAM.**
		1. MGo - So Marc and I identified either a 2 day or a 2 week fix and we went for the 2 day fix.  It builds but there are issues during execution on the test environment.  Probably a couple of days work for Marc to work through the dependencies.  See the [build job](https://openwis-association.ci.cloudbees.com/job/openwis-fix-openam-portals-java-version/).
		2. PN - So when can we expect 3.14.7?
		3. SO - Does Marc know what the exceptions are?
		4. MGo - Yes.
		5. A-OWIS-TC-2016-43: SO/MGo/MGi - will speak on Friday morning (8/7/16). OWIS-A
	2. **Revisit of action items pertaining to OpenAM and OpenDJ scripts and whether they are available in GitHub.**
		1. MGo - MF provided the [install scripts](https://github.com/OpenWIS/open-dj-am-install-scripts). They install OpenAM and OpenDJ with just a few manual steps.
		2. WQ - Is there any testing or deployment work to do?
		3. MGo - So they need to be integrated into your deployment; at UKMO we are using Puppet, but without the Configurator tool MF used.  That's about a week's work.
		4. RG - We have a newer version of the scripts; Yves is currently testing them.  We will make them available next week.  Any Puppet automation etc will be extra work.
		5. WQ - Ok, so that action is done.
	3. **Revisit of action item pertaining to the status of OpenWIS 3.14.6 with XSS vulnerabilities fixed.**
		1. LM - These issues have been addressed in the code.
		2. MGo - So 3.14.6 builds but it hasn't been tested.
		3. PN - At UKMO we are currently working to deploy 3.14.5.  We aim to deploy 3.14.6 in a couple of months time and will test it by then.
		4. WQ - So we will each test in our own environment.
		5. MGo - I sent the [link to the build](http://repository-openwis-association.forge.cloudbees.com/openwis/) in an email earlier.
	4. **Where do we go from here for OpenWIS 3.14?**
		1. PN - We are deploying OpenWIS 3.14.5 on a Test/Pre-prod environment.  At present we are investigating an issue with connections.
		2. MGo - The system has a production load with syncs and ingestion running and users logging in.  We start getting connection timeouts after a couple of hours and dissemination options go missing from the portal, which becomes generally unstable.  We've been looking at the code which fetches the dissemination options but it doesn't try to trap any exceptions, nor check that the database call return is a valid result, nor tidy up its connections.  I've added some debugging to it.
		3. PN - Is anyone else running this version or getting these issues?
		4. LM - I can confirm that this code is an old file that hasn't been changed in a long time.  So we are running it on our system and not getting these issues.
		5. MGo - Yes, it looks like a connection problem is the underlying issue.
		6. PN - So, Leon, you say you are running with a Tomcat connection pool of 200?
		7. LM - Yes, we haven't changed from the Tomcat default.  We haven't changed the DB connection pool either, which is set to 10.  I am currently running a test to log the count of open files on the server.
		8. MGo - How many sync jobs do you have running?
		9. LM - Quite a few, I'm running the sync for most GISCs.
		10. OL - We are running OpenWIS v 3.14.6 and testing it.  Is the problem only in OpenWIS v 3.14.5?
		11. MGo - We've seen the issues in v 3.14.3 and v 3.14.4 as well.
2. **OpenWIS 4**
	1. **Current status with metadata search index (Apache Lucene vs Solr) and the scaling problems experienced with it.**
		1. **Any updates from GeoNetwork community as to how they will resolve this issue?**
			1. PR - We haven't begun to address this problem yet, because we've been too busy automating deployment of 3.14 and trying to get that to work for production.  We did speak to GeoCat when the problem first arose and they did some investigation, but they didn't come up with any quick solutions.
		2. **Is this something that the OpenWIS Solr portal can be used to fix?**
			1. PR - We have been thinking along the lines of Solr or Elastic Search.
		3. **Should we spend some development effort to assist GeoNetworks to address this.**
			1. PR - We are still aiming to resolve this problem and release OpenWIS 4.1, along with the other OpenWIS 4 changes we have been working on.  However, SCISYS (Martin and Andy) are leaving the project (more on that later), so this will happen later than planned.  For now, Martin and Andy have packaged up OpenWIS 4.0 so that everyone else can look at OpenWIS 4 while we work on this problem.
			2. LM - I spoke to Simon Pigot recently when he visited BoM.  Apparently, the GeoNetwork community plan to put Solr into v 3.4, though Simon said he would prefer it to be in 3.2, so Simon would be interested in any work we plan to do here.  Should we be targeting GeoNetwork v 3.2 rather than 3.0?
			3. PR - Ok, we will talk to the GeoNetwork community before we do any work on this.
			4. RG - When will v 3.2 be out?
			5. LM - By the end of this year.
			6. SO - How big a pool of metadata records causes issues with GeoNetwork 3?
			7. MGo - Anything over 2000 records causes issues.
			8. RG - And we have about 180,000 records, far above anything Lucence can handle.  So, we are stuck until we have Solr?
			9. PR - We still aim to have the harvesting working for the OpenWIS v 4.2 release in March 2017.
			10. RG - Even though you don't know how much work will be involved?
			11. PR - Yes, that's the plan.
			12. RG - So, you want us to look at the v 4 functionality on the development environment and perhaps show it to Users?
			13. PR - Yes.
			14. MGo - I've put it onto the Proxmox servers and Andy has Puppetised it.
			15. PN - What state is it in?
			16. MGo - Leon and Dom have logged-in.
			17. LM - It's only the portal at the moment; I will try to get the Data Services on there by the next TC.
			18. MGo - We can also run it on AWS.  Currently it uses the internal GeoNetwork security mechanism rather than OpenAM etc.
			19. WQ - I have looked at the portal briefly.
			20. RG - At present it is available through a non-standard port.
			21. MGo - It's port 8080, the default for Tomcat.
3. **Shared working space in MF private cloud**
	1. **Introduction from MF**
		1. RG - So currently MF has rented a couple of servers.  They run [Proxmox](https://www.proxmox.com/en/) a kind of light-weight VMware.
		2. RG - The servers are dev1.openwis.io and dev2.openwis.io.  They are configured as a private LAN and network address tables (NAT) hide the IP addresses.  This has limitations in that management of the whole environment can't be open to everyone because we can't have more than one team with root access.
		3. RG - So, we need to allocate a team to manage the dev2 environment, that would configure VMs for everyone else.  MF has done this for Leon and Martin and then they have installed whatever stack they want on top.
		4. WQ - Are MF happy to continue in this server management role?
		5. RG - Yes, we are happy to continue to do that.
		6. A-OWIS-TC-2016-44: RG - Will send round an email with the team contact email address. OWIS-A
		7. The NAT is done by IP tables but we are considering a proper proxy server on dev2, so that we can call the target URI openwis4.io or something.
		8. OL - What is dev1 used for?
		9. RG - other MF internal stuff.
4. **OpenWIS Developer Workshop**
	1. **Workshop agenda**
		1. WQ - How many days do we need for the workshop?
		2. SO - I have the venue booked for the whole week, Monday to Friday, 26th to 30th September 2016.
		3. RG - the last workshop was 3.5 days.
		4. PN - What are the agenda items so far?
		5. SO - I would like to run the initial draft agenda past a couple of people early next week before I send it out more widely.
		6. RG - 3 or 4 days should be sufficient, can we agree that we will start Tuesday?
		7. OL - Perhaps Tuesday to Friday morning, so 3.5 days.  Start with simpler things like setup on Vagrant or Virtual Box, but also go a little deeper and look at things like metadata synchronisation, harvesting, pre-production testing, system components and drill-down into things.
		8. LM - So you mean the architectural components and how they work and interact?
		9. OL - Yes.
		10. SO - Ok, so I'll aim to circulate the agenda to all by the end of next week.
		11. WQ - Ok, so let's say 27th to 30th, 4 days max.
		12. SO - Please let me know who is planning on attending.  The workshop facility is on the outer rim so delegates don't need to pass through to the higher security zones - but if you are intending any side meetings with other NOAA staff that would require deeper access, then please let me know.
		13. RG - Please send the precise location of the meeting.
		14. A-OWIS-TC-2016-45: SO - Will email round the address of the Developer Workshop venue. OWIS-A
5. **AOB**
	1. **Personnel changes at UKMO**
		1. PR - As I mentioned earlier, the guys from SCISYS are leaving the project.  We shall miss them, especially Martin who has worked with us for some time now.  Thank you Martin for all the excellent work you have done for us on the project.
		2. SO - When is Martin's last day?
		3. PR - Martin's last day will be next Thursday.
	2. **Personnel changes at MF**
		1. RG - I will be moving to a new position and my last involvement with the project will likely be in September.
		2. My replacement is Michael Claudon

---

#### Participants
- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM], TC Chair
- LM - Leon Mika, Bureau of Meteorology, Australia [BoM]
- YW - Yang Wang, Bureau of Meteorology, Australia [BoM]
- OL - Okki Lee, Korea Meteorological Administration, Republic of Korea [KMA]
- HL - Hyekyoung Lee, Korea Meteorological Administration, Republic of Korea [KMA]
- RG - Remy Giraud, Meteo France, France [MF]
- MC - Michael Claudon, Meteo France, France [MF]
- YG - Yves Goupil, Meteo France, France [MF]
- JP - Jean Perie, Meteo France, France [MF]
- SO - Steve Olson, National Weather Service, USA [NWS]
- PG - Patrick Gillis, National Weather Service, USA [NWS]
- KS - Kari Sheets, National Weather Service, USA [NWS]
- MGo - Martin Gollogly, SCISYS, UK [UKMO]
- DJ - Duncan Jeffrey, Met Office, UK [UKMO]
- PN - Paul Nelson, Met Office, UK [UKMO]
- PR - Paul Rogers, Met Office, UK [UKMO]

