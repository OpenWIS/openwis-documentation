---
layout: page
title: OpenWIS Steering Committee 2017 December
---

#### 7th December 2017 - WebEx

---

(The responsibilities of the Steering Committee [SC] are described in Article 13)

1. **Welcome, introductions and approval of agenda**
    1. JT - Welcome everybody.
    2. JT - So, in terms of representation, FMI and BoM are absent, MDA is representing MF in place of RGr. KMA are absent but you will all have seen the email from SD asking me to be their proxy.
    3. JT - So, 5 of 7 organisations are represented; we are quorate.
    4. JT - Is everyone happy with the agenda?
    5. MDA - I would like to add an item about the ING bank account.
    6. JT - Ok, we'll add that item.
2. **Approve previous SC meeting minutes**
    1. JT - Is everyone happy to approve the previous meeting minutes?
    2. JT - Ok, hearing no dissent, the previous meeting minutes are approved.
3. **Clarification of organisational roles within OpenWIS Association**
    1. JT - So, we're straight into amendments to the Internal Rules. We discussed and agreed these rule changes at length at the previous couple of SC meetings and the Board meeting, so now we're just agreeing the wording. I have prepared a couple of Pull-Requests for us to look at. If we are happy to recommend these to the Board then I propose that we obtain that approval by email, rather than wait for the next Board meeting.
    2. **Added new internal rule to (almost) allow default 2-year tenure**
        1. JT - The first one is about increasing the default tenure of SC officers to 2 years; advice from Michael Robbins is that a change would be required to the articles for that, so he suggested [this alternative](https://github.com/OpenWIS/openwis-documentation/pull/337). If you open the pull-request and look at the file change, you can see the new wording for Rule 7 that allows for unopposed elections, which in effect allow an SC chair or vice-chair to remain in office for up to 4 years, without needing to change the articles. So I'll just let you read that.
        2. JT - Are we content to recommend that Rule change to the Board?
        3. MDA - Yes.
    3. **Changes to describe amended governance arrangements**
        1. JT - Ok, so onto the second Rule change. You may recall my presentation at the October SC meeting in which I described the governance changes we had discussed at the SC and Board meetings before that. In this [second pull-request](https://github.com/OpenWIS/openwis-documentation/pull/340) I have taken the flow charts from my presentation and added them to the website. So feel free to have a look at those.
        2. JT - Next, I linked these diagrams into the Internal Rules, to incorporate the changes to project governance, financial management and accounting procedures we have already discussed.
        3. JT - Commit 4 adds a new Rules Supplement that describes the composition and responsibilities of the Board, SC, TC, PMC and project teams that we agreed in principle last time. The new rules make clearer the relationship between the SC and PMC; now the PMC is required to report annually on progress against milestones etc.
        4. JT -  Are you content MDA?
        5. MDA - Yes.
        6. JT - Does anybody want me to read through the details now?
        7. JT - Hearing none, so I won't do that now. The pull-request is public and comments can be made after the meeting.
        8. JT - The next commit is a small addition to Rule 7 that adds a link to the Rule Supplement summarising the governance arrangements.
        9. JT - The final commit cross-references the articles and rules.
        10. JT - Any comments?
        11. MDA - It's ok, it is clear.
    4. JT - Ok, let's vote:
        1. JT - First Rule change - on tenure:
            - RES-OWIS-SC-2017-13:Resolution: vote: 5-0 in favour - Rule change on tenure is recommended. OWIS-RES
        2. JT - Second Rule change - on project governance:
            - RES-OWIS-SC-2017-14:Resolution: vote: 5-0 in favour - Rule change on project governance is recommended. OWIS-RES
        3. JT - Ok, I will recommend those changes to the Board
            - JT - [Action-SC-2017-71 Make recommendations to Board on Rule changes](https://github.com/OpenWIS/openwis-documentation/issues/341)
4. **Election of Vice-Chair of Technical Committee**
    1. JT - We need to appoint a new vice-chair of the TC, now that Leon has departed BoM. Over to you, SO.
        1. SO - I am very pleased to have received the nomination of Benjamin Saclier, Meteo-France, for the position of TC vice-chair and I recommend him to the committee.
        2. JT - Are there any other nominations? Hearing none, let's vote.
            - RES-OWIS-SC-2017-15:Resolution: vote: 5-0 in favour - Benjamin Saclier is elected vice-chair of the TC. OWIS-RES
5. **Completion of Contributor License Agreements (CLA)**
    1. JT - We still need to complete the [review of CLA, form and process](https://github.com/OpenWIS/openwis-documentation/issues/98) so that we can all do [Action-SC-2017-19 Submit completed CLA forms](https://github.com/OpenWIS/openwis-documentation/issues/190). At the moment the action lies with NWS:
        - KS - [Action-SC-2017-70 Complete the legal review of the CLA](https://github.com/OpenWIS/openwis-documentation/issues/331)
    2. KS - We are still waiting to hear back from Legal; getting this through is proving very difficult. SO and I have been considering work-arounds.
    3. JT - At the moment we are holding off asking everyone to sign the CLA because it might change as soon as they do.
    4. KS - We're looking at letting the developers see the US Attorney's concerns and then asking them to sign anyway, so they're not signing on behalf of the US Government.
    5. JT - OK. Any other comments from anyone?
    6. JT - I propose that we finalize the CLA as it stands and get it signed and collected. Any objections? Ok, hearing nothing, we'll go ahead. Could you do that PR?
    7. PR - Yes - [Action-SC-2017-72 Finalize the CLA as-is and obtain signed copies from all contributors](https://github.com/OpenWIS/openwis-documentation/issues/342)
6. **Update on new Partners**
    1. European Centre for Medium Range Weather Forecasting (ECMWF) (Associate Partner)
        1. MDA - We asked our lawyer in Brussels to sort out the VAT. His final answer was that the Association is not subject to VAT; but we still have no response from the Belgian tax authorities.
        2. MDA - So, we can proceed with ECMWF, who are now ready to sign. ECMWF will lose the money if we go past the end of the year. I need the approval of the Association to sign.
        3. JT - I think you already have Board approval.
            - (post meeting note: RESOLUTION-AM-2016-01: Vote: 5-0 in favour – ECMWF membership is Approved. Board Meeting 10th March 2016)
        4. LLG - We could go ahead with the MFI account; no need to wait for the new account to be available.
        5. MDA - Ok.
        6. JT - So we can proceed with the signing.
            - MDA - [Action-SC-2017-77 Sign the agreement with ECMWF](https://github.com/OpenWIS/openwis-documentation/issues/347)
    2. India Meteorological Department (IMD) (Strategic Partner)
        1. MDA - There has also been a lot of progress with IMD. They cannot pay directly to the Association; they will have to pay through the Indian Embassy in Belgium. As soon as we have the bank account, they will be able to pay. We have an agreement that IMD accept, we just need to know the name of the person who will sign. Up to now, Director General's have signed for the existing partners; I have mentioned this to Dr Singh.
        2. JT - Thank you for progressing that - no action or vote is required.
            - (post meeting note: RESOLUTION-BM-2017-12: Vote: 5-0 in favour – IMD application for Strategic Partnership is approved. Board Meeting 20th July 2017)
        3. JT - Any others? MDA, I think you were going to talk to Norwegian Meteorological Institute (NMI)?
            1. MDA - Yes, but I haven't had the time; I will.
                - MDA - [Action-SC-2017-64 Speak to NMI about the benefits of OpenWIS partnership](https://github.com/OpenWIS/openwis-documentation/issues/325)
7. **New Projects**
    1. JT - The role of the Steering Committee is to make a recommendation to the Board regarding any new project proposal. We check that the project proposal is consistent with the purpose of the OpenWIS Association, check that the timelines are appropriate and check that there is enough resource committed to the project; after all, we don't want to start projects that are unlikely to complete successfully. Then we need to propose a Project Management Committee and Project Lead, at least which organisation is responsible for these things. We should also consider the duration of any incubation phase.
    2. JT - So the first proposal is for OpenWIS Djibouti - WIS 2.0 pilot for demo at TECO
        1. See [Action-SC-2017-16 Project Charter for WIS 2.0](https://github.com/OpenWIS/openwis-documentation/issues/187)
        2. See new project repository: [djibouti](https://github.com/OpenWIS/djibouti)
        3. JT - Is this project consistent with the OpenWIS purpose? By definition it looks like it is. Anybody disagree?
        4. JT - Hearing none...
        5. JT - The charter goes into detail on the milestones etc; thank you KS and SO. It needs updating, but there are 2 clear milestones:
            1. Describe the purpose of the project demo to the ITISS meeting in January 2018.
            2. Do the project demo at CBS TECO in March 2018.
        6. JT - Does that make sense to everyone?
        7. JT - Hearing nothing...
        8. JT - So we won't look at the technical details of the project, that is for the PMC, but we do want to know which organisations will be taking part in the project work. At the scrum meetings held so far, UKMO and NWS have participated - is anyone else interested in taking an active part?
        9. MDA - I thought BS was keen. I think MF would like to participate.
        10. JT - That is consistent with what BS has said before. We'll take that as a non-binding commitment from MF and check with BS - thank you MDA.
        11. JT - What about MFI?
        12. LLG - Not in the short term, maybe later.
        13. JT - Ok, thank you. We should check with the absent partners; PR, could you check whether FMI, BoM and KMA would like to be involved?
        14. PR - Ok.
            - [Action-SC-2017-78 Check if others want to be involved in WIS 2.0 pilot](https://github.com/OpenWIS/openwis-documentation/issues/348)
        15. JT - In terms of PMC, we have 3 organisations driving it. SO, what would you recommend, in terms of project lead?
        16. SO - Where we are today, European Dynamics are putting together use cases and mock-ups. In addition NWS is putting together data and metadata. Once we have the mock-ups complete we will create the working proof of concept. We have PMC meetings twice a week.
        17. JT - In terms of PMC membership: UKMO, NWS, MF - who is driving that?
        18. SO - UKMO are project lead.
        19. JT - So, PR, you are leading the project.
        20. PR - Yes.
        21. JT - Ok, let's vote on that; UKMO will abstain:
            - RES-OWIS-SC-2017-16:Resolution: vote: 4-0 in favour, 1 abstention - UKMO will continue as project lead, now formalised. OWIS-RES
        22. JT - So, our recommendation to the Board is that the WIS 2.0 Djibouti pilot project continues under OpenWIS:
            - RES-OWIS-SC-2017-17:Resolution: vote: 5-0 in favour, Continuation of the WIS 2.0 Djibouti pilot project under OpenWIS is recommended to the Board.  OWIS-RES        
        23. JT - Any other comments on this project proposal?
        24. JT - Hearing none, we'll move on to the second proposal...
    3. JT - OpenWeather - Common Weather API
        1. See project proposal paper at: [Action-SC-2017-17 Project Charter for Weather API](https://github.com/OpenWIS/openwis-documentation/issues/188)
            - [User demo](http://labs.metoffice.gov.uk/map/owdemo/)
            - [Admin demo](http://labs.metoffice.gov.uk/map/owdemo/admin.html)
        2. JT - If you open the action and scroll to the bottom, you will find the latest description of what this project is trying to do - open the WORD doc.
        3. JT - Who is already familiar with OpenWeather?
        4. MDA - Yes, I have seen a presentation and I believe it is a good project for the Association.
        5. SO - Is this the project that Richard Carne socialised, which presents each Met Centres data?
        6. JT - That's the one. MFI?
        7. LLG - I have seen a little. Is it using OGC web service standards?
        8. JT - OGC is recognising that Restful web services are becoming more prevalent than OGC services. The objective of this project is to provide a common API for access to data through Restful web services. The candidate Weather API specs are unlikely to be a Web Feature Service, but should comply with OGC standards for spatial data on the web.
        9. JT - Since the aim is to make it easy for people to access weather data, it is a good fit with the purpose of the OpenWIS Association. Anybody disagree?
        10. JT - Ok, hearing nothing... we think it is consistent. The timelines still need to be worked through in more detail. Who is interested in participating and getting involved in the PMC and the work of the project? MF? Would you like to participate?
        11. MDA - Not sure if we would offer manpower or money, but yes, we are interested.
        12. LLG - We would have to look at it; not short term.
        13. MDA - What is short term; a few months?
        14. LLG - 3 to 4 months.
        15. MDA - So, after 2nd quarter next year?
        16. LLG - Yes.
        17. JT - There may be some technical review work in the short term - but you won't be available for development itself?
        18. LLG - If we have some availability later on, how would it work?
        19. JT - Good question. When we set up a PMC it has the contributors on it, so you wouldn't be on it. Later on, the PMC can vote on a member of MFI onto the project. Any member of MFI or any other organisation can contribute anyway. The PMC steers and drives the project, so you need to be committed to be on that.
        20. LLG - Right now we cannot engage, in the short term. If we have more time to give an answer then we can take a look at the project.
        21. JT - NWS?
        22. KS - I'm good with contributing; SO?
        23. SO - This is something we've had discussions about at high level. Yes, we are involved, up and down the Weather Service chain.
        24. JT - Ok, thank you. PR, would you ask FMI, BoM, KMA and ECMWF if they are interested in participating?
        25. PR - Ok.
            - [Action-SC-2017-79 Check if others want to be involved in OpenWeather](https://github.com/OpenWIS/openwis-documentation/issues/349)
        26. JT - I'm not sure they have thought about how long the incubation phase is; PR, could you find out?
        27. PR - Yes.
            - [Action-SC-2017-80 Check what the incubation period is for OpenWeather](https://github.com/OpenWIS/openwis-documentation/issues/350)
        28. JT - Since UKMO are driving this at the moment, I suggest UKMO lead it, so let's vote on that, UKMO will abstain:
            - RES-OWIS-SC-2017-18:Resolution: vote: 4-0 in favour, 1 abstention - UKMO will be project lead. OWIS-RES
        29. JT - And formally recommend to the Board as an OpenWIS Association project? Let's vote:
            - RES-OWIS-SC-2017-19:Resolution: vote: 5-0 in favour - The OpenWeather project is recommended to the Board as an OpenWIS project. OWIS-RES                   
8. **OpenWIS Technical Workplan**
    1. TC Chair (SO) - I am working on a technical roadmap; looking to have a draft in time for the TECO meeting. The roadmap covers 3 main areas:
        1. WIS 2.0 PoC: We've discussed this at the last few TC meetings, including whether to run a Technical PoC as well as the TECO demo we are working on right now. We have some questions for the SC:
            1. Should we consider doing a Technical PoC as well?
            2. Should we socialise the TECO demo beyond the TECO meeting?
            3. And what should we do with the body of work after TECO?
        2. Next, we continue working on OpenWIS v3. NWS is very security conscious and there are a number of components in OpenWIS v3 that have gone end of life. So, we have pushed forward in several areas recently:
            1. OpenAM - upgraded from v12 to v13
            2. OpenDJ - upgraded from v2 to v3
            3. Upgraded to Java 8 and upgraded the Spring Framework in the process as well as modifying the JNDI to make it compatible with Java 8.
            4. Upgraded the application server from JBOSS to Wildfly.
            5. This is all now available in a pull-request to release 3.14.9 and ready for testing once merged.
        3. The last area of the roadmap is to consider more open-source, for example the PoC.
    2. The roadmap should be finalised by March for presentation to the SC in April.
    3. JT - Any questions for SO?
    4. JT - Hearing none. So, there were 3 questions for the SC:
        1. Should we divide the PoC into a User stream and a Technical stream?
        2. What do we do after TECO?
        3. What do we do with the body of work thus created?
    5. JT - I'm expecting TECO to clarify the direction of travel for WIS 2.0. So, after TECO we can decide what we do next.
    6. MDA - I believe you are right JT. During TECO there will be side events on WIS 2.0. Than after that there will be the Executive Council in June; maybe another chance to demo what we are doing for WIS 2.0.
    7. Does that make sense, SO?
    8. SO - Yes.
    9. JT - Thank you to the TC chair for that input.
9. **Risk Management**
    1. JT - Proposed risk management process; we are short of time now, so I propose we start that conversation offline.
        - [Action-BM-2017-03 Draft Risk Register for Association](https://github.com/OpenWIS/openwis-documentation/issues/227)
        - [Example Risk Register](https://github.com/OpenWIS/openwis-documentation/projects/4)
        - [Action-SC-2017-20 Risks to the Association](https://github.com/OpenWIS/openwis-documentation/issues/191)
    2. KS - Yes.
    3. MDA - Start the next SC with the Risk item.
    4. JT - Yes, good idea:
        - [Action-SC-2017-81 Initiate discussion on Risks to Association](https://github.com/OpenWIS/openwis-documentation/issues/351)
10. **Goals for the Association**
    1. JT - The same goes for the Goals; let's try to make some progress offline:
        - [Action-SC-2017-45 Goals for the Association](https://github.com/OpenWIS/openwis-documentation/issues/216)
11. **Entry into International Yearbook**
    1. JT - We've received a request for information for [Entry into International Yearbook](https://github.com/OpenWIS/openwis-documentation/issues/338)
        1. JT - We've taken no action. We would be visible somewhere, for no obvious purpose. Is this a priority? I'm not inclined to put effort into this.
        2. MDA - I think maybe we are in this yearbook and they are asking for an update.
        3. JT - Ok, let's check that and update if necessary:
            - PR - [Action-SC-2017-82 Check the Yearbook entry; update if it exists](https://github.com/OpenWIS/openwis-documentation/issues/352)
12. **Outstanding Actions**
    1. JT - Please also check the outstanding actions and progress offline if possible:
        - MDA - [Action-SC-2017-34 Promotion at WMO Exec Council 2018](https://github.com/OpenWIS/openwis-documentation/issues/205)
        - RGr - [Action-SC-2017-51 Money transfer tax](https://github.com/OpenWIS/openwis-documentation/issues/222)
        - SO - [Action-SC-2017-57 Reword the text of the TC Briefing to the SC](https://github.com/OpenWIS/openwis-documentation/issues/281)
        - SH - [Action-BM-2017-13 Check that UKMO could bill the Assoc for work](https://github.com/OpenWIS/openwis-documentation/issues/295)
        - JT - [Action-BM-2017-14 Define the mechanisms/rules for financial support of projects](https://github.com/OpenWIS/openwis-documentation/issues/296)
13. **Any Other Business**
    1. **Bank Account**
        1. MDA - We have been trying for the past year to set up a bank account in Belgium. We asked our lawyer to help, so now we have an account number but we need to fill-in a new form. Currently we require 3 people, MDA, JT, SH, to be allowed to use the account. If we want JT and SH to use the account, then JT and SH will have to do a face-to-face meeting in a Belgian branch of ING; a London office is not valid in Belgian law.
        2. MDA - I spoke to ING this morning; they said we can put only MDA's name against the account, because MDA already had a face-to-face meeting in Belgium. We can then add JT and SH later after they have the face-to-face.
        3. MDA - We require an account quickly to help sign-up ECMWF and IMD.
        4. JT - Ok, so an AISBL has to have an account in Belgium.
        5. JT - It makes sense to proceed with one name.
        6. JT - SH and myself will go to Belgium in the new year.
        7. MDA - This afternoon I can remove your names and send the form to ING; we will have the account in 5 days.
        8. JT - UKMO would seek to recoup the cost of the trip from OpenWIS Association.
        9. MDA - That's no problem.
        10. JT - OK, let's vote: Are we all happy to set up the account with MDA as sole name and add JT and SH later?
            - RES-OWIS-SC-2017-20:Resolution: vote: 5-0 in favour - Recommendation to the Board - Set up the account with MDA as sole name and add JT and SH later. OWIS-RES
            - MDA - [Action-SC-2017-73 Set up the bank account with a single signatory](https://github.com/OpenWIS/openwis-documentation/issues/343)
        11. JT - So, MDA, you'll then work with MFI to transfer the OpenWIS funds?
        12. MDA - Yes.
            - MDA - [Action-SC-2017-74 Move the funds from the MFI account to the ING account](https://github.com/OpenWIS/openwis-documentation/issues/344)
        13. JT - How do we arrange the meeting?
        14. MDA - I will send you the contact details of the agency in Brussels.
            - MDA - [Action-SC-2017-75 Send JT and SH the contact details for the agency](https://github.com/OpenWIS/openwis-documentation/issues/345)
        15. JT - Ok, is everyone ok with OpenWIS Association funding the trip?
            - RES-OWIS-SC-2017-21:Resolution: vote: 5-0 in favour - Recommendation to the Board - OpenWIS Association will fund the trips of JT and SH to Brussels, to become signatories for the bank account. OWIS-RES
        16. JT - [Action-SC-2017-76 Travel to ING Brussels for face-to-face meeting](https://github.com/OpenWIS/openwis-documentation/issues/346)
14. **Next meeting**
    - JT - Next SC will be late Feb or early March 2018.
15. **Summary of recommendations to the Board**
    1. JT - We've run out of time, so we won't go through the Board recommendations here, they will be listed in the minutes:
        1. The recommendations to the Board are as follows:
            - RES-OWIS-SC-2017-13:Resolution: vote: 5-0 in favour - Rule change on tenure is recommended to the Board. OWIS-RES
            - RES-OWIS-SC-2017-14:Resolution: vote: 5-0 in favour - Rule change on project governance is recommended to the Board. OWIS-RES
            - RES-OWIS-SC-2017-17:Resolution: vote: 5-0 in favour, Continuation of the WIS 2.0 Djibouti pilot project under OpenWIS is recommended to the Board.  OWIS-RES
            - RES-OWIS-SC-2017-19:Resolution: vote: 5-0 in favour - The OpenWeather project is recommended to the Board as an OpenWIS project. OWIS-RES
            - RES-OWIS-SC-2017-20:Resolution: vote: 5-0 in favour - Recommendation to the Board - Set up the account with MDA as sole name and add JT and SH later. OWIS-RES
            - RES-OWIS-SC-2017-21:Resolution: vote: 5-0 in favour - Recommendation to the Board - OpenWIS Association will fund the trips of JT and SH to Brussels, to become signatories for the bank account. OWIS-RES
        2. The following resolutions from previous meetings are also relevant to this meeting:
            - RESOLUTION-AM-2016-01: Vote: 5-0 in favour – ECMWF membership is Approved. Board Meeting 10th March 2016
            - RESOLUTION-BM-2017-12: Vote: 5-0 in favour – IMD application for Strategic Partnership is approved. Board Meeting 20th July 2017
16. **Closure of the meeting**
  - JT - Anything else? Nothing? Ok, the meeting is now closed. Thank you.

---

#### Participants
- JT - Jeremy Tandy, Met Office, UK [UKMO], [delegate], Chair
- KS - Kari Sheets, National Weather Service, USA [NWS], [delegate]
- LLG - Loic Le Gallou, Meteo-France International [MFI], [delegate]
- RGb - Remy Gibault, Meteo-France International [MFI]
- MDA - Matteo Dell'Aqua, Meteo-France, France [MF], [delegate]
- SO - Steve Olson, National Weather Service, USA [NWS]
- DW - Dominic Woollatt, Met Office, UK [UKMO]
- PR - Paul Rogers, Met Office, UK [UKMO]

#### Apologies

- RGr - Remy Giraud, Meteo-France, France [MF] [delegate]
- MV - Mikko Visa, Finnish Meteorological Institute [FMI], [delegate]
- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM], [delegate]
- SD - Sungsoo Do, Korea Meteorological Administration, Republic of Korea [KMA], [delegate]
