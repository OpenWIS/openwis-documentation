---
layout: page
title: OpenWIS Technical Committee 2018 May
---

#### 29th - 30th May 2018, Helsinki, Finland

---

1. **Opening and introductions**
    1. Steve Olson (SO) (TC chair) welcomed all present, and Weiqing Qu (WQ) and Giorgios Triantafyllidis (GT) who joined remotely.
    2. The attendees were:
        - SO - Steve Olson, National Weather Service, USA [NWS], Chair
        - BS - Benjamin Saclier, Météo-France, France [MF], Vice-chair
        - MP - Mikko Partio, Finnish Meteorological Institute, Finland [FMI],
        - RGb - Remy Gibault, Météo-France International [MFI]
        - SD - Sungsoo Do, Korea Meteorological Administration, Republic of Korea [KMA]
        - JT - Jeremy Tandy, Met Office, UK [UKMO]
        - RGr - Remy Giraud, Météo-France, France [MF]
        - MV - Mikko Visa, Finnish Meteorological Institute [FMI]
        - WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM],
        - GT - Giorgios Triantafyllidis, European Dynamics, [UKMO]
        - DP – David Podeur, Météo-France, France [MF]
    3. Apologies
        - DW - Dominic Woollatt, Met Office, UK [UKMO]
2. **Layout of agenda Items**
    1. There were no issues or comments about the format of the agenda.
    2. SO – the key point is the focus on quality. There are key aspects that are best practise and we should be complying with. The aim is to look at ways in which we improve.
3. **Technical infrastructure: status and plan for future management and operation (including any costs and costs of improvements for SC approval)**
    1. George Triantafyllidis (GT) from European Dynamics (ED) joined remotely to give an overview of their experience of the current CI environment that was used for the WIS2 PoC and development of OpenWIS 3. The presentation is here - https://github.com/OpenWIS/openwis-deploy/wiki/OpenWIS-CI-CD
    2. Key points mentioned by GT are:
        1. Benefits - less risk, reduced effort, improved code quality, and automated analysis and reporting.
        2. Afterthoughts – licensing and maintenance costs. Free sometimes have limitations or require the Integration of tools for added functionality, which increases of maintenance effort. Commercial platforms still require DevOps for maintenance, but are usually more feature-rich and easy to use. As an example, the Jenkins build took 97 iterations.
        3. No DevOps, so not available to fix pipeline immediately.
        4. Test coverage is small – 2% to 3%. Higher coverage possible with DevOps.
        5. No build for v3.14.8. It is available but disabled. This needs to be treated as a risk when changes are merged.
    3. SO - I have a couple of questions before handing over to others. The disabled branch, is that 3.14.8 only?
        - GT - It is for the dev branch only. Tests would be Ok to run locally.
    4. SO - how much resource to customise/enable?
        - GT - Not much. Can be done easily.
    5. SO - Assuming that only 2% to 3% code being tested….
        - GT - A business critical project usually has 80% coverage. So, if quality is important, then effort need to be put in to write test cases. Also, a complex application, for example the metadata deletion issue, a test case should be written. So, if a huge project a huge amount of effort.
    6. SO - What should be the nominal amount to shoot for?
        - GT - Depends on the code you have. For OpenWIS a lot of code to be tested. So, 50% excluding UI as we use the old version of Angular.
    7. RGr - CI is useful when there is continuous development. This is not the case. So what would be useful in the future?
        - BS - Stop dev and then start again.
        - RGr - No we don't envisage OpenWIS 3 dev in the near future.
        - JT - We discussed earlier we need to manage the risks, security and ensuring compliance with GDPR (i.e. legislation changes outside of WMO). So, we need to fix regulatory, security and operational things.
        - RGr - Do we need a CI environment for this maintenance?
        - JT - we agreed to maintain for 6 years.
        - BS - Yes, there will be fewer developments, but we agreed to keep OpenWIS 3 for 6 years.
        - RGr - OK, I may have expressed too strongly. OK, so we make few changes as possible.
        - JT - Agree that we should not invest in something that has a limited future for testing.
        - RGr - OK, we are saying the same thing.
    8. JT - We do not need to increase test coverage. Have a specific test for specific bug as it turns up.
        - BS - Having the bulk metadata issue may need a test.
        - JT - Not sure whether the test coverage is referring to functional tests? You are referring to non-functional tests.
        - SO - Noted that this is about quality and noted that this for future development. We should consider as used operationally.
        - JT - If we were starting this again, I agree. However, as we are not doing active development, I don't think we should do this. UKMO will not be paying for increasing test coverage.
        - RES-OWIS-TC-2018-01 - No effort to be focused on increasing test coverage for OpenWIS 3. OWIS-RES
    9. SO - The CI environment. How big should the environment be? Is it the right size, should be increased or decreased?
        - GT – I think it is good. Deploy and build in 1.5 minutes. Good for the needs of the project.
        - RES-OWIS-TC-2018-02 - Keep the CI environment at the current size. OWIS-RES
    10. SO – Any other questions for Giorgios?
        - No other questions from the attendees.
        - RES-OWIS-TC-2018-03 - continue to maintain capability to provision virtual servers for OpenWIS projects, as required. OWIS-RES
4. **Code of conduct and CLA compliance: status, review, and recommendations**
    1. Review of code of conduct and CLA compliance on web site
        1. SO - We have a CLA is place that has been legally vetted. The next step is to get internal sign-up. JT and RGr, what level does sign-up need to be, individual or organisation?
            - JT - We have had advice that it should be at organisation level.
            - RGr - OK too.
        2. SO - what level of authority does it need to be?
            - JT - Someone with authority to give Intellectual property (IP) away.
        3. SO - What is the time-scale in which sign-up be achieved?
            - JT - last year.
            - SO – So how about we do this is 2 months, by end of July 2018?
            - RES-OWIS-TC-2018-04 – Outstanding Contributor Licence Agreements (CLA) to be signed by end July 2018 OWIS-RES
            - [Action-TC-2018-19 ensure that all outstanding CLAs are completed](https://github.com/OpenWIS/openwis-documentation/issues/456)
        4. SO – On-line form. A question of process. How is it sent out; who would sign it? And how is it collated and stored? Clarity is needed on the CLA process.
            - [Action-TC-2018- 20 check CLA process with Paul Rogers](https://github.com/OpenWIS/openwis-documentation/issues/457) -
        5. JT - could we use a Météo France safe?
            - RGr - Basically a paper copy is stored somewhere. May be a rule change is needed.
        6. JT - We could buy some on-line storage.
            - RGr - Then a virtual key and virtual safe is needed.
            - JT - Yes.
            - RGr – Is DropBox good enough?
            - JT - Yes, as long as it is not publically accessible. The paid for version for £10pm with 2 Tera bytes of storage and easy to use collaboration tools. But has a minimum of 3 users, so £30pm.
            - RGr - So we could have 3 users.
            - JT - Community Manager.
            - RGr - Both chairs and Community Manager.
            - JT - Yes.
            - RGr – We could create 3 email addresses.
            - JT – Yes.
            - RGr- SC Chair, SC Vice Chair and Community Manager.
            - RGr - RGb, can you create email addresses?
            - RGb - Yes I can and change, also create aliases.
            - RGr - This would work.
            - JT - The problem is to keep the email account attended.
            - RGb - Can create an alias to a personal email account. This is what we did before.
            - RGr – Agree that we should proceed.
            - RES-OWIS-TC-2018-05 – The TC agreed the adoption of the secure paid for DropBox on-line storage service to store completed CLAs. OWIS-RES
            - [Action-TC-2018-21 set up emails and secure dropbox service](https://github.com/OpenWIS/openwis-documentation/issues/458)
            - RES-OWIS-TC-2018-06 – The TC agreed that the secure DropBox service for storing completed CLAs would be accessed by the OpenWIS Chair, Vice Chair and the OpenWIS Community Manager. OWIS-RES
    2. Is the code of conduct being applied?
        1. SO - We have our scope, enforcement and attribution. Is there is anything that needs to change or be added?
        2. JT - noted that when people are signing the code of conduct they are also committing to the technical rules.
        3. No further responses from attendees. Therefore, the review of the code of conduct is complete.
   3. Is the code of conduct being followed?
       1. JT - part of the Code of Conduct is to challenge anyone that is not following it by raising it with the TC Chair.
       2. What are our recommendations, if any?
           - SO – So amplify on web site statement?
           - JT - Agree. Alter the first paragraph of the Code of Conduct for initial reporting of poor conduct to TC Chair and for TC Chair to raise issues conduct to SC, requesting resolution if required.
           - RES-OWIS-TC-2018-07 - Alter the first paragraph of the Code of Conduct for initial reporting of poor conduct to TC Chair and for TC Chair to raise issues conduct to SC, requesting resolution if required.
           - [Action-TC-2018-23 alter code of conduct rules on the website](https://github.com/OpenWIS/openwis-documentation/issues/466)
5. **Technical rules compliance: status, review, and recommendations**
    1. Review of technical rules
        1. SO - The action from the last meeting was to review rules. The agreement is to review and apply updated documentation on technical rules to web site.
        2. The following actions were reviewed and updated:
            - [Action-SC-2017-01 Update Technical Rules to clarify roles](https://github.com/OpenWIS/openwis-documentation/issues/172)
            - [Action-SC-2017-03 Define 'patchable'](https://github.com/OpenWIS/openwis-documentation/issues/174)
            - [Action-SC-2017-4 Add test coverage metrics to Technical Rules](https://github.com/OpenWIS/openwis-documentation/issues/175). It was agreed to close this action.
            - [Action-SC-2017-05 Add software quality statement to Technical Rules](https://github.com/OpenWIS/openwis-documentation/issues/176)
        3. A new action to align web site page information on technical rules, code of conduct and development process was agreed.
            - [Action-TC-2018-13 re-align web site pages on technical rules and development process](https://github.com/OpenWIS/openwis-documentation/issues/449)
        4. Agreed that technical rules on how disputes on breach of technical rules are resolved should be added.
            - [Action-TC-2018-14 update technical rules with steps for dispute resolution](https://github.com/OpenWIS/openwis-documentation/issues/450)
        5. Obtain latest position on investigation on testing and test metrics, i.e. [Action-SC-2017-24 Publish test results](https://github.com/OpenWIS/openwis-documentation/issues/195)
        6. JT – A review of goals for OpenWIS-Core were written when we developing the OpenWIS v4, so may not be relevant. Therefore all agreed closure of:
            - [Action-SC-2017-40 Update Goal 6](https://github.com/OpenWIS/openwis-documentation/issues/211)
            - [Action-SC-2017-41 Update Goal 7](https://github.com/OpenWIS/openwis-documentation/issues/212)
            - [Action-SC-2017-42 Update Goal 8](https://github.com/OpenWIS/openwis-documentation/issues/213)
            - and opening a new action: [Action-TC-2018-15 consider new goals for quality](https://github.com/OpenWIS/openwis-documentation/issues/451)
        7. JT - Who is the Project Lead for OpenWIS Core?
            - SO - Leon was but when he left, there was no formal replacement.
            - JT – Up to the TC to decide who is to be the Project Lead.
            - [Action-TC-2018-16 appoint project lead for openwis core](https://github.com/OpenWIS/openwis-documentation/issues/452)
        8. Agreed close of [Action-SC-2017-32 FOSS4G](https://github.com/OpenWIS/openwis-documentation/issues/203)
6. **Project design authority, standards compliance, and release management: status, review and recommendations**
    1. Review of project design authority, standards compliance and release management
        1. SO – Looking for guidance on standards and on what has happened to date.
            - JT – No specific standards are set. It is possible to set specific standards. The TC can do this.
            - JT – Propose that standards are set where multiple project can use the same standards.
        2. Agreed to develop an approach to technical standards:
            - [Action-TC-2018-17 create rules supplement on approach to technical standards](https://github.com/OpenWIS/openwis-documentation/issues/453)
        3. Agreed that the release management process should be accessible:
            - [Action-TC-2018-18 ensure that release management documentation is accessible](https://github.com/OpenWIS/openwis-documentation/issues/454)
            - JT – Did projects follow the release management process?
            - SO – Yes. Only two projects underway.
7. **Key risks and issues of individual OpenWIS Projects: advice to the Steering Committee**
    1. Review of current OpenWIS projects
        1. SO – the PMC captured the risks in project, as follows:
            1. ExceltoWIS – no risks
            2. Only other area of risk is on quality. There is a list of areas where quality is referenced in Github and the web site. A thought is that to use a graphic that pools this information in one place to make it easy to reference and access quality.
                - DP - Metrics as well?
                - JT - who is this aimed at?
                - SO - Existing Developers.
                - JT - You are defining quality at a broader level. Let's try to focus making it useful for current developers.
                - JT - The previous action to tidy up the web site will help? The goal is to make it repeatable, like ISO?
                - SO - Yes that action would help.
                - JT - Is there a preference to having a graphic?
                - SO - For example, under 'Project Governance' or 'Quality Criteria' is where it could be represented.
                - JT - This could be relevant to a specific project such as OpenWIS Core.
                - SO - Or link it to OpenWIS 'Project Governance'
                - JT - What is your preference?
                - SO - Link it to 'Quality Criteria' under 'Project Governance'
                - Agreed to develop a repeatable process for quality:
                    - [Action-TC-2018-19 create a web page that shows a repeatable process](https://github.com/OpenWIS/openwis-documentation/issues/455)
8. **Forum**
    1. SO - Approval gained to purchase Discourse.
        - JT - So will mean no installation is needed?
        - SO – Configuration only.
    2. RES-OWIS-TC-2018-08 – The TC agreed that the approach set out previously in [Action-TC-2017-07 Forum on Discourse](https://github.com/OpenWIS/openwis-documentation/issues/157) should be adopted and if in doubt to go simple. OWIS-RES
        - [Action-TC-2018-24 set up forum using discourse](https://github.com/OpenWIS/openwis-documentation/issues/468)
9. **Creation of overall plan**
    1. The overall plan of the following study projects to explore aspects of WIS2 as discussed at the PMC was agreed to be commenced in the next 12 months:
        1. Schema.org led by UK Met Office
        2. Trust model led by NWS
        3. Future of metadata led by UK Met Office
        4. AMQP led by Météo France
    2. It was agreed that OpenWIS 3 should be maintained until 2024 and the following work undertaken in the next 12 months:
        1. Work with TT-GISC to make use of the global cache (ALL)
        2. Identify existing Openwis documentations (ALL)
        3. Use of discourse forum for Openwis association (NWS)
        4. Develop guidance on Openwis 3 (NWS & MF)
        5. Assess the end of life position of openwis3 components (NWS)
        6. Review setup and installation guide (KMA & MF)
        7. Check OpenWIS last version on CentOS 7 (KMA & MF)
    3. It was agreed that work on the PoC was complete and the project should be closed.
    4. It was agreed that this plan and approach should be recommended to the SC.
        - RES-OWIS-TC-2018-09 – TC agreed that the discussed work plan should be submitted to the SC. OWIS-RES
10. **Any Other Business**
    1. David Podeur requires a 10-minute demo on the PoC
        - [Action-TC-2018-09 arrange a demo of the WIS2 PoC at a scrum with ED](https://github.com/OpenWIS/openwis-documentation/issues/445)
    2. Agreed that it is useful for David Podeur to review the OpenWIS website and technical rules to provide feedback to Steve Olson in restricting the web site page and content. [add action when David Podeur's github account is open]
    3. BS - It would be good to have information from European Dynamics (ED) in deploying the PoC to inform future projects.
        - [Action-TC-2018-10 obtain information from ED on effort for WIS2 PoC](https://github.com/OpenWIS/openwis-documentation/issues/446)
    4. RGr - Ask ED to provide a machine image of the VMs used for the PoC demo (to enable us to re-use (incl. any documentation and passwords).
        - [Action-TC-2018-11 Machine image of the WIS2 PoC from ED](https://github.com/OpenWIS/openwis-documentation/issues/447)
    5. JT – It would be good to ask ED to deploy the PoC onto AWS servers that UK Met Office manages to enable an engineer to understand how to deploy OpenWIS.
        - [Action-TC-2018-12 deploy the WIS2 PoC on AWS servers in UKMO](https://github.com/OpenWIS/openwis-documentation/issues/448)
    6. RGr - Environment for the APMQ study project – will this need to be added to OpenWIS?
        - JT – The SC would task the TC to with setting up the environment. Would Météo France want to supply?
        - RGr – costs would be zero as Météo France would fund.
        - JT – Do you want to the OpenWIS Association to fund anything?
        - RGr – Would the TC have any recommendations?
        - BS – It would be good if the OpenWIS Association funds an environment in the long term.
        - JT – agree in principle that OpenWIS Association should have environments for its projects.
    7. RES-OWIS-TC-2018-10 – TC should maintain capability to provide virtual servers for OpenWIS projects, as required as provide the technical specifications for the required environment(s). OWIS-RES
11. Close
