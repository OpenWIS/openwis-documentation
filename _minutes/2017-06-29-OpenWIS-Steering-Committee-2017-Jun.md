---
layout: page
title: OpenWIS Steering Committee 2017 June
---

#### 29th June 2017 - WebEx

---

1. **Welcome and introductions**
    1. JT - Is everyone happy that SO speaks for KS?
    2. ALL - Yes.
    3. JT - Noting that MV is absent, we have 6 out of 7 represented, so we are quorate.
2. **Approve previous SC meeting minutes**
    1. JT - Anybody not happy with the previous minutes?
    2. JT - Hearing nothing, previous minutes are approved.
3. **Identification of priority topics for OpenWIS Steering Committee 2017 June**
    1. JT - The main topic of discussion today is the OpenWIS-Core work plan. If there is time, we will look at the other agenda items such as project charters, rule changes and funding sources.
    2. JT - In Toulouse we talked about a rigorous risk review and updating goals but I am suggesting we defer these topics until we have reflected on the OpenWIS-Core work plan:
        - Risk review (see actions [Action-SC-2016-14 Add new risks to Risk Register](https://github.com/OpenWIS/openwis-documentation/issues/170) and [Action-SC-2017-20 Risks to the Association](https://github.com/OpenWIS/openwis-documentation/issues/191))
        - Update Goals of OpenWIS Association (see Action-SC-2017 39-44, 46-48 and 54-56, and [Action-SC-2017-45 Goals for the Association](https://github.com/OpenWIS/openwis-documentation/issues/216) "Each SC delegate should propose 3 goals for the Association (not the OpenWIS-Core project), for discussion at the June 2017 SC" )
    3. JT - All content?
    4. ALL - Yes.
4. **Next meeting**
    1. JT -  I propose we hold the next SC teleconference in September 2017 (following northern hemisphere summer break) to resolve deferred topics;
    2. JT - Thursday September 14th at 11:00 UTC.
    3. ALL - Ok.
5. **Approval of agenda**
    1. JT - Is everyone happy with the agenda?
    2. ALL - Yes.
    3. JT - Any other business?
    4. JT - Hearing none.
6. **Review open actions and issues**
    1. JT - I don't want to go through all the actions now, we don't have time.
    2. JT - Up to the Toulouse meeting we kept an action list on the web site, but now Paul has moved them into GitHub.
    3. PR - {sharing screen showing [actions list in GitHub](https://github.com/OpenWIS/openwis-documentation/issues?q=is%3Aissue+is%3Aopen+label%3A%22Steering+Committee%22) - From the list of issues in openwis-documentation, click on the label 'Steering Committee' and you will see the list of open actions for this meeting; click on your GitHub icon on the right hand side and you will see all those assigned to you.
    4. JT - Please attend to your own actions.
7. **OpenWIS Core work plan**
    1. JT - Over to SO to brief the SC on the TC findings.
        - See [Action-SC-2017-23 Future development options report](https://github.com/OpenWIS/openwis-documentation/issues/194)
        - Also see related actions [Action-SC-2017-21 Feature comparison for v3 vs v4](https://github.com/OpenWIS/openwis-documentation/issues/192) and [Action-SC-2017-22 v4 MVP cost estimate](https://github.com/OpenWIS/openwis-documentation/issues/193)
    2. SO - LM and I have summarised the findings of the TC in [SC Briefing June 2017](https://github.com/OpenWIS/openwis-documentation/files/1111224/SC.Briefing.June.2017.pdf)
    3. SO - The TC met 4 times and we also had a couple of scrum meetings.
    4. SO - The document lists the alternatives, discusses those alternatives and then presents some of the implications of our proposals.
    5. SO - So there are the descriptions of Options 1 and 4, that you will be familiar with from Toulouse.
    6. SO - We concluded that Options 1 and 4 were not optimal, so instead we went for a hybrid option that we're calling Option 1.5.
    7. SO - Some questions arose, such as, who would do the further development of OpenWISv3 that is included in Option 1; TC members or Eurodyn?
    8. SO - In Option 1.5, OpenWISv3 is put into maintenance mode, but there are some implications there that I will return to later.
    9. SO - We like Option 1.5 because:
        1. It gives us the opportunity to strengthen our relationship with WMO through WIS 2.0 pilots.
        2. We can explore new ideas on how to do WIS 2.0.
        3. We can demo our findings to WMO and others.
        4. It allows the software design to evolve to meet the WIS 2.0 specifications.
        5. It allows us to determine what skills are required for OpenWISv5 - the modular, extensible version, and create training opportunities for developers.
    10. SO - So for the TC, the hybrid solution Option 1.5 makes the most sense.
    11. SO - We took a poll on what were the WIS 1.0 requirements most relevant to WIS 2.0 and we found 100% agreement on 13 of them. With the dependent requirements taken into account, they cover about 1/3 of the WIS 1.0 requirements.
    12. SO - At a high level, they focus mainly on metadata and data delivery.
    13. SO - We are currently going through the exercise to prioritise the 13 down to the few that will be the focus of the pilot studies. We anticipate a minimum web service that will be the centre-piece, based on a modular architecture.
    14. SO - Next we look at the implications of Option 1.5:
        1. OpenWISv3 would be in maintenance mode, but we can't cease all development because it would be in operations for the foreseeable future and would need enhancements, possibly larger scale, for example replacing OpenAM/DJ.
        2. We would continue open source development of OpenWISv3, including contributions from partners as they wish.
        3. We don't have enough information yet about WIS 2.0 and we should seize the opportunity to influence that.
        4. We can't expect OpenWISv3 to last until 2025 so we will have to replace it before WIS 2.0; we should re-evaluate the position in 2019.
    15. SO - Those are the recommendations of the Technical Committee.
    16. JT - Ok, I'll open it to the floor for discussion; any questions?
        1. MDA - If we stop development of OpenWISv3, does this cause any operational issues for members?
        2. SO - It does not for the time being.
        3. MDA - Is everyone using the current version in operations?
        4. SO - As of Toulouse, it was split between 3.12 and 3.13; 3.14.8 was not released.
        5. JT - So we're all on 3.12 or later?
        6. RGb - We're on 3.13 but plan to move to 3.14.
        7. MDA - UKMO?
        8. PR - We're on 3.14.
        9. JT - 3.14 meets the first set of requirements, the WIS 1.0 Technical Specifications; we can patch anything that needs it.
        10. JT - The second set of requirements were internal, eg: security policy requirements etc. We spent the last 2 years fixing that. Ongoing maintenance of OpenWISv3 is still a concern at NWS though, SO?
        11. SO - Correct.
        12. JT - So NWS most sensitive to ongoing maintenance issues.
        13. SO - The key issue was the Java version. We now see that we can move forward with Java and the system runs with no issues; so some security concerns are addressed.
        14. JT - Can we all confirm that we're all content with OpenWISv3 in the operational environment?
        15. RGr - MF ok with 3.14.
        16. RGb - MFI yes.
        17. SD - KMA yes.
        18. WQ - BoM ok with v3.
        19. JT - So if we maintain v3 we are not causing issues. Ok SO?
        20. SO - Yes, 3.14 is Ok.
        21. MDA - Another question - if a member does some contribution to OpenWISv3, you say the work will not be commissioned by the TC; does that mean each member ends up with their own version?
        22. SO - No. It means that contributions are free of charge to the Association because all contributions are open source.
        23. RGr - But there are 2 separate aspects to this:
            1. Ok, so the Association decides OpenWISv3 is now in maintenance mode, so won't be spending €100k on it.
            2. But even if someone pays for their own contribution, the software should still be official and the TC should still have a say.
        24. JT - I think what RGr is suggesting is, we avoid forking the OpenWISv3 software. So, we want a way to bring enhancements back into the trunk.
        25. SO - Yes, ok, let me reword that in the text of the Briefing:
            - [Action-SC-2017-57 Reword the text of the TC Briefing to the SC](https://github.com/OpenWIS/openwis-documentation/issues/281)
        26. JT - So we all agree to avoid forking.
        27. WQ - What about a development specific to a partner?
        28. JT - My suggestion is that if you're creating an enhancement just for BoM then make it s configurable component.
        29. WQ - Ok.
        30. JT - SO, does that make sense?
        31. SO - Yes, they could become part of an API and we could make these things configurable.
        32. JT - Do we need to update the Briefing note? The note can be turned into a roadmap and what we just discussed would affect the Technical Rules.
        33. SO - Yes.
        34. JT - SO, can you take an action to create the roadmap?
        35. SO - Yes, it's already in progress:
            - [Action-SC-2017-58 Create a roadmap for OpenWIS-Core](https://github.com/OpenWIS/openwis-documentation/issues/282)
        36. RGb - Is there a plan for OpenWISv3?
        37. SO - We would develop maintenance releases from 3.14.8, although there is no plan for another 3.14 release at this time.
        38. JT - So there could be an OpenWISv3 roadmap.
        39. MDA - For Option 1.5, it's not clear what is the proposal for OpenWISv5; just a design or also prototypes?
        40. SO - We're looking at pilot studies to form the basis of the modular approach.
        41. MDA - So the plan is to prototype components and include them in the future OpenWISv5.
        42. JT - The way PR described it to me, OpenWISv5 would be a runnable demo that could be shown to potential partners or WMO. It might look something like Nassos' PoC, but look more like a WIS system than just a collection of technologies. We wouldn't make it compliant with WIS 1.0 Technical Specifications because they will change. SO?
        42. SO - That's right.
        43. JT - So we avoid spending a lot of money on another WIS 1.0. As we continue to develop it, we may reach a point where we need only an incremental change to make it compliant. But, we wouldn't have a milestone that says OpenwISv5 will be operational on a certain date. With a modular architecture and incremental prototype we can replace modules as the WIS 2.0 Technical Specifications evolve. The intent is that we never invest in dead software. We focus on an architectural core that is the basis of an operational system, but won't immediately meet compliance.
        44. MDA - I'm not sure that will work. We are building something to play with but it may not be suitable as an operational base.
        45. JT - Normally you would throw whole prototypes away, but we're developing functional components that we might throw away instead.
        46. RGr - Is this the [PDF drawing](https://github.com/OpenWIS/openwis-documentation/files/1108147/OpenWIS.Core.recommendation.16.Jun.09-42.pdf) you are describing? We are agreeing that we don't want to build a WIS 1.0 system.
        47. JT - Yes.
        48. RGr - So the x's in circles are the pilots that can be thrown away in the future. We have some concerns that the supporting architecture, the cloud around the x-circles, can't be built now. We think technology changes could overtake our current ideas. We agree on having the pilots, but we don't think we need, say for the next 6 months to a year, the supporting architecture around the pilots.
        49. JT - My understanding is that the connections between the functional components must exist to make OpenWIS hang together.
        50. RGr - We don't think we can know what those connections are now. The PoC's don't need to be related. We demo them to WMO then put them in the bin. The PoC's can be built around what we have now in terms of metadata, pub/sub etc; isolated concepts rather than the basis of OpenWISv5.
        51. SO - One of the key concerns in any design with evolving requirements is that you want a design where you satisfy all requirements and don't fall down because of how you built it. Even in micro-services, with each of these PoC's there is a preferred choice for the underlying micro-service. We may have to evolve, but all this comes into play for this prototype design, evolutionary approach.
        52. RGr - Right now I don't care about micro-services or design; it's about functional elements you can see and touch.
        53. MDA - Do you recall the discussion involving Japan and Korea and the difficulty they had seeing the relevance of WIS 2.0 to GDPSS? We don't mind what is under the platform, but must show what you will get.
        54. JT - So we focus on components that enable the business outcome that Users need?
        55. MDA - Yes. After the business say what they want we can always design the architecture.
        56. WQ - RGr, are you suggesting not doing Option 1.5, but that we concentrate on WIS 2.0, say JSON metadata concept, instead?
        57. RGr - Sort of. My idea was not to focus on architecture or design, but launch a project in the Association where we each propose an experiment on something that we think will be in WIS 2.0. Say max cost €30k, we each get a grant from the Association to do a PoC, but it doesn't need a coherent architecture.
        58. WQ - Wedon't know where the WIS 2.0 specification is, so we are working on prototypes of the WIS 2.0 specification.
        59. RGr - Yes, could be.
        60. WQ - What you suggest can't be done without a clear idea of the specification.
        61. MDA - I believe that with the work done on WIS 2.0 in the last 2 years we do have a clear idea of WIS 2.0. We have a few elements in mind but we need to show these things to WMO members.
        62. WQ - And Option 1.5 is not including that?
        63. RGr - We're looking at the problem from a different angle. Option 1.5 is bottom-up. I propose 3 or 4 things we think will be in WIS 2.0. With €30k we could show something around that. Doesn't matter if they don't talk to each other; using Google you can find metadata; using pub/sub is another demo, but they're not joined up.
        64. SO - I agree. I view each of these pilots as stand alone. Focus on the components.
        65. JT - So the architecture is the technical scaffolding.
        66. RGr - The basis we already have is cache and ISO 19115 metadata. So maybe translate ISO 19115 to JSON etc. and create your sandbox, then play with what you want.
        67. JT - We have 10 minutes left. Let's see where we have consensus.
        68. JT - Put OpenWISv3 into maintenance mode - all agree?
        69. ALL - Agree.
        70. JT - OpenWISv3 remains the operational version?
        71. ALL - Agree.
        72. JT - OpenWISv5 for developing understanding and influencing WIS 2.0 Technical Specifications?
        73. RGr - Not OpenWISv5.
        74. JT - Ok, whatever we call what we spend the money on: 'Pilots to support development of the Technical Specifications'.
        75. ALL - Yes.
        76. JT - I see delivering stand-alone pilots with enough core architecture to provide context. I would ask TC how independent the pilots can be. How much consistency do we need between them?
        77. WQ - For what?
        78. JT - For pilots over the next year; all Java? Do we care? TC should recommend the level of consistency between the pilot projects.
        79. SO - That's work in progress at the TC.
        80. JT - Action on the TC; pilots for WIS 2.0 - for example, will they fit into the same architectural framework? Is that the question that is in contention?
            - SO - [Action-SC-2017-59 Provide a statement on pilot consistency](https://github.com/OpenWIS/openwis-documentation/issues/283)
        81. RGr - Yes. I'll put my idea in an email to the SC:
            - RGr - [Action-SC-2017-60 Circulate a proposal on pilots to SC](https://github.com/OpenWIS/openwis-documentation/issues/284)
        82. JT - Do we need to have resolved this for the Board Meeting?
        83. RGr - Can we say at the Board Meeting that we expect to spend €100k on pilots over the next year?
        84. JT - Are you proposing Association funds or staff time?
        85. RGr - I'm proposing that the Association funds €25-30k per pilot, for 3 or 4 pilots.
        86. JT - Ok, that's a discussion for the Board.
        87. MDA - Yes, that's right.
        88. JT - The Board doesn't need to be concerned with whether the pilots are consistent or not.
        89. LLG - We can all agree with the general idea, but we need more information on the pilots.
        90. RGr - The Board agrees the principle and delegates those concerns to the SC.
        91. MDA - Yes, I confirm that. The Board will agree to do some pilots and how to fund. Then the SC decides which pilots to do for WIS 2.0.
        92. JT - The recommendation to the Board is that we proceed in the way I summarised.
        93. RGr - Let's say 3 or 4 pilots selected from say 10 suggestions; TC propose the 4 to the SC at €25k per pilot.
        94. JT - Let's see how the Board want us to structure this.
        95. JT - We've done the OpenWIS-Core work plan review and the TC will start gathering 3 or 4 recommendations. Also they will resolve the question of technical consistency.
8. MDA - Just some information for everyone to keep in mind: During March next year, there will be a Technical Conference of the CBS, 1 day on Information Systems. We want to bring the evolution of WIS to the table, so if the Association can demo something that will help a lot.
9. JT - We'll defer the rest of the agenda until the SC in September, except the Rule change item, which I shall do by correspondence.
10. JT - Meeting closed at 12:37 UTC.


#### Participants
- JT - Jeremy Tandy, Met Office, UK [UKMO], [delegate], Chair
- RGr - Remy Giraud, Meteo-France, France [MF] [delegate]
- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM], [delegate]
- SD - Sungsoo Do, Korea Meteorological Administration, Republic of Korea [KMA], [delegate]
- KS - Kari Sheets, National Weather Service, USA [NWS], [delegate] (joined late)
- LLG - Loic Le Gallou, Meteo-France International [MFI], [delegate]
- SO - Steve Olson, National Weather Service, USA [NWS]
- RGb - Remy Gibault, Meteo-France International [MFI]
- MDA - Matteo Dell'Aqua, Meteo-France, France [MF]
- PR - Paul Rogers, Met Office, UK [UKMO]

#### Apologies

- MV - Mikko Visa, Finnish Meteorological Institute [FMI], [delegate]
