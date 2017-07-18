---
layout: page
title: OpenWIS Technical Committee 2017 May - part 2
---

#### 24th May 2017, WebEx - meeting minutes

---

1. **Option 1 versus Option 4 - cost-benefit analysis**
    1. The related action on GitHub is: [Action-SC-2017-23](https://github.com/OpenWIS/openwis-documentation/issues/194)
    2. PR - So we're continuing with agenda item 1. Would GT please tell us where we're at with consolidating the feedback on the requirements spreadsheet.
    3. GT - So after I have all the feedback, I will:
        1. If more than one version is suggested by a single respondent, I will take the minimum, otherwise I will keep all the requirements where everyone has agreed the version, as they are.
        2. Add new columns and highlighting to show where there are differences in the versions proposed.
        3. Publish the consolidated spreadsheet and request more feedback on how to resolve the differences.
    4. SO - MG has provided our feedback, along with a description of our ideas on how the different versions might develop the architecture.
    5. BS - We are about 50% of the way through. We expect to finish in about 2 weeks.
    6. PR - That would be too late, since the SC meeting is scheduled for June 6th.
    7. BS - Ok, we will try to do it next week.
    8. PR - Perhaps you could send what you have already, half done, to George now?
    9. BS - Yes, ok.
    10. SO - Our approach was to view version 1 as the MVP, with updates based on feedback to get version 2 and version 3; version 3 being the first operational version of the modular approach.
    11. SO - There were a couple of things LM brought up:
        1. We might not be able to get to a cut-and-dried recommendation of Option 1 vs Option 4 for the SC.
        2. We might also want to make a recommendation to the SC on the development approach. I see 4 options here:
            1. European Dynamics do all the development.
            2. European Dynamics start the development and hand over to the Association for further development to completion.
            3. The Association do all the development.
            4. A hybrid where European Dynamics and the Association work together in some way.
    12. PR - European Dynamics don't have enough effort committed to the project to do it alone, and anyway we should be working in an agile way, with, say, LM doing some development, someone else doing some testing, someone else refining requirements as we go etc. Various skills are needed.
    13. SO - Ok, that sounds sensible.
    14. NM - We can implement some ideas initially and then work with the Association from there.
    15. LM - Ok, I agree it would be the hybrid approach.
    16. MC - European Dynamics will do a proof of concept?
    17. PR - More than that, they would develop a platform upon which we all build the rest of the application.
    18. BS - The new functions are not decided. European Dynamics implement a new architecture, then we decide who implements what; as a pilot?
    19. PR - Not really a pilot; a basis for incremental, modular development.
    20. WQ - I have the same question as SO: we had a discussion on what approach we will take on development of the new architecture.  TC to discuss because there are resource issues. Then we raise who does what with the SC. There are several options.
    21. SO - I'd like to hear each person's preferred approach.
    22. LM - I suggest the hybrid approach; European Dynamics design/build the architecture then the Association help with further development.
    23. PR - Yes, there would be a continuous dialog even while European Dynamics are building the architecture.
    24. SO - Once it is determined what the architecture is and which apps will be used, we could hold a Developer Conference.
    25. PR - The Association and European Dynamics would work together in agile teams, as we have discussed before.
    26. WQ - Yes, we have discussed this approach ourselves; that seems viable.
    27. MC - We have concerns about the resources needed because that is not clear.
    28. BS - Are we sure all WIS 1.0 requirements are needed for WIS 2.0? We don't want to spend more time on WIS 1.0.
    29. PR - So, your question is: how much WIS 1.0 do we really need?
    30. BS - And is it a little bit early to start a WIS 2.0 prototype?
    31. SO - If we consider it a minimum viable product for a modular WIS 1.0, we could fold some WIS 2.0 ideas into it, to demonstrate that the architecture is adaptable to WIS 2.0.
    32. PR - Which is why we have the three versions. Version 1 gets us going with the modular architecture; versions 2 and 3 might include WIS 2.0 features if we're already getting an idea of what those are. In any case, we want to influence the WIS 2.0 specifications by showing what is possible.
    33. PN - Certain core APIs will definitely be needed.
    34. DW - Ok, but we don't know what we will need to build yet.
    35. PN - We do in terms of some of the top level User Stories. Do we prioritize Discovery or Retrieval, in the cloud?
    36. WQ - In Toulouse we assumed that some of WIS 1.0 would still be needed. At a minimum we still need to serve WWW data; this is a major User Story whatever APIs we use to exchange the data.
    37. PN - It's interesting that you have chosen data exchange as a key User Story; at UKMO we are still intending to use MSS to do the actual data exchange.
    38. WQ - The spec says you have to exchange metadata and data, it doesn't say _how_ you do it. Some WIS 1.0 User Stories are still valid in WIS 2.0.
    39. LM - I'd go further and say that pretty much all of WIS 1.0 will be required.
    40. PR - I agree, we're talking about a transition over time from WIS 1.0 to WIS 2.0 eventually.
    41. LM - We need to consider what the next version is now that we have abandoned OpenWIS4. Given that a redesign is needed for WIS 2.0, then having a modular architecture would be a reason for version 5.
    42. SO - Do we need a deadline for return of the spreadsheet?
    43. PR - So shall we hold another TC next week?
    44. GT - I will need to have received the spreadsheets a couple of days before the TC to consolidate them and send out the version for the meeting.
    45. PR - Ok, so we could hold the TC next Thursday.
    46. BS - So Tuesday evening?
    47. GT - Ok.
    48. BS - Ok, we will try.
    49. SO - So how will you capture the differences, GT?
    50. GT - I will add new columns and highlight the differences.
    51. SO - Be good if you could summarise the level of differences.
    52. GT - Ok.
    53. SO - So do you need us to explain our approach?
    54. NM - We had a look at what MG wrote. We don't need to look into that right now; we will during the next stage of the analysis.
2. **Draft Option recommendations to SC (SC meeting scheduled for 8th June)**
    1. PR - We'll cover that at the TC next week.
3. **[Issues](https://github.com/OpenWIS/openwis-documentation/issues) review**
    1. PR - So everyone should look at the Actions on GitHub (link above) and check if they have any to do for the SC meeting.
    2. [Action-TC-2017-21](https://github.com/OpenWIS/openwis-documentation/issues/231) DevCon agenda and timing (Leon's Doodle poll)
        - LM - I've had 2 responses so far. Please fill in the Doodle Poll, so we have some idea when we might hold the DevCon.
    3. [Action-SC-2017-03](https://github.com/OpenWIS/openwis-documentation/issues/174) Define patchable - postponed until next meeting.
    4. Guidance for new developers (wiki pages) - postponed until next meeting.
4. **AOB**
    1. SO - I wonder if we should create a list of potential contributors to version 5, from the Association...
        1. PR - Does that sound like a Doodle Poll, LM?
        2. LM - Yes, Ok, I'll set one up.
            [Action-TC-2017-24](https://github.com/OpenWIS/openwis-documentation/issues/271)

---

#### Participants
- SO - Steve Olson, National Weather Service, USA [NWS], Chair
- LM - Leon Mika, Bureau of Meteorology, Australia [BoM], Vice-Chair
- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM]
- MC - Michael Claudon, Meteo-France, France [MF]
- BS - Benjamin Saclier, Meteo-France, France [MF]
- YG - Yves Goupil, Meteo-France, France [MF]
- DW - Dominic Woollatt, Met Office, UK [UKMO]
- DJ - Duncan Jeffery, Met Office, UK [UKMO]
- PN - Paul Nelson, Met Office, UK [UKMO]
- PR - Paul Rogers, Met Office, UK [UKMO]
- NM - Nassos Michas, European Dynamics, [UKMO]
- GT - Giorgios Triantafyllidis, European Dynamics, [UKMO]
- NM - Dimitris Papadeas, European Dynamics, [UKMO]
- MG - Marc Giannoni, National Weather Service, USA [NWS]
- KS - Kari Sheets, National Weather Service, USA [NWS]

#### Apologies
- RGb - Remy Gibault, Meteo-France International [MFI]
- SD - Sungsoo Do, Korea Meteorological Administration, Republic of Korea [KMA]
- MP - Mikko Partio, Finnish Meteorological Institute, Finland [FMI]
- CS - Cassie Stearns, National Weather Service, USA [NWS]
