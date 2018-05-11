---
layout: page
title: OpenWIS Steering Committee 2017 October
---

#### 9th October 2017 - WebEx

---

(The responsibilities of the Steering Committee [SC] are described in Article 13)

1. **Welcome, introductions and approval of agenda**
    1. JT - NWS, MF, MFI and UKMO are represented. SD requested that JT act as proxy for KMA (by email). There is no representative from BoM or from FMI. The meeting is quorate with 5 out of 7 represented.
    2. JT - Apologies for the lateness of the agenda. Is everyone content with the agenda?
    3. ALL - Yes.
    4. JT - Ok, agenda approved.
2. **Approve previous SC meeting minutes**
    1. JT - All content with the previous minutes [OpenWIS Steering Committee 2017 June minutes]({{ site.baseurl | prepend: site.url }}/minutes/2017-06-29-OpenWIS-Steering-Committee-2017-Jun.html)
    2. JT - Ok, previous minutes accepted.
3. **Clarification of organisational roles within OpenWIS Association**
    1. JT - The main topic for discussion today is the TC work plan, but I want to cover the organisational roles first because I think it will be relevant to that discussion later. If you recall, during the March meeting we decided that the roles of the PMC/TC/SC didn't reflect how responsibilities should be assigned once the Association began working on multiple projects. This was covered in item 13.3.1 of the March minutes and there were some actions, resolutions and supporting documents related to this:
        - [Action-SC-2017-14 Improve processes for managing new projects](https://github.com/OpenWIS/openwis-documentation/issues/185) *“In light of the discussion around new projects during SC-MAR2017 (eg: FMI's [smartmet](https://github.com/fmidev/)) and the uncertainties this has surfaced around the roles of PMC/TC/SC, review the Articles, Internal Rules and Technical Rules and propose any improvements.”*
        - [Action-SC-2016-14 Add new risks to Risk Register](https://github.com/OpenWIS/openwis-documentation/issues/170) *“Add a risk to the Risk Register stating that the Articles/Rules of the Association do not adequately define the architecture role of the TC (Article 14.1)”*
        - Note: **Resolution-AM-2016-09** approving "edits to describe governance for multiple projects"
        - See [OpenWIS Project Governance Rules Supplement]({{ site.baseurl | prepend: site.url }}/rules2/2016-03-11-OpenWIS-Project-Governance.html)  [PMC structure diagram]({{ site.baseurl | prepend: site.url }}/assets/ATT-OWIS-SC-2016-7_owis-committee-structure.pdf)
    2. JT - We went through the rule changes we would like at the March SC and the action was placed on me to update the way the organisational structures are described.
    3. JT - As a result I propose update to [Internal Rules Title 7]({{ site.baseurl | prepend: site.url }}/rules/7-management-structure-and-qualification-of-officers.html) based on responsibilities outlined [here](https://github.com/OpenWIS/openwis-documentation/issues/185#issuecomment-335121087)
    4. MDA - I'm not sure that the SC can choose the SC Chair and Vice-chair.
    5. JT - It might look odd but I checked the rules and that's what they say. I've looked back through previous meetings and that's how we've always done it - the SC appoints them. The Board is responsible for policy changes, managing risks and deciding the purpose of the Association. The SC is responsible for ensuring the Association operates correctly according to it's own rules and processes.
    6. MDA - Yes, ok.
    7. JT - We may need to change article 14 relating to the TC. The TC provides technical oversight and operates technical infrastructure for the Association.
    8. MDA - So the PMC is the same as the SC but for a project.
    9. JT - Yes, the PMC sets what the project does, what milestones it works to etc. The SC holds the PMC to account, checks that it is doing what it said it would.
    10. MDA - That makes sense, but there is nothing in PMC that points to SC; you have TC acting as technical board, PMC in charge of each project, with a link to the TC but not to the SC.
    11. RGr - TC/PMC are combined for OpenWIS-Core and we have to shift tasks from TC to PMC, so the description of the TC role is new.
    12. JT - Yes, the TC maintains repositories, release processes etc. What we have been getting so far from the TC is a PMC report for OpenWIS-Core, so we're confused about the roles. This change will increase autonomy for the PMC. Previously we've had a few days at TC deliberating the work plan then we've discussed it again at the SC. This change makes the PMC responsible for the work plan.
    13. RGr - With multiple projects we will discuss each at SC; if SC believe a project isn't going well, how do we control that?
    14. JT - The PMC says what the release criteria are, then the SC will hold them to account if they don't deliver that.
    15. RGr - So we need a report from the PMC to the SC, on say, a yearly basis.
    16. JT - Good idea; SC can then endorse the proposed milestones and quality criteria.
    17. JT - The TC could also use that to comment on the technical approach as part of its architectural oversight.
    18. JT - Ok, I've added those points into the [issue](https://github.com/OpenWIS/openwis-documentation/issues/185)
    19. JT - Anyone not happy with the issue as it now stands? Ok, hearing nothing, I'll complete that action to make those updates and then we can vote on the new rules at the next SC. We need to be clear about these new roles before the next Annual Meeting.
        - [Action-SC-2017-14 Improve processes for managing new projects](https://github.com/OpenWIS/openwis-documentation/issues/185)
4. **OpenWIS Technical Workplan**
    1. JT - Ok, PR, in the absence of SO, are you able to report on the progress with the work plan?
    2. PR - Yes.
    3. PR - The main activity over the last few weeks has been the drafting of proposals for pilots, mainly for the WMO CBS TECO (March 2018) meeting demo but also for longer term technical investigations into aspects of WIS 2.0. All the [proposals](https://github.com/OpenWIS/openwis-documentation/issues?utf8=%E2%9C%93&q=is%3Aissue%20label%3A%22OpenWIS%20Pilot%20Proposal%22%20) are on GitHub.
    4. PR - As you know we then held a poll on which proposals to take further. We got clear winners for both the TECO demo:[OPP-6: WIS Djibouti](https://github.com/OpenWIS/openwis-documentation/issues/309), and for the Technical pilot: [OPP-1: Pub-Sub Notifications](https://github.com/OpenWIS/openwis-documentation/issues/299). Both of these proposals were well clear of any others in both polls.
    5. PR - Since then we have had further discussions at [TC](http://openwis.github.io/openwis-documentation/minutes/2017-09-28-OpenWIS-Technical-Committee-2017-Sep.html) and scrum meetings as well as doing some design work with European Dynamics. We have concluded that we could include some aspects of the pub-sub proposal into the Djibouti proposal and focus on only the TECO demo for the next few months. Also, BS has suggested that we may be able to work in some of [OPP-5: WIS Dashboard](https://github.com/OpenWIS/openwis-documentation/issues/303), so we will be discussing that at the scrum meeting tomorrow.
    6. PR - We have created a new repository for the [Djibouti proposal](https://github.com/OpenWIS/djibouti) where you can see the design documents being worked up.
    7. PR - So, any questions so far?
    8. RGr - I don't think we should name the pilot after a real WMO member country for the TECO demo. We could use a country that is not real, like 'Westeros' from Game of Thrones.
    9. JT - We did intend the recognition that this infrastructure would be available for use by developing nations.
    10. PR - Well, it would be easy to change the name for the TECO demo narrative and for the charter, which we have yet to complete.
    11. MDA - Just looking at the design diagram, I think the story is missing something. You have the observer putting data into the system, then people getting data from a website.
    12. JT - In the TC two weeks ago, the question was raised by European Dynamics about whether the data acquisition part was in scope. We decide that to keep it manageable we would start with limited architecture.
    13. MDA - Acquisition is a problem for users. What we are demonstrating is a value added service showing how people will use WIS 2.0 to provide services to users. You may consider that the user wants notification only when it will rain, say.
    14. RGr - People will see information where they put it in, where are we going to plug in something to take the information out?
    15. JT - Mouktar is publishing to a web server, or Amazon S3, it doesn't matter; it will be trivial to put a visualisation app on top of that.
    16. JT - So, where does the pub-sub fit in? Well, in the narrative, each time Mouktar adds a new entry, WIS 2.0 would put it into a pub-sub queue for people to subscribe to. We're developing new ideas about how this works within the WMO infrastructure; you need reliable infrastructure for pub-sub to work. It may be the role of an RTH 2.0 to provide this, so that wherever you are in the world you can still subscribe. I don't know the answers, we're just trying it out.
    17. RGr - I understand what is behind what you said, but the demo is to look from the user perspective. So don't worry about RTH 2.0. Show how you inject your data and how you then see it on a webpage. Don't focus on the technical infrastructure.
    18. JT - We are going to have to bottom those out at some point, but we do want Mouktar to put some data in.
    19. RGr - But it's a black box.
    20. JT - Yes, but we need to know it works and isn't just smoke and mirrors.
    21. RGr - But the focus at TECO is seeing a service that works.
    22. JT - Right, it's not important what the technology is.
    23. JT - So, PR, am I right in thinking that the primary objective is to demo what approach might be necessary to achieve broad accessibility and widespread use of WIS 2.0?
    24. PR - Yes. We will be running an agile project, so we will see how some things work out and may alter course along the way. We will be focussing on delivering something that will make a good demo of such a service. I do not expect us to show the details of the underlying technologies or architecture at the TECO meeting. We will define what the outcome should look like in the project charter, who will do the demo, how, what they will need; we're assuming any member of the SC could do the demo.
    25. RGr - Should the data input be CSV?
    26. JT - That just shows that low level technology will work.
    27. RGr - We have countries like Senegal that use a simple website for data input; perhaps we could incorporate that?
    28. JT - Maybe, could you contact them about that?
    29. RGr - Yes, ok.
        - [Action-SC-2017-61 Contact Senegal about use of their website for data input](https://github.com/OpenWIS/openwis-documentation/issues/322)
    30. MDA - We need a clear view of what we want to showcase in WIS 2.0; we are not trying to show 100% of the WIS 2.0 concept. Are we trying to show that:
        - observations will flow without the GTS?
        - information is easy to find with a commercial search engine?
        - the WIS 2.0 ecosystem will provide new services?
    31. JT - Yes to all three, starting from low-tech.
    32. JT - We haven't included many things, such as federated ID or cloud based compute. We _are_ showing an authoritative list of WMO datasets, the catalog, can be found. It's not operational, it's just there to ask the question.
    33. MDA - Our problem is that we have a lot of data but we can't find it, or we can find it but we can't use it. It would be nice to show how you can find _and_ use the data.
    34. JT - We talked earlier about notifications of rain.
    35. MDA - Perfect: that provides a service to agriculture. Show that so that we can explain that.
        - JT - [Action-SC-2017-69 Show notifications of rain or similar service in TECO demo](https://github.com/OpenWIS/openwis-documentation/issues/330)
    36. JT - So, PR, in terms of setting up this project, how long will that take, a couple of weeks?
    37. PR - Yes, we should be able to complete the project charter to say what the tasks are and who will work on it.
    38. JT - SC need to review the charter and the Board approve.
    39. JT - We talked about allocation of funds and RGr suggested that we might allocate about €20k to each pilot project. Is that funding still needed, given that we're working together on one project?
    40. RGr - Now that we have one larger project I suggest we make it the responsibility of the PMC chair to ask for whatever funds they need. At the moment it looks like that won't be necessary.
    41. JT - Ok, so the PMC should know that funds can be used to speed up work, if necessary. Everyone happy with that?
    42. KS - Yes.
    43. RGb - Yes.
    44. JT - Ok, it might be that we can deliver without those extra funds but they are there if needed.
5. **Review new Project Charters**
    1. SmartMet
        1. See [Action-SC-2017-15 smartmet project proposal](https://github.com/OpenWIS/openwis-documentation/issues/186) *“Work with the TC to determine how the smartmet project might operate within the Association in practical terms (eg: where should repos be, how would PMC work etc). Draft a Project Charter and report back to SC in June.”*
        2. JT - MV hasn't joined us today so we can't move forward on this. PR, would you take an action to check that FMI are just not here because they're busy, rather than they are not receiving the invites?
        3. PR - OK - [Action-SC-2017-62 Check that FMI are receiving invites to the SC/TC](https://github.com/OpenWIS/openwis-documentation/issues/323)
    2. WIS 2.0
        1. See [Action-SC-2017-16 Project Charter for WIS 2.0](https://github.com/OpenWIS/openwis-documentation/issues/187)
        2. *Discussion*: does the proposal for OpenWIS Core 5.0 (re OpenWIS Core work plan) subsume the WIS2.0 Project Charter? Can we retrofit a Charter to the existing OpenWIS Core project, e.g. to help formally clarify the split in responsibilities for PMC and TC?
        3. JT - KS, did you produce the project charter for WIS 2.0?
        3. KS - Yes.
        4. PR - It was circulated for review and a few updates made. Then it was used as the basis of the charter for [OPP-6: WIS Djibouti](https://github.com/OpenWIS/openwis-documentation/issues/309), so it has been subsumed.
    3. Weather API / OpenWeather
        1. See [Action-SC-2017-17 Project Charter for Weather API](https://github.com/OpenWIS/openwis-documentation/issues/188)
        2. JT - Some of you are aware that UKMO have been working with NMI to develop a common weather API and that we discussed the hosting of that project by the OpenWIS Association. We are not yet in a position to ask SC to sign-off that project charter.
        3. RGr - Should we make available to the Association the presentation of a couple of weeks ago?
        4. MDA - Ok, I can do that, I have the powerpoint:
            - [Action-SC-2017-63 Circulate the presentation on the Weather API](https://github.com/OpenWIS/openwis-documentation/issues/324)
        5. MDA - What is the position of NMI?
        6. JT - PR, do you know?
        7. PR - No.
        8. JT - I haven't heard any concerns. Are you talking to NMI about partnership?
        9. MDA - It may be beneficial to do that.
        10. JT - Could you do that?
        11. MDA - Yes, ok:
            - [Action-SC-2017-64 Speak to NMI about the benefits of OpenWIS partnership](https://github.com/OpenWIS/openwis-documentation/issues/325)
6. **Update on new Partners**
    1. ECMWF (Associate Partner)
        1. [Action-SC-2017-07 Finalise the ECMWF agreement](https://github.com/OpenWIS/openwis-documentation/issues/178)
        2. [Action-SC-2017-09 Clarify ECMWF taxes](https://github.com/OpenWIS/openwis-documentation/issues/180)
        3. [Action-BM-2017-09 Ask RMI for advice on VAT](https://github.com/OpenWIS/openwis-documentation/issues/291)
        4. [Action-BM-2017-10 Try VAT status enquiry with our Belgian Lawyers](292)
        5. Belgian lawyer instructed to investigate VAT issues
        6. *Informally, Baudouin Raoult suggests that VAT is not payable on subscriptions - only goods and services*
        7. RGr - Still not clear about VAT. The report from the Belgian lawyer is due on the 20th October. Then we should be able to say ECMWF is not subject to VAT.
    2. IMD (Strategic Partner)
        1. [Action-BM-2017-09 Draft response letter to IMD](https://github.com/OpenWIS/openwis-documentation/issues/294) clarifying that they are not paying for software support.
        2. MDA - I sent the agreement drafted by Michael Robbins for Strategic Partner one month ago. Now they are going through internal approvals. They said they would get back in one month, so I will contact them:
            - [Action-SC-2017-65 Contact IMD for an update on progress with the partner agreement](https://github.com/OpenWIS/openwis-documentation/issues/326)
    3. CMA
        1. MDA - I will be visiting CMA at the end of the month. The agenda will include OpenWIS Association and WIS 2.0, so I hope to get them on board.
        2. JT - I need to give you a couple of slides on the new governance structure:
            - [Action-SC-2017-66 Provide slides on new governance structure](https://github.com/OpenWIS/openwis-documentation/issues/327)
7. **Any Other Business**
    1. JT - LM has resigned from BoM and so we will need to elect a new TC Vice-chair. PR, would you please ask the TC for nominations?
    2. PR - Ok:
        - [Action-SC-2017-67 Request VC nominations from TC](https://github.com/OpenWIS/openwis-documentation/issues/328)
    3. Financial matters - bank account
        1. JT - MFI are content to manage the Association funds for now, correct?
        2. RGb - Correct.
        3. JT - SS, you worked with UKMO Cash Accounts team on how to manage the money?
        4. SS - Yes. We would still go through our approval process and we'd have a separate bank account and we'd just instruct our team to make any payments.
        5. JT - You saw that email MDA?
        6. MDA - Yes, I have the email.
        7. JT - You asked if a Belgian AISBL can have its bank account in the UK. Have we asked our Belgian lawyer RGr?
        8. RGr - It must be in Belgium. But not had that in writing yet.
        9. JT - So the UKMO account is a backup if we can't set one up in Belgium. Anything else we want the tax lawyer to look at?
        10. SS - Just the bank account and tax issues.
        11. RGr - We are working with the lawyer on the bank account. The lawyer needs the date of the face-to-face meeting and who was there.
        12. MDA - ING sent a copy of the record of the meeting so I can give you that.
        13. SS - Are the bank account details set up in EE's name?
        14. MDA - Yes, but let us finish the difficult task of setting up the account before we try to change the name.
    4. Financial matters - invoices to Météo France
        1. JT - MDA, you wanted to know how the Association could invoice MF.
        2. MDA - I got the answer from SS; now I want to check the money is available.
        3. MDA - With regard to IMD: once they have signed we will ask for €200k and we will have to invoice them, so what is the process.
        4. SS - We can send them an invoice so that they have the paperwork they need.
        5. MDA - Ok, thank you.
    5. Risks to the Association
        1. JT - We still have a weak risk management process. We all have an action on us to address that, so please take a look at that before the next SC meeting:
            - [Action-SC-2017-20 Risks to the Association](https://github.com/OpenWIS/openwis-documentation/issues/191)
    6. Goals of the Association
        1. Also for the goals; the current goals still relate to OpenWIS-Core rather than the Association and multiple projects. Again, please try to progress the outstanding action for the next SC:
            - [Action-SC-2017-45 Goals for the Association](https://github.com/OpenWIS/openwis-documentation/issues/216) “Each SC delegate should propose 3 goals for the Association (not the OpenWIS-Core project)"
    7. CLA
        1. JT - How is it going with the CLA; has everyone signed it yet?
        2. PR - We can't yet, the CLA review isn't finished. NWS legal came back with some comments, to which Michael Robbins responded, so the ball is in your court KS:
            - [review of CLA, form and process](https://github.com/OpenWIS/openwis-documentation/issues/98)
            - KS [Action-SC-2017-70 Complete the legal review of the CLA](https://github.com/OpenWIS/openwis-documentation/issues/331)
    8. JT - Anyone want to raise any other business?
        1. MDA/RGr/RGb/KS - No.
8. **Next meeting**
    1. JT - I propose we hold the next SC in early December 2017, is that ok?
    2. MDA/RGr/RGb/KS - Yes, ok.
    3. PR - [Action-SC-2017-68 Arrange next SC for first half of December 2017](https://github.com/OpenWIS/openwis-documentation/issues/329)
9. **Summary of recommendations to the Board**
    1. JT - There were no recommendations to the Board, except that we are approving the TC work plan; all agree?
    2. RGr/RGb/KS - Agreed.
10. **Closure of the meeting**
    1. JT - Ok, thank you all for your time and apologies for the late agenda; meeting closed.

---

#### Participants
- JT - Jeremy Tandy, Met Office, UK [UKMO], [delegate], Chair
- RGr - Remy Giraud, Meteo-France, France [MF] [delegate]
- KS - Kari Sheets, National Weather Service, USA [NWS], [delegate]
- RGb - Remy Gibault, Meteo-France International [MFI], [delegate]
- MDA - Matteo Dell'Aqua, Meteo-France, France [MF]
- PR - Paul Rogers, Met Office, UK [UKMO]
- SS - Stacey Squires, Met Office, UK [UKMO], Treasurer

#### Apologies

- MV - Mikko Visa, Finnish Meteorological Institute [FMI], [delegate]
- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM], [delegate]
- SD - Sungsoo Do, Korea Meteorological Administration, Republic of Korea [KMA], [delegate]
- SO - Steve Olson, National Weather Service, USA [NWS]
