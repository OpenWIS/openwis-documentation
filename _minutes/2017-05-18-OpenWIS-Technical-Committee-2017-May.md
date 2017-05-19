---
layout: page
title: OpenWIS Technical Committee 2017 May
---

#### 18th May 2017, WebEx - meeting minutes

---

1. **Option 1 versus Option 4 - cost-benefit analysis**
    1. The related action on GitHub is: [Action-SC-2017-23](https://github.com/OpenWIS/openwis-documentation/issues/194)
    2. NM presented [v5 requirements]({{ site.baseurl | prepend: site.url }}/assets/TC-20170518-v5-Requirements.pdf)
    3. NM - So over the last few weeks we have put the requirements from the original SSD into Enterprise Architect. We have discussed them with UKMO and BoM to get a better understanding. They are all linked within the model so we can see where each requirement comes from and what depends on it, eg: WIS 1.0 compliance.
    4. GT (EA on-screen demo)- So here we can see how the requirements are linked within the EA model. We can go from the top-level requirements down to the lower level and back up from low level to the top. We can open them up and read the details of each.
    5. GT - We can also view the Traceability Matrix to cross-reference the requirements.
    6. NM - These are still high level requirements so we will need to do some further analysis to generate the Use Cases. However, because we are short of time, we have put some estimates against the requirements; these estimates will need to be refined later when we do the Use Cases.
    7. NM - We have exported the requirements and estimates into a spreadsheet for ease of access.
    8. BS - Does the use of EA require a software license?
    9. NM - Yes.
    10. BS - Is it possible to change the spreadsheet and then import back into EA?
    11. NM - No, we would import changes or comments from Excel manually.
    12. GT - So here is the spreadsheet: [OpenWIS5-Requirements]({{ site.baseurl | prepend: site.url }}/assets/OenWIS5-Requirements-20170518.xlsx)
    13. LM - Did anyone look at the requirements spreadsheet yet?
    14. BS - We have started.
    15. RGb - Yes, me too.
    16. GT - It should be fairly familiar since it is built from the original SSD, with just a few additions such as GEOSS and suggestions from LM.
    17. GT - So please send any further feedback to us and we will update the requirements.
    18. NM - There are columns for version and priority.
    19. NM - Version means the Release of the v5 software, where:
        - version 1 means the first development release; this should include all the things that are really important to get sorted out early.
        - version 2 means the second development release.
        - version 3 means the operational release.
        - version 0 means that we don't need this requirement any more, or at least not in the first operational release; maybe we will add it later.
    20. NM - We can of course change these releases/versions if we want, but this is the general idea.
    21. NM - Priority is set to medium for everything at the moment, but we want to set them to High/Medium/Low, to show how early in a development iteration they should be done, for the specific release they will be in.
    22. NM - The green box at the top of the spreadsheet shows our assumptions about the other tasks required for implementation, such as analysis, mock-ups, design, test etc. These percentages are averages based on our experience. Please comment on these if you think we have under estimated.
    23. LM - At this stage, I think it is still too early for the TC to be able to choose between Option 1 and Option 4. Does everyone agree?
    24. DW - Yes.
    25. LM - We should set some deadline for completing the review of these requirements; how would we conclude the review - by email?
    26. PR - So I was expecting some sort of summary report that the TC could present to the SC.
    27. BS - Review by email is ok with us.
    28. LM - Email is ok for me too.
    29. PR - Ok, but how does the information presented here help us decide between Option 1 and Option 4? Matteo wants to know what he would get in return for a year's worth of work and how much it would cost; also some idea of what would come after; how we move towards WIS 2.0.
    30. NM - So this requirement is for the full version; Option 1 is a reduced version of v5 that is just a collection of prototypes, of selected features. So, it would be easy to work out the cost of Option 1 once we had a list of the features we want to prototype. The timescale would depend on how many people you have.
    31. PN - But this is the specification for v3; we may not need all of this now.
    32. DW - This is WIS 1.0 compliant, which it needs to be, but working towards WIS 2.0.
    33. DW - Option 1 doesn't improve v3.
    34. DW - Option 4 improves on v3 and moves us towards WIS 2.0, so we are wasting less effort with Option 4.
    35. DW - The full cost of Option 1 is difficult to calculate because it is spread over a long time.
    36. PR - Yes, WQ made this point in Toulouse - some costs are delayed, but not avoided.
    37. PN - But this way we end up with an architecture that does push and pull, when in the end we might only need pull.
    38. DW - Ok, but v5 will be modular so that we can change these things easily when the time comes.
    39. LM - I guess that WIS 2.0 will take a few years, so we're starting with WIS 1.0 on a new architecture so that we can adapt to WIS 2.0 later.
    40. PN - Do we want to build a new solution based on WIS 1.0?
    41. PR - Our expectation is that we could build WIS 2.0 incrementally and transition over time from WIS 1.0, if we have the new architecture.
    42. PR - My concern is whether we have the information to decide this.
    43. PN - This is a view of WIS based on the current components; I think we need a view of WIS based on the to-be components.
    44. DW - Probably be a similar set for WIS 2.0; maybe a different portal, but we'll still need search, retrieval etc.
    45. PR - I think we need a summary report we can present to the SC.
    46. DW - So have we not worked out the cost estimate for Option 1?
    47. NM - It will be easy to come up with a cost for Option 1 by defining the pilots.
    48. PN - So we need a set of recommendations on what we should develop over the next year.
    49. NM - OK, so choosing what should go in, is a business decision.
    50. DW - Harvesting first, in my opinion.
    51. PR - Ok, so we're not going to decide that now. We need to collect everyone's feedback on which features belong in version 1, 2 and 3, as we discussed earlier.
    52. PN - By what date?
    53. LM - I will have a word with SO about holding another TC session next week. We would want the feedback in time for that.
    54. WQ - Are we talking about Option 1 or Option 4?
    55. PN - What we want to see in version 1, 2 and 3 of Option 4.
    56. RGb - Thursday/Friday next week are holidays in France.
    57. LM - Ok, it'll have to be Wednesday then, I'll speak to SO.
    58. Actions:
        - ALL - [Action-TC-2017-22 Provide feedback VIA the requirements spreadsheet](https://github.com/OpenWIS/openwis-documentation/issues/NNN).    
        - LM - [Action-TC-2017-23 Update TC chair on progress](https://github.com/OpenWIS/openwis-documentation/issues/NNN).    
    59. LM - We'll adjourn there and leave the rest of the agenda until next time.

---

#### Participants
- LM - Leon Mika, Bureau of Meteorology, Australia [BoM], Vice-Chair
- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM]
- MC - Michael Claudon, Meteo-France, France [MF]
- BS - Benjamin Saclier, Meteo-France, France [MF]
- RGb - Remy Gibault, Meteo-France International [MFI]
- DW - Dominic Woollatt, Met Office, UK [UKMO]
- DJ - Duncan Jeffery, Met Office, UK [UKMO]
- PN - Paul Nelson, Met Office, UK [UKMO]
- PR - Paul Rogers, Met Office, UK [UKMO]
- NM - Nassos Michas, European Dynamics, [UKMO]
- GT - Giorgios Triantafyllidis, European Dynamics, [UKMO]
- NM - Dimitris Papadeas, European Dynamics, [UKMO]

#### Apologies
- SO - Steve Olson, National Weather Service, United States of America [NWS], [delegate], Chair
- SD - Sungsoo Do, Korea Meteorological Administration, Republic of Korea [KMA], [delegate]
- MP - Mikko Partio, Finnish Meteorological Institute, Finland [FMI], [delegate]
- MG - Marc Giannoni, National Weather Service, United States of America [NWS]
- CS - Cassie Stearns, National Weather Service, United States of America [NWS]
