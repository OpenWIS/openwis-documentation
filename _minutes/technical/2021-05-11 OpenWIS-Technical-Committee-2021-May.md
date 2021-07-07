---
layout: page
title: OpenWIS Technical Committee 2021 May
minuteOwner: technical
---

#### 11th May 2021, Teleconference

---
1. **Welcome and introductions**
    - Steve Olson (SO) (TC chair) welcomed all present.

    *- The attendees were:*
    •	SO - Steve Olson, National Weather Service, USA [NWS], Chair
    •	DP - David Podeur, Météo-France, France [MF], Vice Chair
    •	YG - Yves Goupil, Météo-France, France [MF]
    •	WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM]
    •	JA - Jude Anthonisz, OpenWIS Association Secretariat
    •	JR - Jeyoung Ryu (KMA)
    •	SD - Sungsoo Do, Korea Meteorological Administration [KMA]
    •	BH - Boram HEO, Korea Meteorological Administration [KMA]
    •	DP - David Podeur, Météo-France, France [MF]
    •	JT - Jeremy Tandy, UK Met Office [UKMO]
    •	IE - Ian Edwards, [OpenCDMS]
    •	FB - Fred Branski, National Weather Service, USA [NWS]
    •	MG - Marc Giannoni, National Weather Service, USA [NWS]
    •	ZZ - Zhan Zhang, National Weather Service, USA [NWS]
    •	YR - YK Reddy [IMD]
    •	KSr - Kuldeep Srivastava, India Meteorological Department (IMD)

    *- Not present:*
    •	RGb - Remy Gibault, Météo-France International [MFI]
    •	MP - Mikko Partio, Finnish Meteorological Institute, Finland [FMI]
    •	BR – Baudouin Raoult [ECMWF]

2. **Technical infrastructure: status and plan for future management and operation (including any costs and costs of improvements for SC approval)**

*2.1 Current known limitations (DP)*
  - Travis CI integration not working
	-	GitHub issues, in particular, when installing v3.15.
	-	GitHub account is legacy and paid by UK Met Office. So, costs should be picked up by the Association and
    agree the level of service/plan that is needed from Github.
	-	Need to agree which plan to go forward with when the current Bronze (legacy plan expires).
	-	Not in a position to decide now and postpone for one year, analyzing usage and need.

  - JT - need to resolve sooner than next year.
  - DP - If this this is possible?
  - JT - UKMO happy to carry on paying for the present time. So don’t necessarily need the SC to approve in
    the short term.
  - DP - Need to do some analysis.
  - JT - I think the options and decision will be between choosing from Free, Team and Enterprise.
  - MG - Is ‘automation’ mean Travis?
  - JT - Based on the information I am sharing from GitHub, yes.
  - DT - So we need to assess how many minutes will be used?
  - JT - We may not be using minutes at all.  It may be useful for DT to speak to Tom Kralidis to move away
    from Travis.
  - DP - The aim is to resolve in 3 months.

  [ACTION DP to evaluate and recommend (including talking to Tom) re the potential to adopt GitHub automation instead of Travis](  https://github.com/OpenWIS/openwis-documentation/issues/622)

  - MG - Github automation needs to be able to support Java.
  - JA - any dependency between evaluating v3.15 and the need for a CICD environment.
  - SO - No.

*2.2 Do we anticipate any projected costs this year for Technical infrastructure? **

  - SO - Depends on outcome of evaluation of GitHub 

*2.3 Is there anything we feel we need to change for Technical Infrastructure? **

  - SO - Depends on outcome of evaluation of GitHub.

3. **Review of code of conduct and CLA compliance on OpenWIS Association web site**

  - SO - Any changes required?
  - WQ - No
  - All - No

*3.1 Is the code of conduct being applied?*

  - SO - Yes.  However, discussion with NWS ongoing.
  - FB - Last update I recall was in December 2020. 
  - JT - We’ve been asking our Legal team since December.  However, the team have been busy.  However, he is
    happy to have  call with NWS. So, is this approach OK for you?
  - FB - Yes, I can facilitate setting up a meeting by informing Derrick.
  - JT - I’ll send a message to Michael, Derrick and yourself (cc Jude) to get a slot in the diary.
  - SO - Is this the most recent version?  

[ACTION - SO to establish whether this is the current version](https://github.com/OpenWIS/openwis-documentation/issues/494#issuecomment-839613376)



4. **Technical rules compliance: status, review, and recommendations**

*4.1 Review of technical rules* 
	- Are we complying with all technical rules right now?  - SO reviewed the current arrangement.  Any
    changes needed?
  - All - No 
  - What’s the status of the technical rules section? 
	- SO - All being used, less actively as OpenWIS is in maintenance mode.
	- JA - should these rules apply to OpenCDMS
	- SO - in my opinion, yes.
	- JT - In principle, I agree.  It may be worth asking each project to see whether there are exceptions.
	- JT reviewed the rules and proposes re wording the scope to state ‘… should ad-hear to the technical
    rules...’ and ‘…explain the alternative, with reason(s)…’
	- JT - I would encourage projects to work with the TC to evolve the technical rules.
	- SO - agreed.
	- JT – It could also be useful for projects to contribute code and workflows.
	- All – Agreed.

[ACTION – SO to speak to the OpenCDMS Project (Ian) regarding potential changes to technical rules and document why (if any) different rules are being adopted]( https://github.com/OpenWIS/openwis-documentation/issues/453#issuecomment-839615428)
 
*4.2 Review of Rules Supplement,  Ties to Issue #453 **

  - SO – The last aspect was to provide examples of code styles.  I am progressing this, along with
    identifying metadata templates. I am to close this later this year. 

*4.3 Review of Goals and Metrics.  Ties to issue #451 **

  - SO - these have been updated with additional metric to reflect that we follow quality and best practices.
  - SO - any additional goals and metrics that should be considered?
  - JT - The list of goals and metrics are short is because we were differentiating between those for
    Association and projects. 
  - WQ - For projects it could be difficult to have goals and metrics for all projects.
  - JT - I wanted to make sure we were clear that we were thinking out the difference.  May be it’s a non-
    issue.  Discuss at SC?
  - SO - I Agree that goals and metrics should be different and a discussion at the SC.

- SO - In summary, some updates are needed to the development and release processes to reflect the new CICD
  environment.  These updates are in progress of being made by BS and me.  I will agree the revisions with a future TC and then publish.
- SO - Any questions?
- All - None.

*4.4 Review of Quality Measures (see issue #451)*

  - SO - were a little behind documenting the installation process.  This is now updated (for 3.15). More to
    do on development and release cycle documentation.  A draft is in place and hope to complete in the coming months.
  - SO - Any questions?
  - All - No

5. **Project design authority, standards compliance, and release management: status, review and recommendations**
  - Discussion on updated guidance for OpenWIS development and release management
  - Review of project design authority, standards compliance and release management
  - Are there adjustments needed?
  -	What are our recommendations, if any? 

  - SO - will have updates to these sections. Aiming for end June 2021.
  - SO - Any questions?
  - All - No

6. **Key risks and issues of individual OpenWIS Projects: advise the Steering Committee.**

- Review of OpenWIS, Excel2WIS and WIS2 OpenWIS Association projects 
	- What are the risks associated with each of these projects?
	- Given current budgets, how do we prioritize ongoing work across all projects?
	- How do we ensure quality of our work?
	- Use of new CI/CD environment for reports
	- How do we show if we’ve met all milestones?
	- And did we do what we said we would do? 

*6.1 OpenWIS 3.x*
  - SO - Risk assessment via Zhang (ref 365) which was discussed at the PMC on 10 May 2021.            Are
    there any other risks that we need to be aware of an incorporate into the plan?
   - JT - Does this cover the CICD environment?
  - MG - This covers middleware components to keep the software up to date. A lot of components but a lot
    work has been done.
  - JT - the risk is then that the maintenance work, outstrips resources available.
  - MG - Yes. A lot of things age.
  - JT - I am not expecting to take code modules into WIS2.0.  So, the risk if maintenance ramps up between
    now and WIS 2.0.
  - MG - An item for the risk is the tool chain, so it we move away from Java.  However, the current tool
    chain is pretty modern.
  - JT - Yes should keep a track of this risk.
  - SO - agreed. JT - is there anything that would prevent us from building collaborate?
  - SO - Biggest risk is the security service.  The middleware RFP will hopefully address this issue.
  - JT - the risk is then than NWS will not be able to operate the software?
  - SO - Any other risks?

*6.2 ExceltoWIS*

  - SO - No activity, but are there any risks?
  - All - No
  - JA - Is this being used?
  - SO - Yes for metadata.
  - JT - No risks but will need to be updated.
  - JA - will need a life cycle plan?
  - MG - it’s a small helper tool and would need to follow the changes to the metadata standards. 	
  - JT - There would a big change once the WIS 2.0 related metadata standards are announced.
  - SO - Could set up a charter in the lead up to new metadata standards.
  - JT - There are other initiatives underway to validate metadata and although we need to keep ExceltoWIS
         we need to keep an eye on its lifecycle.  

[ACTION – SO include annual evaluation of ExceltoWIS in similar for OpenWIS 3.x] (https://github.com/OpenWIS/openwis-documentation/issues/623 and https://github.com/OpenWIS/openwis-documentation/projects/15)

*6.3 WIS2.0 related projects*

  - SO – What shall we do with the current WIS 2.0 related projects?
  - All - WIS2.0 evaluation projects – sunset all. 

 [ACTION – SO to update Project Charters](https://github.com/OpenWIS/openwis-documentation/issues/624)


  - JT - We also need to think about starting new projects for WIS2 evaluation and their resourcing.  This
    needs to be discussed at SC.

  - *ACTION - SO to add to report to SC of May 2021 and re OpenCDMS, ask Ian re risks*

  - SO - Any other projects to be adopted beyond OpenCDMS and WIS 2.0 projects. 
  - JT - not aware of any projects at present

*6.4 OpenCDMS*

  - IE - gave a presentation. Key points:
	  - More information available on opencdms.org
	  - Technical approach – 3 layers (data, application, and presentation)
	  - Data layer – many sources. So, aim is to make inter-operable.
	  - Work in 2020: prototyping, process library, review of existing data models and status report.
	  - Roadmap 2021 to 2026 influenced by INFCOM and SERCOM.
	  - Plans for 2021 – User stories, additional processes, create a test database, implementation of core,
      initial UI and status report by December 2021. 
  - SO - Could you add Project Charter information to enable it to be published on the OpenWIS website?
  - IE - OK, I can show you where this information is already available.
  - DP - Can you let us know who is on the OpenCDMS project and what they do?
  - IE - Presented information from the OpenCDMS site.
  - JT - Would be keen understand parrallel initiatives of cloud development.
  - IE - OpenCDMS is open source.  So, cloud will happen in parallel. At present, in discussion stage and no
    commitments. Separating the software from cloud deployment.  Some discussion with AWS for prototyping.  There is commitment to AWS nor does AWS expect any from OpeCDMS.  
  - IE- software is completely agnostic at present. However, there will be some hardening as we move to a
    production capability.  Atleast 12 months away before private sector involved.

  - JT - An action for the project team has a task to draft an MOU with AWS as requested from the SC.
  - IE - Yes.  OpenCDMS is not dependent or critical to this aspect. Can join the OpenCDMS discussions if
    interested.
  - JT - Can you share the location for these discussions?
  - IE - I will set up a space for these discussions, i.e. here https://github.com/opencdms/opencdms-cloud
  - JT - Is there anything that the OpenWIS Association can help with?
  - IE - Communication and collaboration with members.  Common software componets (DAYCLI messages and
    Compute normals data).  CLAs, Understands what the next steps will be re data standards and models.
  - JT - there is a good link with Met Ocean. OGC have long term experience in developing data models, so
    there is expertise that could help in understanding practical steps.
  - SO - Yes, there is a real good opportunity to bring this into OGC for awareness and OGC is very active
    with a number of working groups where further expertise could be drawn upon. The next OGC TC during wc 14 June where a presentation would help
  - IE - That’s great.  Thank you.
  - JT - Are you aware of the CICD environment that OpenWIS has set up?
  - IE - Could be. Would be useful when testing.  Need help on libraries.
  - JT - No commitment to use our pipeline but it would be good for us to aware of what each other is doing.
  - IE - Yes agreed.
  - SO - I will be the best contact point. I think sharing information on metadata will be a good area to
    share ideas.
  - IE - Happy to discuss further.


	*6.5 WIS 2 presentation (Jeremy Tandy) and discuss potential roles the TC can play*

  - JT gave an overview and re-cap on WIS2.0:
  - Will share presentation, high level info:
	  - WIS2.) will prioritise public telephone networks
	  - Adopts web technologies
	  - Used web services for publishing data
	  - Adds open standard message protocols.  Implementation plan has 6 activiies:
	  - Project - demos to inform and validate.  Circa 10 projects that each pick out one or more aspects to
      test and validate.
	  - Normative works - INFCOM and people inolved in operating GISCs to update operating manuals and
      identify best practises.
	  - Monitoring – Set up tools and incident management mechanims to enable a smooth and effective
      transition from WIS 1.0 to WIS 2.0.
	  - Transition -  How migration from WIS to WIS 2.0 is working.  Particularly, as GISCs will need to do
      work to migrate existing catalogues.  
	  - Comms – Activity to engage and get feedback on challenges, perceived risks.
	  - Timeline: 2019 Endorsed by CG.  2020 – delays due to COVID.  2021 – experimental implementation, 2023 - Technical regulation approval.  2024 - ?? 2026 – stop updates to the current WIS catalogue. 2030 -  
      Hoping that migration to new message protocols are complete.  The key is to be aware of the lifecycle of Messaging Switching systems in organizations and the needs of small and island states.
	  - 2021 - KPIS, experimental real time data exchange in WIS2 draft tech specs.

    - JT - WIS 2.0 seeks to leverage industry standard protocol. So, in the case of messaging, this        
      could lead to no need for maintaining routing tables, for example, i.e. a real possibility of
      reducing complexity in the OpenWIS software.
    - JT - Questions?

  - SO - I have some updates and questions.  We are also looking at JSON LD and exploring the use
    of Ontologies in the Met Ocean communities.

  - SO - What do you see as the expectation re supporting WIS 1.0, given the time-line for  WIS2.0.
   - JT - Initial operating capability is aimed for 2024 for GISCs.  In 2026, the existing     
    catalogues  would be deprecated.  So, for OpenWIS, these are the time-scales that we should be looking at.So, as we discussed in Helsinki, OpenWIS will be in maintenance for a long period.
  - SO - Thank you. Time-scales change and we evaluate risks each year
  - WQ - Re metadata.  I understand the complexities around the current ISO standard.  So, what is the plan
    going forward, in connection with the new messaging format? What  architecture is being thought of?
  - JT - Relying heavily on Tom Claradis’s work in OGC and WMO.

**7.  Creation of overall work plan for 2021**

  - Creation of overall work plan for 2021.
  -	What does this consist of?
  - What monies are we seeking for 2021?

  - SO - Focus is on middleware Aim is to start development in July.  Aim is to test v3.15 by this         
    time.  The fall back is to use v3.14.  There would be a difference in the budget required.

  - SO - There is also the monthly cost for Github (depending on option to be chosen).

  - SO - No other items for the budget to be recommended to the SC.

	*How to ensure quality of our work?*

  - SO - A repeatable process and release management, adhere to the CICD environment (evidenced via report from this environment). Any more thoughts on ensuring quality?

  - All - No

Meeting ended 1600 UK time.
