---
layout: page
title: Minutes - OpenWIS Technical Committee 2017 March - Toulouse
---

#### 20th - 21st March 2017

---

1. **Welcome and introductions**
    - SO - Welcome everybody.
2. **Approval of agenda**
    - SO - The agenda is approved.
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
            4. Are there any compatibility issues with the Overlay approach?
                1. NM - As long as the plug-in places don't change we don't have any compatibility issues.  If they removed a major feature, say the entire Admin Menu, then our code would break and we would have to fix it. But, we would only have to fix that part.  We are as independent as it is possible to be.
        3. NM presented: [Skills and training]({{ site.baseurl | prepend: site.url }}/assets/TC201703-Skills-and-training.pdf) - how will we transfer skills in the Overlay Approach?
            1. NM - So its a mixture of skills; there is some legacy technology left hanging around in CGN as well as some newer technology.  This is expected of a 10 year old project.  A lot of it is XML based.
                1. SO - What schemas are supported out of the box?
                2. NM - This XML refers to component configuration rather than for metadata. Wro4j also uses XML.
                3. SO - Is there support to change that through plug-ins?
                4. NM - No need to do that, just change the XML.
            2. NM - We have made plug-in examples of all the components we could think of; there may be a few others.
            3. RGr - Is it possible to disable SSO?
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
            2. PR - Ok, what we thought is that we could do some WebEx training first, so that GT can take small groups through the approach and get people started.  Then later, if further consolidation is required, we could arrange a Developer Conference.
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
                1. PR - The repository is public: https://github.com/geonetwork/core-geonetwork
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
        1. NM - [OpenWIS5]({{ site.baseurl | prepend: site.url }}/assets/TC201703-OpenWIS5.pdf); including pros and cons of v4 vs v5 and description/demo of the advanced MQ PoC
    2. **Release roadmap**
        1. PR - for at least next 12 months - schedule releases 4.1 and 4.2
8. **OpenWIS Lifecycle**
    1. PR - 'features' and 'squads' and how they will work in practice ([lifecycle]({{ site.baseurl | prepend: site.url }}/howto/2017-03-17-OpenWIS-Development-Process.html)) / ([features and squads]({{ site.baseurl | prepend: site.url }}/howto/2017-03-17-OpenWIS-Features-and-Squads.html))
9. **Planning workshop**
    - [Workshop instructions]({{ site.baseurl | prepend: site.url }}/howto/2017-03-17-OpenWIS-Planning-Workshop.html)
    - [kanban board](http://openwis.github.io/openwis-documentation/kanban/)
    - [backlog](http://openwis.github.io/openwis-documentation/backlog/)
    - [github issues: OpenWIS4](https://github.com/OpenWIS/openwis4/issues)
    - [github issues: OpenWIS3](https://github.com/OpenWIS/openwis/issues)
    - [github issues: openwis-documentation](https://github.com/OpenWIS/openwis-documentation/issues)
    - We will go through the kanban/backlog items and agree the following:
        - the definition and priority (MSCW) of each kanban/backlog item
        - which kanban/backlog items belong to which Features
        - which Features are candidates for releases 4.1 and 4.2
    - this will include work on the website and docs as well as the code (they are all on the kanban)
    - PR will add any new ideas to the backlog, preferably before the meeting, but can do during as well
    - new backlog items can just refer to an issue on GitHub, otherwise, a brief description would be useful for PR to publish on the website prior to the meeting (for example, the MF/INSPIRE question on the metadata query performance of OpenWIS v3 should be raised as a GitHub issue)
10.  **Allocation of people to squads to features**
    1. PR - work allocation:
        - establish who is interested in each feature
        - build squads accordingly
        - firm up on lists of Features for upcoming releases (eg: 3.14.9 and 4.1)
11. **Development facilities for OpenWIS4**
    1. MC - status of MF servers - are they useful and should we keep them?
    2. XX - status of AWS CI - is it still useful and should we repurpose it for v4?
12. **excel2wis**
    1. MC - Metadata tool [excel2wis](https://github.com/OpenWIS/excel2wis)
13. **Metadata hierarchies**
    1. DW - Why we need metadata hierarchies
14. **WIS 2.0**
    1. JT - WIS 2.0 Status Update
15. **AOB**
16. **Summary for SC**

---

#### Participants
- SO - Steve Olson, National Weather Service, United States of America [NWS], [delegate], Chair
- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM], [delegate], (WebEx)
- SD - Sungsoo Do, Korea Meteorological Administration, Republic of Korea [KMA], [delegate]
- MC - Michael Claudon, Meteo-France, France [MF], [delegate]
- RGb - Remy Gibault, Meteo-France International [MFI], [delegate]
- MP - Mikko Partio, Finnish Meteorological Institute [FMI], [delegate]
- JT - Jeremy Tandy, Met Office, UK [UKMO], [delegate]
- KS - Kari Sheets, National Weather Service, United States of America [NWS]
- MG - Marc Giannoni, National Weather Service, United States of America [NWS], (WebEx)
- CS - Cassie Stearns, National Weather Service, United States of America [NWS] (WebEx)
- LM - Leon Mika, Bureau of Meteorology, Australia [BoM], (WebEx)
- BS - Benjamin Saclier, Meteo-France, France [MF]
- YG - Yves Goupil, Meteo-France, France [MF]
- JMD - Jean Marie Dumas, Meteo-France, France [MF]
- RGr - Remy Giraud, Meteo-France, France [MF]
- MV - Mikko Visa, Finnish Meteorological Institute [FMI]
- BR - Baudouin Raoult, European Centre for Medium Range Weather Forecasting [ECMWF]
- PR - Paul Rogers, Met Office, UK [UKMO]
- MF - Mark Francis, Met Office, UK [UKMO]
- DW - Dominic Woollatt, Met Office, UK [UKMO]
- NM - Nassos Michas, European Dynamics, [UKMO]
- GT - Giorgios Triantafyllidis, European Dynamics, [UKMO], (WebEx)
- NM - Dimitris Papadeas, European Dynamics, [UKMO], (WebEx)
