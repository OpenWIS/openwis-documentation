---
layout: page
title: OpenWIS Technical Committee 2017 March
---

#### 20th - 21st March 2017, Toulouse, France - meeting minutes

---

1. **Welcome and introductions**
    - SO - Welcome everybody.
2. **Approval of agenda**
    - SO - All happy with the agenda?
    - SO - Ok, the agenda is approved.
3. **Declaration of delegates**
    - PR - Delegates and attendees are listed at the foot of these minutes.  
    - PR - Six delegates are present in the room and one delegate is on WebEx; with seven of seven represented, the meeting is quorate.
4. **Outstanding actions**
    - PR - So, just running down the Action Tracker, which lists Actions open at 15th March 2017:
    - Sep DC-2016-01: LM - Creation of video on the build process
        - LM - To do: [Action-DC-2016-01-Build process video](https://github.com/OpenWIS/openwis-documentation/issues/149)
    - Sep DC-2016-05: PR - Have full sponsor’s Legal review CLA agreement and comment
        - PR - In progress: [review of CLA, form and process](https://github.com/OpenWIS/openwis-documentation/issues/98)
    - Sep DC-2016-07: RGr - Administration of Open Mailing list. Probably need to have one administrators of this list
        - PR - Done, closed.
    - Sep DC-2016-11: LM - General examination of extended JBOSS capabilities for portals) (Action: Entire Team, led by Leon)
        - LM - To do: [Action-DC-2016-11 JBOSS Capabilities](https://github.com/OpenWIS/openwis-documentation/issues/233)
    - Sep DC-2016-13: LM - Examination of using GN3 LDAP for user accounts. Work to understand is how to shoehorn user permissions and groups to data as well as metadata, and the application of this to cache.
        - LM - Covered by the general examination of CGN v3 for OpenWIS v4.  Action closed.
    - Sep DC-2016-17: MC - Update OpenDJ/OpenAM scripts for deployment
        - MC - Done, the code was pushed to the dev branch in Dec.  Action closed.
        - PR - New: [Action-TC-2017-01 Merge OpenAM/DJ changes to master]( https://github.com/OpenWIS/openwis-documentation/issues/151)
    - Dec TC-2016-59: All - review OpenWIS v4.0 and provide the feedback as GitHub Issues within the OpenWIS4 repository.
        - DW - Will report on this later on. Action closed.
    - Sep TC-2016-46: LM - Circulate the url of the portal on Proxmox.
        - LM - Done, closed.
    - Jul TC-2016-44: RGr - Will send round an email with the team contact email address.
        - PR - Done, closed.
    - Mar TC-2016-25: WQ - TC to set a task to develop on-boarding docs set for developers.
        - LM - Pretty much done except for the architecture docs.  Action closed.
        - LM - New: [Action-TC-2017-02 Architecture docs]( https://github.com/OpenWIS/openwis-documentation/issues/152)
    - Mar TC-2016-23: JT - Include the requirement for the Security Service to control data access in the Data Policy workpackage.
        - PR - Covered by the general examination of CGN v3 for OpenWIS v4.  Action closed.
    - Mar TC-2016-22: RGr - Create a work package to review Data Policy and Access Control implications in detail.
        - MC - To do: [Action-TC-2016-22 Review Data Policy and Access Control](https://github.com/OpenWIS/openwis-documentation/issues/234)
    - Mar TC-2016-21: RGb - Investigate how to link the data policy in the metadata with the assignment of GeoNetwork privileges.
        - RGb - Covered by the general examination of CGN v3 for OpenWIS v4.  Action closed.
    - Mar TC-2016-20: JT - Create a work package for WMO metadata guidance templates.
        - JT - To do: [Action-TC-2016-20 WMO metadata guidance](https://github.com/OpenWIS/openwis-documentation/issues/150)
    - Mar TC-2016-18: JT - Create work package on UI improvement for bulk subs.
        - PR - Bulk subscriptions is one of the hot issues we expect to resolve using the Overlay approach, so we'll specify a requirement when we do that work.  Action closed.
    - Mar TC-2016-15: RGb - draft a User Story for the User Portal subscription process.
        - PR - Action closed, for same reason as action 18 above.
    - Mar TC-2016-13: WQ - document the design pattern policy; still deploy to wildfly in short/medium term.
        - LM - There is an issue here; Java 8 won't work with JBOSS 7.  Pass action to LM: [Action-TC-2016-13 Investigate Wildfly](https://github.com/OpenWIS/openwis-documentation/issues/235)

5. **Retrospective (past year)**
    1. LM presented this summary of the work over the past year: [OpenWIS Retrospective](https://docs.google.com/presentation/d/1ymCkRa-0elUnMYOJhztjJu-k4-SqhqPH8-d8lt58v_Q/edit?usp=sharing​)
    2. LM presented the results of an online survey he ran within the OpenWIS community: [OpenWIS Survey]({{ site.baseurl | prepend: site.url }}/assets/TC201703-OpenWIS_Retrospective_Survey.pdf)
    3. LM - From the survey results it is clear that the time it takes to rollout or install is considered by most to be a serious issue.
    4. MF - Regarding the check on compliance with the Technical Specifications (1.0), during the Developer Conference - how was that check done?
        1. LM - We did a theoretical comparison of the technical regulations with the expected features of OpenWISv4.  It looked good in that we didn't find anything we thought would be a major non-compliance.
6. **Current development planning (coming year)**
    1. **OpenWIS4**
        1. NM presented this summary of the work on OpenWIS4: [Progress to date]({{ site.baseurl | prepend: site.url }}/assets/TC201703-Progress-to-date-v2.pdf)
            1. NM - we are in the process of releasing v3.14.8, but we ran into a problem with the ForgeRock open source repository - they have closed it!  This means we can't build v3.14.8 until we put the artefacts we were getting from there somewhere accessible.  The situation with ForgeRock is strange - it raises the question whether we want to continue using ForgeRock open source.
            2. SO - Regarding the testing referred to on slide 5, I assume that's for the build; are there plans to run audit tests?
                1. NM - We have not discussed that yet.  We will need a full set of tests for future releases, unit tests and everything else.
            3. SO - How much attention do we want to pay to SAML? If we envision the use of SAML for individual users, we may want to discuss that here this week.
                1. NM - GT has worked on that.  We have the choice of using an external SAML provider or using the internal security in CGN.
                2. JT - The difficulty of installing OpenAM/DJ has given us the impetus to break-out the security.
                3. PR - Especially since ForgeRock just closed their repository.
                4. NM - We will have to find those artefacts and build/provide them ourselves.
            4. SO - What about automated installation?
                1. NM - We have used Puppet for these instances.  
                2. BR - Only for the development environment?
                3. NM - We have cleaned up the Puppet scripts we use for the Vagrant installs; now you can use them on VMware or on bare metal.  I wouldn't say they were production quality scripts, but they're good enough for serious testing.
                4. SO - That's good; we use Puppet for our operations.  If there is interest from other operations centres then we can share those.
                5. NM - If there is interest in operational Puppet scripts then we can make those too.
                6. KS - Are ECMWF using Puppet?
                7. BR - Yes, we are moving to Puppet.
                8. SO - By using Puppet, we have deployment down to a couple hours.
                9. NM - We have put instructions on the wiki about how to use Puppet for VM and non-VM installations.
        2. GT presented: [Overlay Approach]({{ site.baseurl | prepend: site.url }}/assets/TC201703-Overlay-approach.pdf); what is it and why do we need it?
            1. GT - So, the Overlay approach adds a little more complexity at the start, because you have to learn to use the method that applies to each kind of plug-in you want to make, but, it gives you independence from whatever GeoNetwork may do, unless they make a major change.  Even then, we just have to adapt our approach.
            2. SO - This is repeatable, scalable and flexible?
                1. NM - Yes.
            3. SO - Have we investigated how receptive the CGN community are to our changes?
                1. NM - Well, we fixed a small bug and the pull-request took 2 and a half months to be accepted.  So, contributing our features could be long and complex. For any major contribution, we would have to agree with them in advance that they want it.
                2. GT - Loose coupling would be best for OpenWIS; it would also be best for CGN.  We could contribute the whole approach to CGN.  It gives anyone flexibility in contributing back to them.  But, it all depends on what they want to do; we should discuss that with them.
                3. NM - So we need a background communications channel if we work in their code.  While it would be useful, we don't depend on that communications channel if we use the Overlay approach; we release as often as we want without CGN approval.
                4. GT - So far, we have added the plug-in mechanism, as well as the features that GeoCat worked on before.  It would be better if we were able to plug-in directly, but CGN has no hooks, it was not designed to work that way. We could contribute some glue code, but we would need to contact them about that.  We could also contribute some features they do not have, like subscriptions.
            4. SO - Are there any compatibility issues with the Overlay approach?
                1. NM - As long as the plug-in places don't change we don't have any compatibility issues.  If they removed a major feature, say the entire Admin Menu, then our code would break and we would have to fix it. But, we would only have to fix that part.  We are as independent as it is possible to be.
            5. JT - The Overlay approach is based on Angular JS, right? So we are less concerned about binding into Core GeoNetwork code.
                1. NM - That's right, we don't need to pull-request back to Core GeoNetwork, but we could if we wanted.
        3. NM presented: [Skills and training]({{ site.baseurl | prepend: site.url }}/assets/TC201703-Skills-and-training.pdf) - how will we transfer skills in the Overlay Approach?
            1. NM - So its a mixture of skills; there is some legacy technology left hanging around in CGN as well as some newer technology.  This is expected of a 10 year old project.  A lot of it is XML based.
                1. SO - What schemas are supported out of the box?
                2. NM - This XML refers to component configuration rather than for metadata. Wro4j also uses XML.
                3. SO - Is there support to change that through plug-ins?
                4. NM - No need to do that, just change the XML.
            2. NM - We have made plug-in examples of all the components we could think of; there may be a few others.
            3. RGb - Is it possible to disable SSO?
                1. NM - OpenWIS v4 does not use SSO by default; you have to enable SSO if you want it.  You can do that, but CGN will not create new users in your SSO.  CGN has built-in security that you can use out of the box.  If you are currently using SSO then you might need a way to port your User accounts from your v3 SSO to the v4 CGN database.
        4. Developer Conference - when and where is best to embed Overlay Approach skills?
            1. PR - Can we just take a poll of how many coders each organisation is likely to have who will need training in the Overlay approach:
                - KMA = 1
                - MF = 2/3
                - MFI = 1
                - FMI = 1
                - ECMWF = 1
                - NWS = 2/3
                - BoM = 2
            2. PR - Ok, so we could do some WebEx training first, so that GT can take small groups through the approach and get people started.  Then later, if further consolidation is required, we could arrange a Developer Conference. Assuming the SC are happy with the approach, the TC can schedule the training, then the Developer Conference later.
                - SO - [Action-TC-2017-20 Schedule Training](https://github.com/OpenWIS/openwis-documentation/issues/230)
                - SO - [Action-TC-2017-21 Schedule DevCon](https://github.com/OpenWIS/openwis-documentation/issues/231)
        5. GeoNetwork3 features relevant to OpenWIS4
            1. DW presented the following analysis of GeoNetwork v3.2.1 and OpenWIS v4.0: [powerpoint]({{ site.baseurl | prepend: site.url }}/assets/TC201703-GeoNetwork_Features.pptx)/[pdf]({{ site.baseurl | prepend: site.url }}/assets/TC201703-GeoNetwork_Features.pdf); additional discussions about each slide are captured below:
                1. **Home Page**
                    1. DW - The main question I would raise here is whether we need the Admin and User portals to be separate; something to think about.
                2. **Search Page**
                    1. DW - The keywords you see here are extracted from the metadata.
                    2. DW - GeoNetwork has built pseudo parent/child metadata.
                    3. DW - The keywords can be used to narrow your search, better than we can in v3.14.
                    4. DW - There are more map search options in v3.14; but do we need them all?  There is no Lat/Long search, which would be useful, I think, so we might need to develop that.
                    5. DW - The documentation for GeoNetwork v3 isn't finished yet and is poor in places, or even misleading, because it is still the old v2 documentation.
                    6. SO - Does the left hand column show all the metadata you put in, or is that configurable?
                    7. DW - Don't know. It's all from your metadata, Geonetwork seems to recognise what it can use; perhaps it works it out from the ISO schema?
                    8. BR - Have you loaded the whole catalog?
                    9. DW - No, just a few.
                    10. BR - If you load more, will the left hand side explode?
                    11. DW - There seems to be a limit of 25 per heading; but that's no good to us, maybe it is configurable.
                    12. BR - Looking at the keywords, it looks random.
                    13. DW - Perhaps it needs work with our metadata; we could get rid of this tool, but I found it useful.
                    14. MG - How many levels do the parent/child relations go?
                    15. DW - It's not really parent/child; it's just grabbed headings from the metadata.
                    16. MG - Lucene flattens the metadata out, so you lose structure.
                    17. DW - There is no parent/child in the WMO metadata.
                    18. BS - Can we configure this?
                    19. DW - Nothing in the documentation to say whether we can or not. GeoNetwork acknowledge that the documentation is incomplete. We may find some information on their forum; might be best if we raise a list of questions on there.
                    20. DW - The initial metadata view is a cut-down version; it can be expanded, but it is useful for a quick check that you have found the thing you were looking for.
                    21. DW - The _subscribe_ button is part of the OpenWIS4 overlay.
                    22. DW - the other display icons, such as the social sharing buttons, may be useful, or we can remove them.  No other GISC will have them so maybe hide them.
                    23. SO - Are subscriptions _push_ or _pull_?
                    24. DW - Depends how your Harness works; we would use _push_ through our Message Switch. That bit isn't working yet, there is no data in the data cache.  Note that _provided-by:_ is missing; it would be useful to add that.
                    25. BR - Unless it's from the OAI-PMH source.
                    26. DW - Maybe.
                    27. **View Metadata**
                        1. DW - Nice _dataset_ and _climat_ icons.
                        2. DW - Icons built from keywords and topics.
                    28. **Metadata Options**
                        1. DW - It's not clear how _owners_ and _groups_ work when managing metadata.
                        2. DW - You can create a child group, but that wouldn't work for other GISCs.  This is why we need parent/child in the WMO metadata model. We should switch that feature off until we have that.
                        3. DW - Can transfer ownership eg: _institutional_.
                3. **Admin Page**
                    1. DW - The summary on the right hand side is similar to OpenWISv3 but it is broken down further.
                    2. DW - Groups, roles and privileges are similar to how it was before, though now a user can be a member of more than one group. But, lining this up with harvesting doesn't work well.
                    3. BS - Is it possible to associate and editor with a specific group of metadata?
                    4. DW - Yes, but on the GISC all metadata belongs to a single group: _institutional_. Could be useful for a DCPC.
                    5. BS - But any user can upload to any group, not just their own?
                    6. DW - Not tried that, we'll need to test.
                    7. **Groups**
                        1. DW - In GeoNetworkv3.2.1 and OpenWISv4.0, groups cover metadata, not access to the data itself.
                        2. DW - A user has to be in the group to see the metadata.
                        3. DW - You can subscribe to the data but you have to get your privileges uplifted manually to get the data. Maybe AKKA put something in to cover this; if so we need to add that.
                        4. DW - There are no overall group privileges like in v3.14.
                    8. **Privileges**
                        1. DW - There is a difference between metadata and data access privileges.
                        2. DW - Privileges are now assigned to groups rather than users, which causes issues with sync.
                        3. DW - We want everyone to discover metadata but not necessarily have access to the data.
                        4. PR -Where are the data access policies in v3.14?
                        5. DW - Data Services?
                        6. PR - So we need to migrate the v3.14 Data Services to OpenWISv4.
                        7. SO - Various ways we could do this, eg: assign to LDAP.
                        8. DW - Managing the metadata in groups makes sense, but we need the functionality that AKKA added into GeoNetworkv2 in OpenWISv4.
                        9. RGb - Metadata visibility; how is this affected?
                        10. DW - If you assign metadata to a group that none of the users are in, none of them will see the metadata.
                    9. **Roles**
                        1. DW - Helpful for DCPCs; if they used the _metadata-portal_, then the GISC could approve before publication and the metadata only gets displayed when it is ready.
                    10. **Blacklisting**
                        1. DW - This function is added via the overlay technique.
                        2. DW - I've never seen the point of Blacklisting. If users have access to the whole catalog, then they have access to the whole cache. Yes, that is a lot of data, but isn't the point that if they are allowed access to the data then they are allowed to get it. We might discuss this during the workshop later.
                        3. BS - We use it to prevent a user getting too much data.
                        4. DW - Aren't customers allowed to subscribe to whatever they discover? We'll debate this later.
                            - DW/BS/SO: [Action-TC-2017-03 Blacklisting](https://github.com/OpenWIS/openwis-documentation/issues/153)
                    11. **Users**
                        1. DW - There are more fields we can fill in, but also some missing, such as _class of service_ and _favorites_; do we need these?
                    12. **Managing Categories**
                        1. DW - The way GeoNetworkv3 does this is not the way we currently work; we do it by GISCs, but they want it broken down by datasets.
                        2. DW - Categories can have a logo; could we use them for GISCs?
                        3. DW - Though the UI looks different, it works in a similar way to the old one.
                    13. **Harvesting**
                        1. DW - The documentation on harvesting is very poor; it appears to be the old v2 documentation.
                        2. DW - Some useful features we had are missing in the new version, I think; hard to say without proper documentation.
                        3. DW - Harvesting is very slow, which is why Nassos had to come up with an improved method.
                        4. DW - Harvest set up is ok; a few minor bugs.
                        5. DW - The harvest count is wrong.
                        6. DW - I have concerns about _Sync_; it says it's doing a sync, but in the interface log it looks like a full harvest, although it appears to be quicker.
                        7. DW - There is no button to force a _validation_. There was an issue with the Melbourne metadata, but not sure what. Validation seems to have to be done after the harvest, but an editor can't really do an edit after a harvest.  Unfortunately, you can't just choose a GISC and press _validate_. Is OpenWISv3 validating against ISO 19139? I dunno.
                        8. DW - Still getting memory errors, but there is no alerts page like in OpenWISv3.
                    14. **Metadata**
                        1. DW - Supports ISO 19139 and a couple of other standards.
                        2. DW - So this is the screen where you add metadata and it has these icons for the edit functions.
                        3. SO - Are those icons based on your privileges?
                        4. DW - I guess so, they disappear when harvesting; you can't edit harvested metadata.
                        5. DW - We would need to configure these menus.
                        6. DW - Now, do we need _stop-gap metadata_? As far as I can see, no-one is fixing the _stop-gap metadata_, so we need to discuss this.
                            - DW/LM/BS/SO: [Action-TC-2017-04 Stop-gap metadata](https://github.com/OpenWIS/openwis-documentation/issues/154)
                        7. DW - Admin gets logged as the owner of the metadata, just because the Admin harvested it; but the Admin doesn't own the metadata.
                        8. DW - If you add duplicate metadata you can sometimes overwrite the original metadata unintentionally.
                        9. DW - OAI-PMH: OpenWISv4.0 only gives us a _category_, whereas OpenWISv3 gives us a _count_ as well; we need to have that in v4.
                        10. DW - GeoNetworkv3 has the concept of a metadata _lifecycle_; this could be useful for DCPCs and NCs.
                    15. **Reports**
                        1. DW - These need work to be useful.
                        2. DW - They can be extracted into CSV/Excel, but they're not well presented.
                        3. DW - There are some nice charts and graphs in Status/Statistics that may be useful to show what metadata is being used.
                    16. **Batch Tools**
                        1. DW - I had hoped that this would be good for changing multiple fields, but it doesn't allow you to change all the XML headers you would want.
                4. **Further analysis required**
                    1. DW - So, there is still work to do to identify everything important that is still missing from the combined GeoNetworkv3.2.1/OpenWISv4.0 package.
                5. **Q&A**
                    1. SO - Is there metadata version control?
                    2. DW - Yes, but only in your system, using _last updated date_; but no version number.
                    3. PR - Wouldn't that have to be in the WMO metadata?
                    4. MG - Seems like there's a lot to do to get this to do what we want. We're looking at a big tool-chain and complexity to keep this going.
                    5. BR - We have a project where we use GeoNetwork to do the heavy lifting, but also Drupal for the outside world.
                    6. MG - I don't consider the UI heavy lifting.
                    7. NM - Ok, the UI is lightweight, but there are many things going on in the backend. There are close to 100 issues that we must at least investigate. The question is: how does the backend suit our purposes? The more we deviate from vanilla GeoNetwork, the more load we have to carry. We can't really say at the moment whether it is better to continue with GeoNetwork.  However, from what I have seen, GeoNetworkv3 isn't the best scaffolding to build on. Maybe we could come up with a couple of options and work out how much effort each would take.
                    8. SO - We may need to delve into the next level.
                    9. DW - Nassos is presenting some future options later...
                    10. PR - ...when the Bureau is online.
                    11. SD - GeoNetwork is an essential part of OpenWIS - managing the metadata - so we need to check compliance.
                    12. DW - If we do the work we should be able to get a v4 that does what we need.
                    13. SD - The Data Policy needs to be taken care of.
                    14. BR - You have to implement the Data Policy yourself, through a flag in the metadata.
                    15. DW - This is where the AKKA glue comes in.
                    16. PR - I think that's in the Data Services that LM is expecting to port from OpenWISv3.14.
                6. **Demo instances**
                    1. DW - Anyway, you can all have a look for yourselves at the demos that ED have set up:
                        - [GeoNetwork 3.2.1](http://cgn-original.eurodyn.com:8080/geonetwork)
                        - [OpenWIS 4 (using GeoNetwork 3.2.1)](http://cgn-openwis.eurodyn.com/geonetwork)
                        - (The credentials required to log into these instances are available from GT)
        6. Compliance of OpenWIS4 to WIS Technical Regulations
            1. SO - Wasn't sure who would lead this, it was discussed at the Developer Conference in Washington.
            2. DW - Should we wait for JT, to talk about WIS2.0?
            3. MF - There won't be any 2.0 Technical Regulations for a while, so OpenWIS needs to remain compliant with the 1.0 Technical Regulations.  That compliance must be recorded and preferably published.
            4. PR - Ok, when we look at the lifecycle later, you will see on the diagram that test criteria for 1.0 compliance feed into the acceptance procedure via requirements, so proof of compliance is a test outcome.
    2. **Development process for OpenWIS4**
        1. Engagement with the Core GeoNetwork Community
            1. PR - We know who the Core GeoNetwork community is:
                1. PR - The [repository](https://github.com/geonetwork/core-geonetwork) is public
                2. PR - We worked with two of the main developers from GeoCat, Maria (Delawen) and Jose (josegar74) during 2015
                3. PR - JT is acquainted with the founder, Jeroen Ticheler
                4. PR - Other members are known to some of us - eg: BoM/Simon Pigot
            2. SO - How transparent are they?
                - NM - The code is very open; we've not seen much of the community governance; seen no roadmaps.  We haven't explored how we would work with any committees; we just submitted a small pull-request.
            3. SO - How engaged do we want to be?
                - NM - Depends; technically, it will always be easier to do things in their code than to work independently, but obviously that increases our dependence on them.
        2. Process for handling contributions offered from external collaborators
            1. SO - I wanted to discuss how external collaboration would work in an open source environment. I have 2 questions relating to external contributors:
                1. What are the ground-rules?
                2. What is the process?
            2. SO - Here are my initial thoughts (email):
                1. Motivation to expand developer participation.
                2. Discuss level of code openness.
                3. Discuss vetting needed to support expanded openness.
                4. What needs defining:
                    1. What is the nature of the project - how open do we want it to be?
                        - Who gets to access the code?
                        - Do we want a login at all?
                        - Can any developer participate, or only weather-related entities?
                        - Who gets to join (who gets to get access to the code) and what are requirements?
                        - Can non-GISC members join?
                        - To what degree do you need to have a relationship with a GISC entity to join?
                        - Do we really want a true open-source community?
                    2. Given a less than completely open posture, how does vetting happen?
                        - Are there technical qualifications?
                        - Are there organizational qualifications?
              3. PR - Ok, so let me explain a little about how the GitHub repositories work, to give some context:
                  1. Most of the code repositories are public, which means they are open for anyone to read the code, the issues, the documentation, anything we put on there.
                  2. To do anything else, for example, update code, fork the repo or comment on an issue, the user must sign-in to GitHub.
                  3. To update code, the user account must have the rights to update the relevant branch assigned to it, by the UKMO Release Engineering team.
                  4. Usually, you would issue a Pull-Request from your own fork and get your code reviewed prior to updating a branch.  If you try to update a branch you do not have permission to update, GitHub does not update the branch, instead, it generates a Pull-Request for you.
                  5. A Pull-Request can only be merged by someone with the permissions to do so.
                  6. As a safety precaution, only the UKMO Release Engineering team has permission to update the master branches and the rest of us merge our forks into the develop branch.
              4. SO - Do we use the forum to manage discussions about contributions or potential contributions?
                  1. PR - If the code/pull-request exists or relates to an existing issue or kanban task, then we would discuss that on GitHub. The CLA process says that it is the responsibility of the Pull-Request reviewer to ensure a signed CLA is on file. We would use the forum to discuss new ideas or perhaps new contributors.
                  2. NM - Having to sign a CLA makes it more difficult for people to submit small changes.
                  3. PR - In future, we might make it easier by having an electronic CLA, but we do need a CLA.
                  4. MP - FMI also require CLAs to be signed, to safeguard future rights to the code.
                  5. PR - Would we expect the TC to be involved in any forum discussions? Perhaps the forum would be used to publish the decision.
                  6. DW - Could the CLA be signed on the forum?
                  7. PR - It might be possible to have the gateway to an electronic CLA on the forum - we should investigate that.
                      - PR/CS - [Action-TC-2017-05 Electronic CLA](https://github.com/OpenWIS/openwis-documentation/issues/155)
              5. SO - Who decides we are going to accept a change or suggestion?
                  1. DW - TC is fine but may need an official SC decision.
                  2. PR - TC/PMC recommends and SC approves.
                  3. MP - We need 3 levels, I think. Small changes can be made lower down; I suggest the person reviewing the pull-request can make the decision. They would escalate only larger changes.
                  4. PR - Yes, the squads could make that assessment.
                  5. SO - GitHub or the forum for small changes?
                  6. MP - GitHub.
                  7. SO - So we keep the forum out of the process for small changes.
                  8. SO - Who would manage the pull-requests and utilize the TC?
                  9. PR - The squads.
                  10. KS - Is there a list of standard questions?
                  11. PR - I guess we would be interested in impacts on the current work. If it isn't small and ends up being discussed on the forum, do we escalate to the PMC/TC?
                  12. SO - Could this be an activity we engage GeoNetwork on; what are their processes?
                  13. DW - Who will find time to monitor and respond to that activity on the forum? What about the 4 week delay between TC meetings?
                  14. SO - We should position ourselves to manage expectations. Do we need a process diagram?
                  15. DW - Copy someone else's process?
                  16. PR - This is a Community Manager task, but while the community activity is low level, we are all Community Managers.
                  17. SO - Any volunteers to define the process?
                  18. PR - Ok, I can investigate some options.
                      - PR - [Action-TC-2017-06 CLA management](https://github.com/OpenWIS/openwis-documentation/issues/156)
                      - BR - Have a look at the CLA on the Discourse forum site.
                  19. RGb - Did we define the Community Manager role?
                  20. PR - Yes, JT has a document describing it. We can ask him about it tomorrow when he joins the meeting.
        3. Options for Forum
            1. SO - Thanks to MF for publishing the forum option demos on the internet.
            2. SO - CS and MG set up these demos, hope some of you got to try them out:
                - [Discourse forum demo](https://discourse.dev2.openwis.io);
                - [Discourse website plugin demo](https://cassie-stearns.github.io/test/discourse40.html)
                - [NodeBB forum](https://nodebb.dev2.openwis.io);
                - (log in to both forums through a portal using: username: openwis password: 9Sym2c3ypjv; You should be able to register on the front page. If you are having problems, please email Cassie with **subject:openwis forum help**)
            2. SO - CS also provided some notes:
                - [Notes on Disqus]({{ site.baseurl | prepend: site.url }}/assets/TC201703-DisqusNotes.pdf)
                - [Notes on Discourse]({{ site.baseurl | prepend: site.url }}/assets/TC201703-DiscourseNotes.pdf)
                - [Notes on NodeBB]({{ site.baseurl | prepend: site.url }}/assets/TC201703-NodebbNotes.pdf)
            3. SO - We wanted to evaluate the following:
                - Which forum do you prefer (Discourse or NodeBB)? Why?
                - Are the categories and subcategories good? What do you want to change?
                - What tags do you think should be used?
                - Any other comments or questions
                - [Comparison so far]({{ site.baseurl | prepend: site.url }}/assets/TC201703-OpenWISForumDevelopment.pdf)
            4. SO - CS will take us through the software.
            5. CS ran through Discourse and NodeBB, via WebEx; some additional questions were asked:
                1. BR - Can Discourse be moderated?
                    - CS - Yes, there are both _moderators_ and _admins_; admins set up the categories for topics.  Discourse has _trust levels_. So a brand new user has limited capabilities.  As they interact, their trust level increases and they get more capabilities. There is a large amount of flexibility in the configuration of these trust levels. We found Discourse easier to manage than NodeBB and when we needed help, the Discourse forum was responsive, whereas we got no replies from NodeBB.
                2. PR - Will we need Disqus?
                    - CS - Probably not.  We were looking at it as a way to put comments on the website pages. Where we do need that, there is a plug-in for Discourse that actually links back to the forum, so Discourse appears to do everything we need in one package.
            6. SO - Are we ready to vote? Yes, ok, let's vote:
                - Discourse: 8 votes
                - NodeBB: 0 votes.
            7. SO - Ok, the decision is to establish the Forum on Discourse and to collect feedback on what Category/Tag/Topic structure we want to start with, to use the Forum in earnest for the next year.
                - SO - [Action-TC-2017-07 Forum on Discourse](https://github.com/OpenWIS/openwis-documentation/issues/157)
7. **Future strategy (to 3 years ahead)**
    1. **Architecture Possibilities for OpenWIS5**
        1. NM presented [OpenWIS5]({{ site.baseurl | prepend: site.url }}/assets/TC201703-OpenWIS5v2.pdf); including pros and cons of v4 vs v5.
            1. SO - Just referring back to slide 7, are we stuck with Lucene?
                1. NM - We could use something else but we would need big changes to Core GeoNetwork. We haven't found a problem with Lucene itself; Solr and Elastic Search both use Lucene and give good performance. So Lucene is fine if it is configured properly.
            2. NM - It takes 19 hours to harvest Beijing because the process makes serial http and indexing calls, one item at a time. However, Core GeoNetwork already supports harvesting from the file-system, so I separated the http calls from the indexing, using an external tool for the http fetch to disk. This gives at least a x10 performance improvement so that you can harvest Beijing in a couple of hours. The external http app is free, has a nice UI, does OAI-PMH and has a built-in scheduler.
                1. BS - But we do the full harvest only once, so it is not a problem, we usually sync.
                2. DW - Well, I tried to set up a harvest from Germany and it is still running, days later.
                3. BS - For us, 21 hours for Beijing is ok.
                4. BS - Is it possible to index separately?
                5. NM - It's not set up that way. Anyway the indexing is ok, it's the http calls that take the time.
                6. BS - Could we compress the metadata?
                7. NM - Yes, if both ends use the same protocol. But that's not really the problem, it's the handshakes etc. Sequential fetch-and-index is a clear design flaw.
                8. JT - A typical GeoNetwork catalog would contain 200 metadata records, whereas we have tens of thousands.
                9. DW - We raised this issue with GeoCat, but they didn't fix it. We don't want a harvest running for 5 days! We've checked memory and it looks adequate. Strangely, the sync log appears to be the same as for a harvest, though a sync does run quicker. You don't get to set a date for a sync, just a time. Also, in v3 you get more breakdown on what was added/deleted.
            3. NM - So for v5, the installation is fully automated, you just trigger it with one command. It is all done using Docker.
            4. JT - So, just referring back to slide 14; what you're calling the _private cloud_ is on public cloud infrastructure, it's private in the sense that you are controlling access. It's just a different instance of the same software. Also, you're deploying multiple instances of the same software because that is much easier to manage and maintain than having a single piece of software do multiple jobs; that would make the software too complex.
                1. BS - Do users have to log in to 2 instances?
                2. JT - No, you would configure your local instance to log in to both private and public clouds.
                3. NM - You define how many upstream clouds you can connect to through your local instance.
                4. JT - Also note that all the metadata is made public, even if the data is controlled. Public data is in a cache that provides simple data access. A DCPC or NC may provide more complex subsets of data through a richer API, outside of the OpenWIS software. OpenWIS just provides the metadata that you use to discover the service end-points.
            6. NM - Slide 16 shows the asynchronous message driven architecture that overcomes the serial processing issues we discussed earlier; it also scales very well.
            7. NM - Slide 18. With the automated, containerized installation, we aim to provide an out-of-the-box experience, but also make it possible to install the OWPC into your own infrastructure or cloud.
                1. SO - There is a lot in your v5 architecture that we prototyped a few years ago and I can vouch for the approach.
                2. SO - Did you think about dynamic vs static queues?
                3. NM - In the PoC they are static. However, we could have monitoring and auto-tuning of dynamic queues. We could also use elastic load-balancing to auto-tune the number of boxes, for example. Docker also has similar auto-load-balancing features.
                4. SO - We were thinking of using JBoss for load balancing, perhaps we don't need that?
                5. NM - You don't need JBoss, but you could use it.
                6. BS - At MF we have a project to Dockerize OpenWIS v3.14, this year. We hope it will also work for OpenWIS4.
                7. PR - It would be useful to have a GitHub issue or Kanban item for that so others could observe progress or even contribute.
                8. BS - [Action-TC-2017-08 v3.14 on Docker](https://github.com/OpenWIS/openwis-documentation/issues/158)
                9. WQ - The architecture looks great. At the Bureau we are building a similar event-driven system with a message-broker at its heart. We did try to Dockerize but our security people say that you can ship malicious code in your container. How can I go to our security people and say not to worry?
                10. NM - The data can be externalised.
                11. WQ - Not talking about data.
                12. NM - In the latest version of Docker, you can get a paid service, _Trusted Registry_, that will auto-scan, validate and sign your container. It is like shipping an operating system, so it is up to us to check. We need DevOps to take care of that; as long as we have guaranteed the parts, they will deploy. We could operate our own private Docker registry, so only our containers are in there and we know what is in them. External companies also offer that service.
                13. MF - You have the yaml manifest, so you can decide whether you trust the services in there.
                14. NM - Ok, but unless you are sure you can trust all those sources, you can't be sure your container is secure.
        2. NM presented a demo of the advanced message queue protocol (AMQP) PoC
            1. NM - So for the PoC we have created a container based on Ubuntu.
            2. MC - So this includes no Core GeoNetwork and no OpenWIS?
            3. NM - That's right, it just demonstrates the underlying message architecture. However, we are doing OAI-PMH harvesting in real-time from real GISCs.
            4. NM - Ok, so the PoC has started; it came up in 1 minute and 10 seconds.
            5. {NM showed the harvest queues working very quickly, the raw XML metadata results from Elastic Search and also a rich variety of out-of-the-box sample UI components}
            6. NM - So, this is what we managed to achieve in just 5 days.
            7. JT - Elastic Search, which is based on Lucene, provides all sorts of tools for geo-searches etc. Some distribution companies use it to track all their parcels. A colleague of mine has 2 billion records in Elastic Search and gets sub-second responses to queries. Elastic Search is open source and you can also buy support.
            8. NM - Elastic Search also does clustering.
            9. SO - We use Elastic Search at NWS to do audit reports on our log files.
    2. **Release roadmap**
        1. PR - So when we set the agenda, we thought this item would be about the schedule for releases 4.1 and 4.2 over the next 12 months. However, after what we heard about v5 from NM in section 7.1.1 and about WIS 2.0 from JT in section 14 (which we did earlier in the meeting to accommodate BoM), we have much more to think about. Now it's more about v4 vs v5.
        2. WQ - If we decide to go for v5, then the sooner the better:
            1. Why spend money on v4 when we will soon move to v5?
            2. How could we make v4 align with WIS 2.0? It could be difficult.
            3. The way we build v5, modular, bearing in mind that WIS 2.0 is still taking shape, we should be ok, confident that it will align with WIS 2.0.
            4. So we should do the bare minimum on versions earlier than v5.
        3. JT - A key difference between v4 and v5 is the shape and handling of metadata:
            1. The WIS 2.0 strategy document talks about discovery by search engines...
            2. Rather than the use of heavy-weight ISO metadata standards that are difficult to operate.
            3. So I think we will see a significant change in the way we do those things.
            4. v4 leverages the management of metadata by Core GeoNetwork in that heavy way.
            5. v5 brings much lighter metadata management.
        4. JT - The modularity that we strive for today could be developed for v4 and reused for v5.
            1. NM - If we start changing Core GeoNetwork in such a major way then we end up with our own product. I would prefer to do that in cooperation with the GeoNetwork community.
            2. JT - But we could do some containerization.
            3. NM - They currently use the Quartz scheduler so there could be some difficulties. Better to do those kinds of changes in their source code.
            4. JT - Core GeoNetwork is only one of the 6 or 7 components; could we do the message-driven thing to the Data Services, cache, etc?
            5. NM - Yes, we could.
            6. JT - Ok, let's use Core GeoNetwork to the max but not unpick it; stitch-in our other components.
            7. NM - Yes, ok.
        5. NM - How much effort do we put into v4 before we work on v5? Do the minimum?
            1. JT - As we work on the next level down, the question is: how much effort do we invest in something that will be used for 4ish years?
            2. JT - v4 does improve on v3.
            3. JT - We could work on v4 and do v5 pilot activities in parallel to influence how WIS 2.0 works.
            4. WQ - I agree with what JT said earlier; let's work around Core GeoNetwork in v4. Apart from the plug-n-play features, what new stuff do we really need? Bulk Subscriptions?
            5. PR - We will work that out during the workshop later.
        6. BS - But metadata is not an application problem, it is a WMO problem.
            1. WQ - Agree, but the fact is that OpenWIS is geared to handle that metadata model and 150 thousand metadata records.
            2. PR - So we change the software as much as we can without altering the metadata model.
        7. LM - We can implement Bulk Subscriptions when we migrate Data Services to v4.
            1. PR - So there are choices to be made between the way Core GeoNetwork provides a function and the way our Data Services provides the same or similar.
            2. LM - So we can change Data Services to use the Core GeoNetwork function or we write our own.
        8. BS - Do we still need subscription, or do we migrate to web services?
            1. RGb - You would have to change the WMO Technical Specifications.
            2. JT - Yes, that's WIS 2.0 and we will have to support _push_.
            3. NM - Probably need to subscribe to notifications that data is ready.
            4. WQ - Yes, people will have to subscribe somehow; email, web services etc. are all just delivery mechanism. I think we will still have subscriptions in WIS 2.0.
        9. PR - So, the schedule I had in mind for v4 was 2 main Releases over the next 12 months:
            1. PR - A development release, v4.1, in September 2017. The objective of this is to check we are making good progress on the main features.
            2. PR - A stable production release, v4.2, in January 2018, so that we can prepare the deployment package and documentation etc. by March 2018.
            3. PR - We will be using the agile approach, so only those features that are ready on time will make it into the release.
            4. JT - What about the parallel v5 pilots?
            5. PR - We could decide on a case by case basis whether we think any of them are candidates for inclusion in a v4 release, otherwise they're stand-alone pilots.
8. **OpenWIS Lifecycle**
    1. Features and Squads and how they will work in practice
        1. PR presented [lifecycle]({{ site.baseurl | prepend: site.url }}/howto/2017-03-17-OpenWIS-Development-Process.html)
        2. PR presented [features and squads]({{ site.baseurl | prepend: site.url }}/howto/2017-03-17-OpenWIS-Features-and-Squads.html)
            1. NM - So it's not pair-programming as I understand it?
            2. PR - Correct, it's not true pair-programming as practised in eXtreme Programming, where 2 programmers look at one screen and work through the coding together; obviously, we can't do that because the squad members are not often together. But we can get some of the knowledge sharing and code-quality benefits by working in pairs as best we can. I think this will be particularly helpful in embedding the Overlay approach.
9. **Planning workshop**
    1. PR - The purpose of this workshop is to agree what priorities we want to assign to OpenWISv4 development activities, for Release 4.2, and by implication, Release 4.1. If we get time, we'll have a look at the OpenWISv3 maintenance backlog and the documentation backlog too.
    2. PR presented [Workshop instructions]({{ site.baseurl | prepend: site.url }}/howto/2017-03-17-OpenWIS-Planning-Workshop.html)
    3. PR - So for round 1, we're looking at the issues in:
        - [github issues: OpenWIS4](https://github.com/OpenWIS/openwis4/issues)
    4. PR - You can add new issues, but you should check they're not logged somewhere already:
        - [kanban board](http://openwis.github.io/openwis-documentation/kanban/)
        - [backlog](http://openwis.github.io/openwis-documentation/backlog/)
        - [github issues: OpenWIS3](https://github.com/OpenWIS/openwis/issues)
        - [github issues: openwis-documentation](https://github.com/OpenWIS/openwis-documentation/issues)
    5. PR - The teams are:
        1. Pink: BR, BS, MV, PR
        2. Blue: KS, NM, RGb, YG
        3. Green: DW, MF, MG, MC
        4. Yellow: DP, MP, SO, SD
    6. PR - Some of you have a remote team member on WebEx, so you will need to figure out how to include them; this is something we will have to do when we work in squads.
    7. {Each team worked independently on the round 1 task and then the post-its were collected by PR}
    8. The results were:
        1. Pink:
            - +2: [#107](https://github.com/OpenWIS/openwis4/issues/107)
            - +2: [#58](https://github.com/OpenWIS/openwis4/issues/58)
            - +1: [#74](https://github.com/OpenWIS/openwis4/issues/74)
            - +1: [#72](https://github.com/OpenWIS/openwis4/issues/72)
            - +1: [#42](https://github.com/OpenWIS/openwis4/issues/42)
            - +1: [#20](https://github.com/OpenWIS/openwis4/issues/20)
            - +1: [#14](https://github.com/OpenWIS/openwis4/issues/14)
            - +1: [#8](https://github.com/OpenWIS/openwis4/issues/8)
        2. Blue:
            - +1: [#103](https://github.com/OpenWIS/openwis4/issues/103)
            - +1: [#94](https://github.com/OpenWIS/openwis4/issues/94)
            - +1: [#90](https://github.com/OpenWIS/openwis4/issues/90)
            - +1: [#89](https://github.com/OpenWIS/openwis4/issues/89)
            - +1: [#85](https://github.com/OpenWIS/openwis4/issues/85)
            - +1: [#84](https://github.com/OpenWIS/openwis4/issues/84)
            - +1: [#83](https://github.com/OpenWIS/openwis4/issues/83)
            - +1: [#54](https://github.com/OpenWIS/openwis4/issues/54)
            - +1: [#40](https://github.com/OpenWIS/openwis4/issues/40)
            - +1: [#18](https://github.com/OpenWIS/openwis4/issues/18)
        3. Green:
            - +2: [#73](https://github.com/OpenWIS/openwis4/issues/73)
            - +2: [#71](https://github.com/OpenWIS/openwis4/issues/71)
            - +2: [#70](https://github.com/OpenWIS/openwis4/issues/70)
            - +2: [#50](https://github.com/OpenWIS/openwis4/issues/50)
            - +2: [#29](https://github.com/OpenWIS/openwis4/issues/29)
        4. Yellow:
            - +2: [#103](https://github.com/OpenWIS/openwis4/issues/103)
            - +2: [#99](https://github.com/OpenWIS/openwis4/issues/99)
            - +1: [#84](https://github.com/OpenWIS/openwis4/issues/84)
            - +1: [#82](https://github.com/OpenWIS/openwis4/issues/82)
            - +1: [#73](https://github.com/OpenWIS/openwis4/issues/73)
            - +1: [#72](https://github.com/OpenWIS/openwis4/issues/72)
            - +1: [#18](https://github.com/OpenWIS/openwis4/issues/18)
            - +1: [#10](https://github.com/OpenWIS/openwis4/issues/10)
    9. PR - Ok, so looking at the results together, we have 11 issues that scored more than 1.
        1. PR - That seems like an achievable number of changes to be considering for a release; around a dozen would be 3 changes per squad on average. Could we just say that those 11 are the MUSTs, so they represent the MVP for the release?
        2. SO - That sounds reasonable.
        3. PR - Ok.
        4. PR - Because BoM couldn't be with us this afternoon, LM is sending their votes by email, so I will add those in, but they won't alter the numbers by much.
            1. _Post meeting note_: BoM voted as follows, which resulted in 13 MUSTs:
                - +3: [#58](https://github.com/OpenWIS/openwis4/issues/58)
                - +2: [#72](https://github.com/OpenWIS/openwis4/issues/72)
                - +2: [#45](https://github.com/OpenWIS/openwis4/issues/45)
                - +1: [#70](https://github.com/OpenWIS/openwis4/issues/70)
                - +1: [#54](https://github.com/OpenWIS/openwis4/issues/54)
                - +1: [#48](https://github.com/OpenWIS/openwis4/issues/48)
        5. PR - OK, I will take an action to label the issues list on GitHub with the priorities we have agreed.
            1. So more than 1 vote is a MUST, 1 vote only is a SHOULD, 0 votes is a COULD.
            2. PR - [Action-TC-2017-15 Add priority labels to openwis4 issues](https://github.com/OpenWIS/openwis-documentation/issues/165)
    10. PR - Ok, we're short of time, so I suggest we do the other backlogs offline if required.  They have far fewer issues and we could probably just cover them during a TC meeting.
10. **Allocation of people to squads to features**
    1. PR - I think we need to deliver some Overlay training and see how that goes before we can assign people and features to squads. I am happy to take actions to follow that up at the appropriate time.
        - PR - [Action-TC-2017-16 Feature squads](https://github.com/OpenWIS/openwis-documentation/issues/166)
        - PR - [Action-TC-2017-17 Feature backlogs](https://github.com/OpenWIS/openwis-documentation/issues/167)
    2. PR - However, it would be interesting to see who is interested in each feature, just to give an idea of the spread; I will not be using the responses to allocate work. Shall we go round the table?
        1. The responses were:
            - 7 interested in Discovery: NM, PR, KS, JT, SO, SD, DP
            - 2 interested in Access: RGb, YG
            - 5 interested in Retrieval: MP, MV, DW, MF, MC
            - 3 interested in System Admin: MG, BR, BS
        2. PR - That's probably the sort of distribution we will need, with more focus on the things the end-users are most concerned about, Discovery and Retrieval.
    3. PR - Ok, I will think about how best to structure the backlog/Kanban etc. for the work ahead and take actions to update them as required.
        - PR - [Action-TC-2017-18 Update the Kanban](https://github.com/OpenWIS/openwis-documentation/issues/168)
        - PR - [Action-TC-2017-19 Update the Backlog](https://github.com/OpenWIS/openwis-documentation/issues/169)
11. **Development facilities for OpenWIS4**
    1. Status of MF servers - are they useful and should we keep them?
        1. MC - We have 6 months subscription remaining for the servers. We recently used them for the Forum demos.
        2. JT - What's the running cost of the servers?
        3. MC - 70 Euros per month per server.
        4. NM - What's the purpose of this infrastructure? What happens after 6 months?
        5. BS - They could be paid for by OpenWIS Association?
        6. MC - They can be used for whatever we want. They are 2 physical servers with the Proxmox VM installed.
        7. NM - What memory do they have?
        8. BS - 32Gb.
        9. SO - How easy is it to create new accounts and support development?
        10. MC - Quite easy, MF agreed at the Developer Conference in Washington to support development on them.
        11. NM - So we could move the public servers at European Dynamics there?
        12. MC- Yes.
        13. MC - We use the nginx proxy to authorise http connections. We direct according to url, to the dedicated VM we have set up for you.
    2. SO - Where do we envisage Discourse is deployed operationally?
        1. NM - For long term use, I would look at a cloud provider. We had to assign 16Gb to Core GeoNetwork v3.2, which is half of the 32Gb. Rather we put things on cloud so we can uplift memory etc. as things grow. Also, we would be doing less system admin.
        2. MG - There are several options for various containers or commercial offerings for running Discourse.
        3. SO - Rough cost?
        4. MG - No idea, but I'm sure there are some low-end tiers.
        5. SO - Could you get us a table of cost options?
        6. MG - Sure.
            - MG - [Action-TC-2017-09 Costed options for Discourse](https://github.com/OpenWIS/openwis-documentation/issues/159)
        7. JT - Shall we try it for 6 months?
        8. PR - I suggest a year to give it a good run. Anyway we only really discuss costs at the annual meetings.
        9. JT - Ok, we'll recommend SC budget for a year of Discourse.
        10. JT - Someone should ask the question: how do we get our forum data out of Discourse if we change our minds after one year?
        12. KS - It's standard in US contracts to require that.
        11. MG - Ok, I can do that too.
            - MG - [Action-TC-2017-10 Establish how we could get off Discourse](https://github.com/OpenWIS/openwis-documentation/issues/160)
        12. RGb - Is the Forum only for developers, or for end-users?
        13. JT - Both. I'm just looking for the address of a well used Discourse instance...
            1. JT - Try looking at: [W3C Web Incubator Group](https://discourse.wicg.io/)
            2. JT - Also, if you go up one level to [here](https://wicg.io/), you will see a choice between GitHub and Discourse.
            3. RGb - Should developers discuss on Discourse?
            4. PR - Developers should mainly use GitHub for discussion of issues or detailed technical work that is in progress (limited audience). New ideas, theories etc. should be discussed initially on Discourse (wider audience).
    3. Status of AWS CI - is it still useful and should we repurpose it for v4?
        1. PR - AWS CI is currently in use for OpenWISv3.14 builds and we still need that throughout maintenance mode.
        2. NM - We also need to build CI for OpenWIS4. AWS is ok, so no need to change to something else.
        3. JT - So budget to continue the existing spend of about 2000 USD per year?
        4. NM - Well, we need to build another for v4 and nice to know quickly when something is broken, so should also run continuously, so probably cost more.
        5. MF - At present we are running: 1 large, 3 medium and 3 micro services.
        6. JT - NM, perhaps you could take a look at our current usage and decide what we might end up using?
        7. PR - The UKMO Release Engineering team will be able to say what we run on it. We probably used it more when we were in the thick of v3.14 uplift.
        6. NM - Ok, I'll speak to Release Engineering and look at how it is being used.
            - NM - [Action-TC-2017-11 Future use of the CI environment](https://github.com/OpenWIS/openwis-documentation/issues/161)
    4. RGb - Do we want to redirect openwis.io?
        1. PR - Yes, once Discourse is operational.
12. **excel2wis**
    1. BS presented [excel2wis](https://github.com/OpenWIS/excel2wis)
         1. MC - We have submitted the pull-request. How do we get it approved?
         2. PR - You can approve your own pull-request into the _develop_ branch - you know the code best.
         3. PR - Then the Release Engineering team will merge to _master_; I will arrange that with them if you like.
         4. DW - How does it handle updates to metadata?
         5. BS - We run some Javascript to copy out the original metadata to a CSV file, then import it into Excel and edit it.
         6. MC - I have just merged back to _develop_.
         7. PR - Ok - [Action-TC-2017-12 Merge excel2wis to master](https://github.com/OpenWIS/openwis-documentation/issues/162)
         8. SO - I suggest we incorporate a 'new project' page for excel2wis on the website.
         9. JT - So, you need to make that recommendation to the SC.
         10. BS - I will prepare a summary and send it to CS, to put on the website.
             - BS - [Action-TC-2017-13 Project summary for excel2wis](https://github.com/OpenWIS/openwis-documentation/issues/163)
13. **Metadata hierarchies**
    1. DW - To save time, I won't say much more on this now; we've covered it a few times already. We all know we need better metadata hierarchies, to make it easier to find and manage metadata as well as to improve subscriptions.
14. **WIS 2.0**
    1. WIS 2.0 Status Update
        1. JT - The initial presentation on the need for WIS 2.0 was made at WMO CBS in November 2016.   It was recommended.
            - [WIS 2.0 proposal - WORD]({{ site.baseurl | prepend: site.url }}/assets/CBS-16-d05-5-1-DEVELOPMENT-OF-WIS-draft1_en.docx)
            - [WIS 2.0 proposal - PDF ]({{ site.baseurl | prepend: site.url }}/assets/CBS-16-d05-5-1-DEVELOPMENT-OF-WIS-draft1_en.pdf)
        2. JT - So, we are hoping for approval at the WMO Executive Council meeting in May 2017.
        3. JT - WIS 2.0 is a fundamentally different proposition to WIS 1.0. WIS 1.0 didn't extend the reach or availability of weather data. WIS 2.0 does involve a fair amount of change and we expected challenges, but it was well supported by lots of people who have similar concerns about increasing data volumes etc.
        4. JT - We have asked WMO Secretariat to employ a full-time project manager to get the WIS 2.0 programme up and running. However, we're not sure if we'll get the spend prioritized from June.
    2. OpenWIS Association strategy for WIS 2.0
        1. JT - So for the rest of this discussion, I'll assume the WIS 2.0 project manager is approved.
        2. JT - That project manager would support TT-EWIS; the chair is Bob Bunge and vice chair is me (JT).  BR is also involved. The task team role is to establish an implementation plan.
        3. JT - This plan would need to be founded on reality, which means we need to show that the technology works and delivers value. I estimate that the draft Technical Specifications will take 24 months to develop. During that time the community needs to validate ideas so that the Technical Specifications will be truly implementable.
        4. JT - BR, do you think 2 years is achievable?
        5. BR - Yes, based on the experience of the last time (1.0 Specifications), I would say so.
        6. JT - There was a lot of prior knowledge last time about how to implement. We will need more outreach this time, to find out what people are doing with cloud etc. There will be overlaps, for example with Copernicus.
        7. JT - So I would expect the proposal to be put before CBS in 2020.
        8. JT - I would want to see the Association doing pilots in the meantime to show that the Technical Specifications can be implemented.
        9. JT - We need a significant rethink about how metadata is structured.
        10. BR - Yes, metadata is for people, not for computers; people can't use half a million metadata records!
        11. JT - From the UKMO perspective, we have a major programme running, _Transform & Efficiency_, that is looking at the adoption of cloud, message driven architectures etc. We're expecting proposals by October 2017 and we will share that.
        12. Anyone else got relevant projects running in the next 12 months?
        13. WQ - Yes, at BoM we have a proposal for a 5 year programme to reengineer our main infrastructure:
            - Security (2017-2018)
            - MSS including WIS (2017-2019)
            - Forecasting apps etc (2019-2021)
        14. JT - So it would be useful to BoM to understand what OpenWISv5 looks like.
        15. WQ - Yes. We are already using a messaging backbone, in pockets; what is missing is an enterprise approach to a message-based architecture. Someone has to demonstrate the capabilities.
        16. SO - Within NOAA we have a number of activities, but I don't think they influence these timelines here.
        17. KS - One-stop discovery and data-shopping is something I want to promote.
        18. JT - In WIS 2.0 we will implement general patterns for data discovery and sharing that will be useful for way more than GTS etc.
        19. BS - In MF we are still working on INSPIRE. We are working on OGC web services for access to climatology and other data. The future now is to offer web services and not to push data. This is the main project around WIS in MF. We will be using enterprise-bus services to build a web services catalog. We can show a presentation later on.  Also work on our DCPCs: VAAC, Radar, Long-range forecasts, Cyclone (by the Summer). We are also involved in Copernicus and waiting for OpenWIS4.
        20. BR - At ECMWF we are looking into cloud, especially how we deliver our forecasts into cloud. And Copernicus, with EUMETSAT.
        21. WQ - What's Copernicus?
        22. JT - Earth monitoring; various satellite data services.
        23. BR - ECMWF are doing the Climate Change and Atmospheric Monitoring. We redistribute the work tenders.
        24. [Copernicus](http://www.eumetsat.int/website/home/AboutUs/InternationalCooperation/Copernicus/index.html)
        25. SD - At KMA we are not planning any OpenWIS activities this year, but we have another Harness project. We don't know what data is going out of OpenWIS, or how much, so we are deploying monitoring.
        26. RGb - At MFI we are developing the Assisi solution. We are using OpenWIS as a module to deliver data to end users. We have a dedicated Harness for long-range forecasts etc. We have one data centre for Climate and one for Satellite and Radar imagery. We have plugged these into WIS.
        27. MV - At FMI we have nothing planned that is directly related to WIS. We are mainly working on our open data portal, based on OGC services and our Smartmet server. We want Smartmet to be our backend for OpenWIS.
        28. MV - We are also working on Copernicus, where we use Smartmet server and GeoNetwork already. We could perhaps use OpenWIS.
        29. SO - Kari and I discussed a couple of aspects with Fred Branski and Bill Bolhofer:
            1. How important is it to show linkage to other WMO programmes?
            2. How important is the use of emerging data formats such as JSON and GeoJSON?
        30. JT - So both are very important, as explained in section 4.1 of the proposal to CBS:
            - [WIS 2.0 proposal - WORD]({{ site.baseurl | prepend: site.url }}/assets/CBS-16-d05-5-1-DEVELOPMENT-OF-WIS-draft1_en.docx)
            - [WIS 2.0 proposal - PDF ]({{ site.baseurl | prepend: site.url }}/assets/CBS-16-d05-5-1-DEVELOPMENT-OF-WIS-draft1_en.pdf)
        31. WQ - Ok, this is all good; but let's not take another decade!
        32. JT - So we can expect the Technical Specifications to be finally approved in 4 years time; that gives us time to do this properly and be ready for that approval.
15. **AOB**
    1. YG presented [MF OpenWIS Operations]({{ site.baseurl | prepend: site.url }}/assets/2017_MF_OpenWIS_Deployments_YGO_vAnim_20170317.odp) (first part of slide-deck).
    2. BS presented [MF OpenWIS Deployments]({{ site.baseurl | prepend: site.url }}/assets/2017_MF_OpenWIS_Deployments_YGO_vAnim_20170317.odp) (second part of slide-deck)
        1. BS - The enterprise service bus (ESB) is the backbone of our system architecture.
        2. BS - DCPC data services access at MF is based on a Service Oriented Architecture.
        3. SD - Is the ESB around OpenWIS?
        4. BS - The ESB is not part of OpenWIS, it's in front of the data.
        5. SD - So data policy is separate?
        6. BS - It is linked.
        7. BS - All the software is open source, Docker solutions.
        8. BS - We have only one main entrance for users. We monitor all use of web services, preventing each system from doing its own monitoring.
    3. MC presented [MF OpenWIS Harness]({{ site.baseurl | prepend: site.url }}/assets/2017-MF-Harness-v3-20170319.odp)
        1. MC - Should we make the Harness code open source and share experiences of implementation and deployment?
        2. DW - How does dissemination work? Does the Harness deliver the data?
        3. YG - We install the Harness on the NWP DCPC etc. It produces an XML file that specifies a non-OpenWIS location.
        4. RGb - OpenWIS is very specific to the data source. Is yours more generic?
        5. MC - The harness indicates our own SOAP web service, so is specific.
        6. BR - So an adapter pattern model?
        7. MC - Yes. So that means we could share some components.
        8. PR - Ok, I'll arrange for a new Repository and then you can start us off by adding your Harness code.
            - PR/MC - [Action-TC-2017-14 Share Harness components](https://github.com/OpenWIS/openwis-documentation/issues/164)
16. **Meeting Summary** (SO)
    1. LM gave us a retrospective on the last year:
        1. It's been a good year with the release of a stable v3.14
        2. And we have gone open source.
    2. LM also shared the results of an online survey. It was notable that:
        1. Most GISCs are running v3.12 or v3.13
        2. The hardest part of v3.14 to install was OpenAM/DJ
        3. Most installs took days rather than hours
        4. Two centres have used puppet to get installs down to 2 hours.
    3. We heard from NM about the progress with v4:
        1. We have a v4.0 instance running
        2. We have developed the Overlay approach to make development of v4 easier
        3. We're looking at training 10-12 folks in multiple sessions
        4. After that we'll assess whether to hold a Developer Conference.
    4. DW has briefed us on the capabilities of Core GeoNetwork, relative to OpenWIS4:
        1. There is a lot of work to do and in progress
        2. We've discussed parent/child metadata
        3. And the compliance of OpenWIS4 to WIS Technical Specifications
        4. We need a set of tests to show compliance.
    5. We discussed engagement with external communities:
        1. The Core GeoNetwork community
        2. External contributors
        3. And we distinguished between major and minor contributions
        4. Also, we intend to look at how other small open source organisations work.
    8. We compared the options for forum software and we chose Discourse.
    9. We have discussed what the balance of the work should be between v4 vs v5.
    10. We anticipate that we will Release a v4.1 and a v4.2 during the next year
    11. We have discussed a squad and feature based approach to future development and aim to assign work at the next TC.
    12. We have discussed the facilities we need and the financial implications.
    13. We have decided to adopt excel2wis into the Association and to create a shared repository for harness components.
    12. We have also heard about the future, in the shape of WIS 2.0.

---

#### Participants
- SO - Steve Olson, National Weather Service, United States of America [NWS], [delegate], Chair
- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM], [delegate], (WebEx) (mornings only)
- SD - Sungsoo Do, Korea Meteorological Administration, Republic of Korea [KMA], [delegate]
- MC - Michael Claudon, Meteo-France, France [MF], [delegate]
- RGb - Remy Gibault, Meteo-France International [MFI], [delegate]
- MP - Mikko Partio, Finnish Meteorological Institute [FMI], [delegate]
- JT - Jeremy Tandy, Met Office, UK [UKMO], [delegate] (day two only)
- KS - Kari Sheets, National Weather Service, United States of America [NWS]
- MG - Marc Giannoni, National Weather Service, United States of America [NWS], (WebEx)
- CS - Cassie Stearns, National Weather Service, United States of America [NWS] (WebEx) (parts)
- LM - Leon Mika, Bureau of Meteorology, Australia [BoM], (WebEx) (mornings only)
- BS - Benjamin Saclier, Meteo-France, France [MF]
- YG - Yves Goupil, Meteo-France, France [MF]
- JMD - Jean Marie Dumas, Meteo-France, France [MF] (observer)
- MV - Mikko Visa, Finnish Meteorological Institute [FMI]
- BR - Baudouin Raoult, European Centre for Medium Range Weather Forecasting [ECMWF]
- PR - Paul Rogers, Met Office, UK [UKMO]
- MF - Mark Francis, Met Office, UK [UKMO]
- DW - Dominic Woollatt, Met Office, UK [UKMO]
- NM - Nassos Michas, European Dynamics, [UKMO]
- GT - Giorgios Triantafyllidis, European Dynamics, [UKMO], (WebEx)
- NM - Dimitris Papadeas, European Dynamics, [UKMO], (WebEx)
