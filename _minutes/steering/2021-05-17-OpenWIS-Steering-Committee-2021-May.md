---
layout: page
title: OpenWIS Steering Committee 2021 May
minuteOwner: steering
---

#### 17th May 2021 - MS Teams video-conference

---
**1. Welcome and introductions**

  - JT and RGr agreed for JT to chair the meeting.

**2. Attendance**

  - JT - All delegates confirmed. Could defer decisions if delegates are not available.  
  - JT Confirmed that 6 out of 8 delegates attending, therefore quorate.

*2.1 Current members that were present*

  - Rémy Giraud (RGr), Météo France [MF] - SC Chair
  -	Jeremy Tandy (JT), Met Office [UKMO] - SC Vice Chair
  -	Loïc Le Gallou (LG), Météo France International [MFI]
  -	Kari Sheets (KS), National Weather Service [NWS]
  -	Mikko Visa (MV), Finnish Meteorological Institute [FMI]
  - Weiqing Qu (WQ), Bureau of Meteorology (BoM)
  - Mr. Y K Reddy, India Meteorological Department (IMD) partially attended
  -	Sungsoo Do (SSDo), Korea Meteorological Administration [KMA]


*2.3 Other attendees*

  - Steve Olson (SO), National Weather Service [NWS]
  - Jude Anthonisz (JA), (OpenWIS Association Secretariat)
  - HEO, Boram (BH), Korea Meteorological Administration [KMA]
  - Baudouin Raoult (BR) (ECMWF)

**3. Approval of the agenda**

  - All - No changes or addition to the agenda.

**4. Approval of previous minutes**

  -  All - No changes. Therefore approved.

**5. Election of chairperson ("TC-Chair") and vice-chairperson ("TC-Vice-Chair") of the Technical Committee**

 -  JT - SO full term. Benjamin Saclier left and David Podeur (DP) has taken over.  So, DP as Chair and SO
   as Vice Chair.
 - JT - So, one nomination for Chair and Vice Chair.  Any more nominations?
 - All - No
 - JT - Is everyone content with DP and SO as Chair and Vice Chair?
 - All - OK
 - JT - I would like to formally thank Météo France and RGr for putting forward DP as Chair
 - JT - Everyone happy to SO to be Vice Chair?
 - All - OK

RES-OWIS RESOLUTION - The SC agreed that the TC Chair is David Podeur and that the Vice Chair is Steve Olson

**6. Recommendations to the Board regarding admission of new Members and Partners (see Articles 6 & 9, and Rules 4 & 5)**

-  JT - Expecting DWD
- All - No others.
- JT - DWD have approached RGr and me with a view to working together to support WIS 2.0.  Wanting to work to
  help design WIS 2.0 compliant software.  So, RGr and I feel that DWD should be allowed to participate in Association discussion re WIS 2.0.

- RGr - DWD is heavily involved in WMO and WIS 2.0 activity, so a good time to talk again.  The DWD policy is
  that it cannot participate in using open source software.  We can also cover more as part of item 8.  Overall, a really good sign that DWD want to work with us.
- JT - I agree. What does everyone think?
- KS - I support.  They are TT-GISC leaders,  especially around monitoring. So well worth it, a great idea.
- SO - Can DWD join as an Associate member?
- JT - Not yet.  Let’s start as a contributing member.
- All - OK
- JT - So, agreed that DWD can participate in discussions.  But no need to recommend to the Board as a new
  member.
- RGr - Agreed. Can cover as part of no.8

  RES-OWIS RESOLUTION - The SC agreed that DWD would participate in WIS 2.0 discussion as an informal contributing partner OpenWIS 3.x**

**7. Project Reports and requests for Financial Support or changes to existing Charters**

*7.1	OpenWIS 3.x (https://github.com/OpenWIS/openwis-documentation/projects/8) **

- JT - Two active lines of work – 3.15 branch which the TC is aware of and middleware project that builds on
  version 3.15.  SO - Background - 3.15 uploaded by MFI to GitHub.  BoM, KMA, MF and NWS working on this branch. An omnibus issue created in GitHub to track.  A few issues need resolving.  It became apparent that 3.15 is aimed at a DCPC and as such GISC related aspects were missing.  Tickets raised with developer and some have been resolved.

- SO - Was looking to complete evaluations by end Feb 2021.  But needed to delay to end April as  result of
  installation issues.
- SO - Agreed at TC that we need to make a decision and that to pursue with 3.15 integration into the main
  branch by July 2021, assuming evaluations say that GISC features are available (i.e. acceptance by TC).
- SO - If satisfactory, then will look at implications for middleware.
- JT - Status to fix issues with 3.15 build issues?
- SO - These should be resolved this week. Our CICD environment based on Travis and Sonar which makes use of
  Java 8.  However, now Java 11 is required.  So, the work plan is to develop and upgrade the CICD components to work with Java 11 independently on 3.15 being on Java 8 without issues.
- JT – Questions?
- RGr - How optimistic are you about the July target/objective?
- SO – The TC as a whole is ready for the July date.  If there are still issues in July, the RFP will be
  altered to reflect what is outstanding.
- JT - The deadline is regarding 3.15, not the RFP?
- SO - Yes
- RGr - Using 3.14.1 as the base for the middleware is that the right approach as we may lose features of
  3.15, which may have to be re done?
- SO - I think we will be able to work these issues out by July 2021, so unlikely that 3.14.1 will to be used
  as the baseline.
- RGr- OK
- JT - Can I suggest that if we still have outstanding, I wonder whether we should delay the start of the
  middleware work until resolved?
- SO - Yes we can do that.
- JT - So RGr would you like a communication from the OpenWIS PMC to the SC about whether to delay or not?
- RGr - I would prefer doing middleware to be based on 3.15 rather than rushing. So, best to wait until
  issues are resolved. What would be expected from the SC, is it just the budget?
- JT – It’s about the complexity of having two branches, i.e. a need for a simple roadmap.
- RGr - So, yes a simple roadmap is favoured from SC perspective.
- LL - Why not get the middleware to be resolved via the RFP?
- RGr - I have no preference in who does the middleware.
- SO - a few factors.  New developers in the team, so time needed for learning. A question for RGr – any
  chance that more time can be gained from the developers of 3.15?
- RGr - I can ask within MF to see if I can help.  WQ - in TC we didn’t discuss having two branches.  Any
  work would start from 3.15 and if any issues then include in RFP, same as LL.  If we can resolve within the Association, then less cost of RFP.  Prefer not to delay.
- SO - the problem here is if we accept some of the issues of 3.15, then faced with not understanding the
  interdependencies and testing/validation in all potential implementation scenarios.
- JT – We all aspire to have 3.15 as the baseline and TC is confident that this will be possible by July.  
- RGr is speaking to MF to see if additional effort can be provided.  As SC, we would rather see the issues
  resolved before starting the RFP, which could include a delay up to September 2021.
- JT  - Is that fair summary?
- WQ - Work on RFP?
- JT - Yes
- WQ - This is dependent on the procurement partners.  How feasible?
- JT – let’s get to that in a moment.  Just to agree with the approach.
- RGr - Yes
- LL - We need to be confident that the issues will be resolved and accept that 3.15 is not perfect as we may
  be waiting  a long time.  If we say that its only say 2 days effort, we should accept 3.15.
- JT - we want the same thing.  My proposal is that we see if there are additional issues by end July, then
  the PMC need to provide a costed proposal as part of the RFP.  Being clear what the cost increase is from current version of the RFP
- SO - I am aware of a number of GISCs that planned upgrades from their existing baseline installations of
  OpenWIS software.  So, would be good to communicate the plans to these centres.
- JT - A great idea to have a comms plan.  Can  comms plan be added to the PMC/TC Work Plan?
- SO - Yes.

[ACTION - SO to create and implement a communication plan for all users /centres that have deployments of OpenWIS. The communication plan should reflect the updated roadmap of OpenWIS](https://github.com/OpenWIS/openwis-documentation/issues/626)

*Middleware RFP*
- SO - Recommendations from the TC to upgrade to Tomcat 10; Java 11 preferred if not v8; Wildfly v19;
  Postgres 13; OpenAM and OpenDJ replaced by Plug in - Keycloak; Merge 3.15 into master and incorporated in the CICD environment.  RGr - In principle I would like to avoid paying for an upgrade unless absolutely necessary.
- SO - that’s the stance taken by the TC.
- JT and RGr - Great
- MK - Java OpenJDK or Oracle?
- SO – OpenJDK  	JT - The other aspect is incorporating procurement and budget?
- SO - My understanding is that the contract is on track to start in July.
- LL - Yes.  Everything is on track.  Now awaiting content of RFP and then agree how payments will be made.
- MV - Agreed.
- JT - Thank you all three of you for working through the technical and contractual matters.
- SO - Thank you LL and MV.  The budget value agreed in 2020 is deferred to 2021.  I don’t expect much
  additional costs.  Can’t speak for MF or developers of 3.15.  May be maximum of in the region of 75k Euros. JT - recommend that we take a break and resume in 10 minutes and for RGr to chair.
- RGr -  OK.
- RGr - A summary.  By July a conclusion either all OK with 3.15 or a recommendation for an alternative to
  SC. So, this means a potential change to the RFP.  The RFP goes to the procurement partner and the procurement partner provides a response.  The response will inform the budget needed to be known by the SC.  
- SO - Yes.
- RGr - So the SC will know whether the 50k budget previously agreed needs to be increased.  If an increase,  
  a report is needed to the SC and Board.  By middle September we need a communication from the TC to SC and Board.
- All - OK.

[ACTION –The TC to inform the SC by September 2021 of the scope and cost for the middleware RFP.  If there is  a change in scope and cost to compared to the current RFP and agreed budget, this should be made clear](https://github.com/OpenWIS/openwis-documentation/issues/628)

*7.2	[OpenCDMS](https://github.com/OpenWIS/openwis-documentation/projects/14)*

- JT- We have previously talked about AWS.  A driver for this is OpenCDMS.  OpenCDMS is about building a
  reference implementation that its cloud deployable.  At the TC Ian mentioned that he would want to be deployable on any cloud platform.  So, no dependency on AWS.  AWS are happy to contribute via in-kind contributions.  No need to have AWS to be an Associate member.  
- JT - Any questions?
- RGr - No issues.  Still cautious but based on what you say that there is no need for this at present.
- JT - The project will develop a more structured relationship via an MOU and would help if you can join.
- RGr - No problem at all.
- JT continued with an overview of OpenCDMS (per slide deck).
- JT - Aspects that OpenCDMS would like to engage and share with OpenWIS members (per slide on             
  ‘plans for next 12 months’ slide)
- RGr - From OpenWIS members, which one are contributing to the software?
- JT - From UK perspective, Ian Edwards via VCP.
- RGr - Any others?
- JT - Don’t think so, a small number of developers and data modellers – c 20 people.
-	JT - We have the right level of autonomy.
- RGr - No other questions


**8.	Review new proposals for projects that are compatible with the purpose and objectives of the OpenWIS Association and in the interest of Members and Partners  ***

- RGr - This relates to the discussion on item 6.  JT and I are heavily involved with WMO re WIS 2.0.  In MF,
  we concluded that we will still need a new MSS system when WIS 2.0 is implemented.  RGr - So is this the right time to create a pre PMC environment for starting discussions on what an MSS would be as part of and compliant with WIS 2.0.  It would, therefore, be good to have DWD on board for this. What do people think?

- SO - This makes sense to me.  JT - A really good call, as the change on how real time data is handled is
  key.  Will be good to see working code as soon as possible.  There is also the link with metadata.  What did you have the outcome of this project in mind- finished software, prototype, something else?

- RGr - Looking at what is happening in OpenCDMS, potentially a reference implementation.  Perhaps in 3-4
  years’ time a finished product that organisations could adopt.  This is the right time and message to say that the Association is starting on open source software.  The specific target could be discussed as part of the pre-PMC.

- JT - A couple of questions.  Donor code, a lot out there for message brokers.  How does it related to the
  work that Peter Silva has spun up already?

- RGr - Brokers will be part of the solution.  However, for using these brokers in an operational environment
  there will other components needed.  The idea is to identify components and glue them together.

- JT - A great strategy.  There is a difference of approach for example between UKMO – which buys a service
  rather than develop in-house.  Will help get resources from UKMO is both approaches are considered.  	

- RGr - These kinds of discussions could take place.
- JT - I am keen for UKMO to be involved in principle and will pursue within UKMO.
- WQ - The need is to develop the glue.  So, the WIS 2.0 specification will have a task to define this.  Is
  that a fair statement/plan?
- RGr - What we need the collection of software for a solution and don’t know what is missing.  I feel that
  it’s the right time for the Association to take steps in defining this.
- JT - the glue might be something as simple defining containers (i.e. configuration requirements/files).  It
  may not involve writing lots of code.
- RGr - Yes.  MetPX is currently a candidate for example.
- JT - Agreed. MF,UKMO, and FMI interested in principle.  Also, DWD.
- WQ - BoM as well.  Still need to what is needed, a specification?
- RGr - This is for the pre-PMC to define.
- SO - NWS also interested, especially synergies with pub-sub.
- JT - Is BoM deploying aspects already?
- WQ - Yes, OpenStack
- SSDO - KMA interested in pub-sub, essential. So, interested.
- JT - We also have EUMETNET.	Some of the partner Met Services still not aware that GTS will be changed.
- RGr - So most Association organisations happy to work on the pre-PMC. DP happy to lead on this work. So,
  happy for SC to task work for the next 6 months.  Is that OK?
- JT - Yes.
- WQ - relationship between pre-PMC and WMO ET work?
- RGr - At the moment, within WIS 2.0, there is a list of demonstrator projects.  In the Association is kind
  of another demonstration project.
- WQ - Understood.
- JT - WMO defines the standards, we and others will figure out how to make it work.  All - happy to DP to
  set up the pre PMC and agree the Charter.  All to dominate representatives.

  [ACTION - DP write short Charter as soon as possible and for the pre PMC feedback by December 2021 (work between June and November 2021)](https://github.com/OpenWIS/openwis-documentation/issues/627)

- SO - Other pre WIS 2.0 studies.  Metadata – working with Canada – authoritative template/API for
  consideration for WIS 2.0.  The aim is to find the minimum amount of data that aids discovery.  
- SO - From a web services point of view - the working on the EDR API is again prime. So, happy to answer
  questions or happy to start a background project.
- JT - is everyone aware of the EDR ?  I can summarise - Environmental Data Retrieval (EDR)?  Driven through
  OGC with representation from UKMO.  Uses web-based approaches to simplify access data using simple metadata in 4-dimensional space.
- JT - Are there strands of activity on metadata that anyone wants to participate in?
- RGr - I believe that compared with WIS 2.0 this advanced there is relatively good awareness.  
- JT - I think more needs to be done before stability.
- RGr - Agreed.
- SO - Agreed.
- JT - So, let’s wait for Tom’s work to progress further before setting up projects.
- RGr - Is there anything else?
- JT - As mentioned I am working on the WIS 2.0 architecture.  As this develops, there will need to be
  projects.
- RGr - So this concludes this agenda item.  

Meeting resumed on 19 May:  


**9.	Recommendations to the Board regarding new or amended Projects (incl. creation of any ad-hoc committees or subsidiary bodies (including PMCs for new Projects)**

- RGr - No recommendations to Board (pre PMC to stay at SC level)
- JT - agreed
- All - agreed 

**10.	Report and recommendations from Technical Committee**

- SO - I can give a summary of the work plan- We have already talked about 3.15, the middleware situation;
  potential for new costs; on-going maintenance (GitHub bot and other vulnerabilities and Sonar); Sunset of projects; Github subscriptions options;  Recommendations - per earlier items. Nothing for the Board.

- RGr - Any questions?

- JT - I like to update on the GitHub plan.  UKMO currently pay for bronze service, which is now deprecated.  
  New plans are available from GitHub.  The initial assessment is that the free plan is OK.  However, the big change is around GitHub automation, which has similar features to our CICD.  So, there may be a change needed.  So we took an action to look and what OpenCDMS and other known open-source projects are doing – DP leading to have a recommendation by 3 months’ time.

- RGr - When are we being kicked out of the bronze plan?

- JT - Unsure but the plan is currently continuing.  We are not using GitHub automation.  A point to note is
  that Github is moving to per-user pricing.  If a small cost UKMO happy to pay but may need to change if expensive.

- BR - Can mix public and private repos.  Cannot do CICD on public repos.  For compiling can take up to an
  hour for C++ or Python. So not sure about Java.  Simple and elegant solution but need to be using most recent software, otherwise need to use Docker.

- JT- most time taken up by running test scripts.  Given that we spent money on CICD recently, I am not
  comfortable moving off, but keen for looking at optimisation.

- SO - Agreed.
- RGr - No additional requirement of funding?
- SO - Yes.
- RGr - Any more questions?  JT - a function of SC is to make projects accountable.  We’ve seen milestones
  for OpenCDMS.  It would be useful, once the technical rules, a short report on the status of compliance with the technical rules.  Is there is any value in projects reporting to the SC on compliance on technical rules?
- RGr - I am confident that OpenWIS is being managed well, so not concerned with reporting.  OpenCDMS is high
  profile and the SC doesn’t want to hold things up but should get some form of assurance.  

- JT - So the SC rep on the project should provide assurance to the SC?

- RGr - OK

RES-OWIS RESOLUTION - The SC agreed that rather than a formal assessment against compliance by the SC, it’s the SC rep on each Project Management Committee should drive assurance on compliance on technical rules.

-  JT - Is there anything else to advise the SC?
- SO - the only things is about the WIS2 and other OpenWIS 3.x projects will be stopped or managed informally.
- RGr - Anything else?
- LL - will good work on planning the middleware upgrade and share the main milestones, how to take to do the
  work and validate/test?
- SO - Ticket 590 has the latest milestones and I will update after the annual meeting.  If there is a need
  for additional, happy to answer queries.
- LL - OK
- RGr - Any more comments or questions?
- All - No
- RGr - Thank you Steve for all the work on the TC.


**21.	OpenWIS Association logistics**

*12.1	Programme management / secretariat function*

- JA - Can commit until end October 2021.
- JT - we have new process for managing demand for all external requirements.  We will have to go through
  this process, which means there will be completion.  We are also happy to pursue sourcing UKMO via this process. So, is there other options?
- JT - Take over by 3 months’ time or later?
- RGr - Not available in MF. Other organisations?
- SO  - Not at present.
- WQ  - No resource, can look at other groups
- LL - Have to think- may be
- SSDo - No extra resource
- MV - Most likely no.
- BR - No.
- JT - Two ‘may bes’. Simplest may be for UKMO to maintain continuity and go through demand management by end
  July 2021.  
- JA - OK
- JT - Can LL look in parallel to we have time.
- LL - OK
- RGr - Can the chair help
- JT – Yes, a letter with the request will be useful for UKMO and potentially LL and WQ.
- RGr - Can JA and JT a draft a proposal.

*ACTION - JA and JT to draft a proposal for the Association’s Secretariat function / role for RGr to agree.*

- RGr - Back up plan is to have a rota?
- JT - May not work as Jude does a lot of work behind the scenes.

*12.2	Treasurer*
- ND happy to continue.
- RGr – anyone else want to take over?
- All - No

*12.3 	[Information Management [from GDPR](https://github.com/OpenWIS/openwis-documentation/issues/459)*

- JT - No progress, on the basis that we haven’t expanded the pool of people.
- JA - We’ve not had any requests for information or complaints.
- RGr - OK.  No issues.  But let’s talk about the situation regarding CLAs and NWS.
- JT - Very little has happened as legal teams is NWS and UKMO are busy.  However, a meeting is scheduled for
  late June 2021 to progress.
- RGr - My concern is around the OpenCDMS project as we may get caught between which CLA is being used.  The
  aim is to avoid having separate CLAs for each project.
- JT - Agreed, the approach is best to have overall CLA if getting a CLA is not time consuming.  If not,
  then we need to use separate CLAs.
- RGr - Will make sense to have a decision at the September 2021 meeting to make a decision.
- JT - Agreed.
- All - Agreed.
- RGr - We need to inform MR and Derek.

*ACTION - JT to inform Michael Robbins and Derek Hanson that the Association’s SC will need to decide in September 2021 on whether to adopt a single / overall CLA or multiple CLAs that are project specific.*  

[ACTION – JA to set up a meeting with Michael Robbins, Derek Hanson, Fred Branski and Jeremy Tandy to enable progress of CLA definition and ensure that the CLA decision is on the agenda for the SC in September 2021](https://github.com/OpenWIS/openwis-documentation/issues/494#issuecomment-844909497)

**1.3  Shaping the OpenWIS Association** 

*13.1.    Status establishing a procurement partner](https://github.com/OpenWIS/openwis-documentation/issues/590)*

-  RGr - Any more to add? All issues resolved?
- LL  - agreement reached on using French or Swiss law.  Probably good to have a contract between FMI and the
  Association, so to initialise can propose a document.
- MV  - No addition, a good summary.  Should be not a big issue re contract between FMI and Association.
- RGr - When work was managed by UKMO, we didn’t have a contract. So, where is the request coming from?
- MV - not a request from FMI, can do without.
- LL - FMI will need to invoice the Association to detail the operation.  So, the issue is that there may
  invoices to recover from Association without a contract.
- RGr - Not a problem, as Treasurer recommends.
- JT - Agreed that we should have a contract
- RGr - Can LL draft a contract, for FMI to agree and RGr to sign/endorse.

[ACTION – LL to draft a contract for FMI to agree and RGr to sign / endorse]( https://github.com/OpenWIS/openwis-documentation/issues/590#issuecomment-844893022)

- LL - Re payments, the contracts needs to align so that payments between all parties in the same year, i.e.
  by December each year.
- JT - So given this and a 30-day period, can invoices be received by 30 November 2021? A schedule of
  payments ?
- RGr - Discuss in September SC about payments.
- JT - Can we have a process to ensure that the quality of code, its packaging and documentation is of
  adequate quality?  Is this something that SO and DP approving for goods receipt notice?
- SO - Yes agreed.
- RGr - How we want the goods to be delivered should be described in the RFP.
- LL - Yes. as well as conditions of acceptance. I.e. after testing/validation.
- JT – SO, are you comfortable that the technical rules cover this adequately for acceptance criteria?
- SO - I’ll review technical rule

[ACTION - SO to review Technical Rules to ensure Acceptance Criteria is adequate for inclusion within the RFP](https://github.com/OpenWIS/openwis-documentation/issues/590#issuecomment-844893022)

- WQ  - Do we have to pay e-works as the middleman?
- LL  - Fees are quite low
- MV - There will be a fee
- WQ - It will be part of the budget?
- MV - Yes
- JT - For the acceptance criteria, the ability to build and deploy from code to functioning software from
  the CICD environment would be a good criterion.
- SO - Yes
- LL - it would be good to define a payment schedule into the RFP.
- RGr - Not sure I see the relationship between work being asked and payment?
- LL - Lawyers see a risk. So a higher initial payment may be requested.
- JA - So both a higher initial payment and a schedule?
- LL - Yes
- JT - No problem for me.
- RGr - Would it be useful if a Board member is part of the discussions?
- LL - Make sense to add into the contracts
- RGr - OK
- JT - Happy either way SC or Board member
- RGr – So can something to reflect this be included in the draft contract?

[ACTION – LL to ensure that the draft contract includes the need for an Association SC or Board member to be part of decisions when making payments and contract development](https://github.com/OpenWIS/openwis-documentation/issues/590#issuecomment-844893022)

*13.2    Status of establishing updated byelaws of the Association (also see item 17, below)  **

- RGr - I wrote to Board members on 25 Feb 2021 with the power of attorney to allows notaries to sign on
  behalf.  Awaiting responses from KMA.  Received responses from others.  LL has the invoice been paid to the notaries 1662.80 Euros?  Will check as part of Accounts.
- RGr - I expect that the new by-laws are published in the Belgian gazette by July 2021.

*13.3    How/where can/should OpenWIS Association add value?  **

- RGr - This is the open question to make sure we are not wasting time.
- JT - I’ll share a paper to INFCOM, I gave in October on the need for open-source software for WIS 2.0.  It
  shows a huge range in expected expenditure on GISCs by WMO members.  The conclusion is that the availability of open-source software is beneficial.  

- JT - So in term of the Association adding value, there is a clear need for open-source software for
  WIS2.0.  There is no evidence that other WMO members coming together to develop software.

- SO - Cloud based development appetite?

- JT - This aspect was not discussed.  However, it was evident that some members with higher operating costs
  correlated with lower implementation costs – meaning likely cloud-based implementation.  SO - Has WMO ever broached the subject of Weather Watch data being part of the big data initiative?

- JT - Is this the NWS big data initiative with the four cloud providers?
- SO - I wasn’t aware whether there is an initiative like this in Europe?
- JT - I am not aware of a co-ordinated approach globally.
- RGr - I agree that WIS 2.0 we are defining functional requirements and may not define the implementation
  level. An idea in WIS2.0 is avoid asking the GISC to do the same thing multiple times.  We as an Association we can do the technical things for a number of GISCs.

- RGr - Re public-private partnerships, I am wary of fundamentally different purposes.  It’s a difficult
  position as strategically and politically it may be attractive and there is a different approach in regions, so cannot assume that one model is applicable to all.   A difficult position.

- RGr - The approach to WIS 2.0 is accommodate multiple models.
- JT - Happy to accommodate members as part of the WMO ET team.

*13.4      Review the continuing need for the OpenWIS Association*

- Covered in 13.3 and 13.2

*13.5.    Identification of opportunities for engagement with WMO*
- JT - We have opportunities to engage with WMO and community with the message broker pre-PMC as well.  It is
  also possible to offer side-session or seminar at future Congress re getting onboard WIS2.0, however, we must have something meaningful to say.

- SO  - If such a session were to occur, what would the topics be?

- JT- I am imagining that at Congress will be non-technical audiences, so communicating what WIS2.0 means in
  practise.

- RGr - We have received a request so far from WMO so far, so not sure?  We can ask WMO Secretariat.

- WQ - What can be achieved virtually?
- JT - A presentation
- WQ - We can only raise awareness.
- SO - Is CBS TECO still an opportunity?
- JT - CBS doesn’t exist.  The INFCOM has replaced and this.
- RGr - The next INFCOM is in February 2022 which may result something like CBS TECO.

*ACTION -  RGr or JT to end Enrico Fucile, Anthony Rea on whether it’s possible for  side session at Congress and whether an equivalent of CBS TECO is available.*

**14.	[Review of Strategic Goals and Metrics (3-year horizon) [metrics]] (https://github.com/OpenWIS/openwis-documentation/issues/589 ***

- JT - Two things on our books – Make available open-source software for WIS 2.0 and maintain OpenWIS
  software for WIS 1.0 that is secure 

**15. 	[Risk review and development of mitigation plans](https://github.com/OpenWIS/openwis-documentation/projects/4)**

- Not discussed.

**16.	Finances of the OpenWIS Association [Treasurer or delegate for Treasurer]**

*16.1	FY2020 expenditure* 
- LL – Total in-kind contributions 199k
- LL – total income is 203.9-k
- LL – total expenditure 232k
- LL – net position is a deficit of 28k
- LL – last year we benefitted from IMD’s contribution
- LL- Balance sheet
- LL - Bank account 511k euros
- LL - Accruals 3.8k BAT and Met Office.
- LL - Total 507k available to Association
- JT - Why do we have two accounts?
- LL - Not sure?
- RGr - Most of the funds should be in the savings account.  WQ - Can withdraw at any time from savings?
- LL - Yes.

[ACTION - LL to ask ND to move money into savings account following advice from Société Générale](https://github.com/OpenWIS/openwis-documentation/issues/611#issuecomment-844876239)

- LL - Benefits in Kind trend is shown in the slide.  Note that all partners are not declaring benefit in    
  kind work done.
- RGr - MF is not a zero but no problem.
- JT - I recognise and thank MF for the work done in 2020.
- JT - Extend thanks to NWS, MFI for the contributions. Also note that FMI is not a zero.
- SO - I want to recognise the work done by BS and YG for the work done via MF.

*Budget 2020 review*
- LL – The highlights are:
	•	ECMWF fees
	•	Domain name paid by MFI directly
	•	Secretariat little more than expected
	•	Dropbox a little less than expected.
	•	CICD final costs
	•	Total – overall 5k less than expected due to project costs being in 2021. 
	•	Review of need for additional finance  Agreed that there is no need for additional finance.  Review at SC in September 2021 

*Budget for 2021 (https://github.com/OpenWIS/openwis-documentation/issues/611) **

 - LL – The usual repeating items and we need to consider whether all of the 50k Euros for project will be
  spent in 2021.  The total budget is 44640 euros.  Note that this includes accrual for ECMWF fees, legal costs and Secretariat fees.
 - JT - By law work coming up. Is this reflected
- RGr - Invoice for 1.7k
- JT - Any more costs
- RGr - No 

*ACTION - LL to check with ND re adding the 1.7k invoice relating to by laws legal work, if not already accounted for.  RGr -  Is the SC OK with the budget.*

- All  - Agreed 

RES-OWIS RESOLUTION - The SC agreed the that Annual Accounts for 2020 as presented for recommendation to the Board

RES-OWIS RESOLUTION - The SC agreed that 2021 budget values for recommendation to the Board

**17. Recommendations to the Board to make and adopt, alter, supplement, or repeal the Internal Rules**

- RGr - No other recommendations other than budget
- All - agreed.

**18.	Outstanding actions (not already covered in the agenda)**

*18.1	[Definition of contributing partner](https://github.com/OpenWIS/openwis-documentation/issues/619)*

*18.2	[Retention policy for non-personal data](https://github.com/OpenWIS/openwis-documentation/issues/552)*

- All - Agreed that these items should be discussed at the September SC

**19.	Any other business**
- JT Face to face meetings to be discussed at September’s SC.

**20.	Summary of recommendations to the Board**
- Please see item 17, above.

**21.	Next meeting**
- Monday 27 September 2021 – virtual meeting 1100 to 1400 UTC.

**22.	Closure of the meeting**
- 15:04 UTC
