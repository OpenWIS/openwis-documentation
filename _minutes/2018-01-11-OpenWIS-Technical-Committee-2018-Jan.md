---
layout: page
title: OpenWIS Technical Committee 2018 January
---

#### 12:00 UTC 11th January 2018

---

1. **Welcome**
    1. SO - Welcome everybody.
    2. Firstly, I would like to congratulate BS on his election to TC Vice-chair and thank him for agreeing to contribute.
2. **CBS TECO Demo**
    1. Updates/demo from [European Dynamics](http://www.eurodyn.com/) on pilot progress and next steps.
        1. NM - So, we have been working on a pilot project to explore possible aspects of the future WIS 2.0.
        2. NM - The pilot we are building has a Local Data Sharing Hub (LDSH), where the data sets are initially published by the data owner; a Regional Data Sharing Hub (RDSH), which collates data sets from the LDSHs; and an Authoritative WIS Catalogue (AWISC), which is where official WIS data sets are registered.
        3. NM - The LDSH collects local measurements. It connects to the RDSH to create message queues. Users of the data sets can subscribe to the queues at the RDSH.
        4. NM - When the data set is deployed at the LDSH a web page is automatically created that contains structured metadata for search engine crawlers such as Google and Yahoo! etc.
        5. NM - The AWISC is also a search engine that indexes the RDSHs only and gives a richer search experience than Google etc, because it understands the RDSH metadata.
        6. NM - The goal is to have the demo ready about 2 weeks before the TECO meeting.
        7. NM - We have created mock-ups, more than mock-ups really, with routing and other processing included, to demo what we are building.
        8. GT - So I will first show the LDSH (demo via shared screen).
        9. NM - So we have been working to a narrative provided by JT. The narrative describes who works at each Hub, using the names of fictional users of the system; 'Mouktar' operates the LDSH.
        10. GT - So I am Mouktar, on the LDSH, where I will be configuring data sets for my location. This is a public page where you can see what the LDSH is providing. For the PoC the datasets are in CSV format. Also here is the queue users of the data set can subscribe to, if allowed by Mouktar. All this info is provided by Mouktar.
        11. BS - Is the metadata coming from the WIS catalogue?
        12. GT - So this page is listing the registered data sets. Mouktar adds the metadata for the datasets himself, using a format we defined just for the PoC. So Mouktar can give us a data set name, description, period etc; what you saw earlier.
        13. GT - There is a UI where Mouktar can put this info; these codes for weather types we have used here are from the WMO site. This is what will be searched by the AWISC. So, if you search for 'rain' for Djibouti then you will find Mouktar's page in your search results.
        14. GT - So here we can see the download URL and the subscription URI and how Moultar creates them.
        15. NM - And here Mouktar provides the metadata and uploads the actual data.
        16. GT - This filename gives the prefix for the files Mouktar will upload.
        17. GT - If Mouktar wants he can also here enable the RDSH dissemination, either a notification or the data itself. If Mouktar enables subscriptions then the data set users will be able to see this URI.
        18. GT - The search engine metadata is added here on the metadata page.
        19. NM - We are using open text for now.
        20. BS - Would I be able to download a data set from yesterday?
        21. GT - For the PoC, we can only download the last data set.
        22. NM - There is an option to keep a queue history, so we could do that; get data for, say, the last 10 days.
        23. GT - Here on the registered data sets page there is an Add button and a View data set info button.
        24. GT - So as we said, dissemination is done through the RDSH, so every LDSH will be connected to one RDSH that manages it's queues.
        25. GT - So here is the RDSH. 'Omar' is the administrator of the RDSH, which has a set of LDSHs and the info on them. Here is where Omar adds the LDSH. Mouktar says he wants to disseminate via this RDSH and so Omar gives Mouktar a token, say via email. Mouktar will put the token into his LDSH and then his LDSH will be registered with Omar's RDSH. Now, Mouktar can add and delete queues etc.
        26. NM - For the PoC we are showing the minimum amount of admin - a real system will need security and permissions etc.
        27. GT - Yes, the focus here is on a simple demo.
        28. GT - Once Mouktar's LDSH is registered, other Mouktar data sets can be automatically published by Omar's RDSH.
        29. GT - The AWISC is where the authoritative datasets are registered. So if Mouktar is a partner of WMO he will be registered here so that Users can find the official data for Djibouti etc.
        30. GT - Mouktar will put a token into his LDSH and then every dataset that Mouktar publishes is registered within the AWISC in order to be searched for. So, the AWISC will show Mouktar's datasets in the search results, along with the metadata Mouktar provided. So, Users can get a lot of useful information about the data to help them decide whether they want to subscribe to it.
        31. GT - At the AWISC, Users who understand WMO codes can use them to do intelligent searching. There is not just one vocabulary of WMO codes, but many different ones for different weather types. This intelligent searching would be done here through the advanced search interface.
        32. GT - And here we have the setting page, where you can see the contact info etc.
        33. GT - This is the page where the queues are managed. There are queue statistics and graphs of the traffic.
        34. SO - Do we envision using static queues for the messages?
        35. NM - The queue creation is dynamic; when you register on the LDSH, a new queue is created on the RDSH.
    2. Questions to resolve:
        1. Should we set a deadline for development of Demo pieces and then focus on the messaging aspects going into CBS?
            1. SO - When do we need the demo ready?
            2. NM - It should be ready by 13th March 2018.
        2. Should we develop a poster and/or presentation video to accompany the demo?  If so, we need to discuss what that consists of.
            1. SO - What additional preparation do we need?
            2. PR - I've spoken to JT about what else we might need. He said there is a CBS TECO planning meeting next week in Geneva. JT will attend that meeting, so we can get feedback from him on the general expectations for the TECO demo and anything additional we require for the CBS TECO. I'll arrange a discussion on that and any support required, for when JT is back.
                - PR - [Action-TC-2018-01 Ask JT to provide feedback on TECO arrangements to TC](https://github.com/OpenWIS/openwis-documentation/issues/356)
            3. Who do we envision going to demo?
                1. PR - It is likely that JT will attend the CBS TECO and do the demo within the narrative we have developed.
2.  **OpenWIS Roadmap**
    1. One of the actions items from the Steering Committee is to report back on an OpenWIS roadmap by CBS TECO.  Some of the important roadmap pieces to consider are:
        1. How long to support OpenWIS 3 and in what capacity?
        2. The evolution of PoC demo.  What pieces we see remaining in tech design, and what gets thrown out
        3. Prioritization of first new OpenWIS modular build.  What goes in the initial release?  What goes in the second?  And so on and so forth?
        4. What's the schedule for these builds?
        5. What are the benefits of the new modular builds to end users?  What are the benefits of the new modular builds to the operational centers running the software?
    2. SO - So we need to report back to SC with a roadmap by the time of the CBS TECO demo.
    3. PR - Ok, but it's just a high level roadmap to provide context for the WIS 2.0 work we'll be discussing at TECO. We'll be able to add to it when we see what else is going on in the community and get feedback on our demo.
    4. SO - What I would also like to do is schedule in some time for development of the roadmap at the Annual Meeting in Finland. Do we know yet when the meeting is scheduled for?
    5. PR - Just that it will be in April, no specific dates.
    6. PR - I have an action from the last Annual Meeting to propose a new meeting structure in which PMC and TC meetings are distinct.
    7. SO - I also was wondering if we might run the Developer Conference in parallel?
    8. PR - It's not really the same people involved and we all have constraints on how many people we can send away at once.
    9. PR - I agree it would be a good time to run a roadmap workshop. Though the PMC and TC meetings should be distinct, we could have a joint session on the roadmap. Not sure what facilities FMI expect to provide, for example, break-out rooms.
    10. SO - Yes, we should set aside some time to consider the feedback from TECO.
    11. PR - In the meantime, we just need a skeleton roadmap to support the narrative at TECO.
    12. DW - A brainstorming session at the Annual Meeting would be good.
    13. PR - Ok, I'll include a joint roadmap session in my proposals for the meeting schedule and check with FMI what the dates and facilities are.
        - PR [Action-TC-2018-02 Inc a combined TC/PMC brainstorm session in Annual Meeting agenda](https://github.com/OpenWIS/openwis-documentation/issues/357)
        - PR - [Action-TC-2018-03 Check arrangements for Annual Meeting](https://github.com/OpenWIS/openwis-documentation/issues/358)
3. **Name for new OpenWIS**
    1. What is the name for this new modular future OpenWIS build?  Should we create a doodle poll once we have a number of potential names and let TC members decide?
    2. SO - Be good to know what we're calling the software by the TECO meeting.
    3. SO - BS, would you be able to poll for names?
    4. BS - OK, yes.
        - BS - [Action-TC-2018-04 Run a poll on a name for the new OpenWIS-Core software](https://github.com/OpenWIS/openwis-documentation/issues/359)
4. **OpenWISv3**
    1. Recent improvements to support Java 8, etc. (Marc/Zhang discussion, Eurodyn on inclusion into CI)
    2. Discussion on the prioritization of other OpenWIS 3 things to fix?
    3. SO - What are the priorities for OpwnWISv3?
    4. DW - Now in maintenance mode, so just make sure it is patchable, only make improvements if needed.
    5. PR - Security maintenance activities should be on the roadmap. Otherwise, we have an Issues Backlog; people can fix bugs from the backlog if they have the time and resources.
    6. DW - But bear in mind that I'm still waiting for test systems here to test the new release. It's not a high priority.
5.  Any other business
    1. SO - Any thing else? No? Ok, thanks all.

---

#### Participants

- SO - Steve Olson, National Weather Service, USA [NWS], Chair
- BS - Benjamin Saclier, Meteo-France, France [MF], Vice-chair
- MC - Michael Claudon, Meteo-France, France [MF]
- JP - Jamie Piulachs, Bureau of Meteorology, Australia [BoM]
- DW - Dominic Woollatt, Met Office, UK [UKMO]
- NM - Nassos Michas, European Dynamics, [UKMO]
- GT - Giorgios Triantafyllidis, European Dynamics, [UKMO]
- DP - Dimitris Papadeas, European Dynamics, [UKMO]
- PR - Paul Rogers, Met Office, UK [UKMO]


#### Apologies

- YG - Yves Goupil, Meteo-France, France [MF]
- MG - Marc Giannoni, National Weather Service, USA [NWS]
- RGb - Remy Gibault, Meteo-France International [MFI]
- SD - Sungsoo Do, Korea Meteorological Administration, Republic of Korea [KMA], [delegate]
- MP - Mikko Partio, Finnish Meteorological Institute, Finland [FMI], [delegate]
- DJ - Duncan Jeffery, Met Office, UK [UKMO]
- JT - Jeremy Tandy, Met Office, UK [UKMO]
