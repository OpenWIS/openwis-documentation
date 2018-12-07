---
layout: page
title: OpenWIS Technical Committee 2018 September
---

#### 7th September 2018 - via WebEx teleconference

**Attendance and proxies**
The attendees and proxies for this meeting via tele-conference were:
- Benjamin Saclier (BS), Météo-France, France (MF) - Vice-chair
- Dominic Woollatt (DW), UK Meteorological Office (UKMO)
- Weiqing Qu (WQ), Bureau of Meteorology (BoM)
- Steve Olson (SO) representing National Weather Service (NWS) (Chair)
- David Podeur (DP), Météo France (MF)
- Kuldeep Srivastava (KS) India Meteorological Department (IMD)
- Jude Anthonisz (JA), UK Meteorological Office (UKMO)

Apologies:
- Stephan Siemen (SS), European Centre for Medium-Range Weather Forecasts (ECMWF)

Not present:
- Sungsoo Do (SD), Korea Meteorological Administration (KMA)
- Mikko Visa (MV), Finnish Meteorological


- SO welcomed IMD (Kuldeep)

**2.	**Approve previous TC meeting minutes****
- Minutes of previous minutes approved.

**3. Review of Annual TC meeting actions**

  1. [Ensure that all outstanding CLAs are completed](https://github.com/OpenWIS/openwis-documentation/issues/456)  
- a.	BOM Status: BoM will be re-submit
- b.	Exeter Status: Completed.  MO to re-submit as Paul Rogers left organisation.
- c.	MF Status: Submitted in September 2018
- d.	Korean Status: Completed
- e.	NWS Status: to be submitted and will update and the next TC meeting
- f.	FMI Status: SO to chase FMI
- g.	ECMWF Status: SO to chase
- h.	India Status: SO to chase

2.	[Check CLA  Process with Paul Rogers](#457).  
    - Agreed to close the action.

3.	[Check secure dropbox service options](https://github.com/OpenWIS/openwis-documentation/issues/465)
- Agreed  to leave open until decision on GDPR is known to inform wheher DropBox is required

4.	[Alter code of conduct rules on website](https://github.com/OpenWIS/openwis-documentation/issues/466)
  - This work is complete!

**5.	The following actions were reviewed and updated:**
- [Update Technical Rules to clarify roles](https://github.com/OpenWIS/openwis-documentation/issues/172)
  It was confirmed that is In progress and agreed that list is comprehensive so that the list is adopted.

- [Add software quality statement to Technical Rules](https://github.com/OpenWIS/openwis-documentation/issues/176)
    - BS - Need to ensure that the use of quality is flexible according to the project
    - SO - BS to update the statement to reflect flexibility of use
    - WQ - should we specific on which integration platform or should this be flexible
    - BS - I agree it should be flexible
    - SO - can we amend the text to reflect flexible and use Cloudbees and Jenkins as an example?
    - WQ - If the aim is consider software quality then we should be more general
     - SO - agreed

     **ACTION – SO to update statement on Technical rules and align web site page information on technical rules, code of conduct and development process.**


- [Re-align web site pages on technical rules and development process](https://github.com/OpenWIS/openwis-documentation/issues/163)
  - SO – asked for comments on the draft process
  - All – no comments
  - SO – A general question on what information should information should on the Wikki vs the website?
  - DW – static documents should on the website and more fluid on Wkki, i.e. with a link from the web    site to the Wikki.
  - WQ – agree with DW
  - SO – Any comments
  - All – none

  **ACTION All to comment on the word document to enable Steve to update document for approval at    the next TC meeting.**

- [Technical rules on how disputes on breach of technical rules are resolved should be    added](https://github.com/OpenWIS/openwis-documentation/issues/450)
  - This is closed!

- [Obtain latest position on investigation on testing and test metrics](https://github.com/OpenWIS/openwis-documentation/issues/195)

  - SO - any comments on the proposal from ED.
  - DW- the current tests relate to WIS1.  The question is whether the test result publication is a validation of WIS1 compliance.
  - SO - This is intended to a measure of quality and how test automation.
  - JA  - Is this for all projects, rather than just WIS1.
  - SO -Yes.
  - DW - Yes this could be used beyond WIS1, a generic approach. Suggested that we look at other projects and feedback.
  - WQ - We have some automated testing in the CI process. But not clear how it fits with WIS1
  - DW - I don’t we should be specific to WIS1 as this is the only criteria we have now and the Association will consider other projects. A generic statement would be good.
  - SO - It would be good if its applies to WIS1 and can evolve.
  - DW - It would be good to keep this one and see what applies to WIS2 when more information on WIS2 is available.
  - WQ - Keep WIS1 is maintenance mode. So should not be concerned with test metrics and review if there is a major issue.  The next round of GIS audits are being worked on but no detail yet.
  - DW - can SO establish background from JT?
  - SO - Agreed that SO will get more information from JT. ACTION
  - SO – Can we discuss the effort required at a future PMC meeting?
  - ALL- agreed.

**[set up PMC agenda and meeting](https://github.com/OpenWIS/openwis-documentation/issues/516)**

- [Consider new goals for quality](https://github.com/OpenWIS/openwis-documentation/issues/451)
Agreed to discuss at next PMC

- [Appoint new project lead for OpenWIS core](https://github.com/OpenWIS/openwis-documentation/issues/452)

  - SO – BS and SO discussed potential candidates and skill sets.  The
          outcome is a need for a  broad understanding of WIS1 and ability to participate actively in PMCs.  Could not see someone obvious could fulfill this.  So concluded that this would be worked up collectively at each PMC and action taken by a number of individuals, appropriate.
   - WQ -  this would work but a co-ordination role is useful.
   - JA -  who is best to co-ordinate? SO and BS?
   - SO and BS agreed
   - SO - Agreed the use the model.


- **Develop an approach to technical standards.**
   See Action-TC-2018-1 create rules supplement on approach to technical standards
   - BS - presented the proposal
   - SO - suggested that people comment off-line and agree at the next TC.
   - BS - Good to let everyone have more opportunity to feedback to make the right decision.
   - WQ - This is dependent on specific needs of a project.  Its not the right time now,
   - DW - agree with WQ but happy to go with BS recommendation so that no-one is discouraged.
   - BS - this is a request from SC.
   - WQ - in that case I agree with DW.  
   - DW - Each organisation has it own standards as well.  This will the basis requirement.  
   - SO - Need to review but accept BS’ recommendation re Apache or review further before committing to any aspect.
   - WQ - agree with DW but can delay the final decision.  They key point is that there is no requirement.
   - BS - Is the objective of OWA to start new projects?
   - WQ - yes.  
   - BS - So if I am to promote OWA in MF, I need to understand the rules that would apply.  
   - JA - it depends on the needs of the project.
   - DW - Strict rules could restrict potential projects.
   - ALL - Agreed that further comment is needed before a final decision

- [The release management process should be accessible](https://github.com/OpenWIS/openwis-documentation/issues/454)
  - SO - presented the issue.  
  - DW - is the action whether to publish items from the Wikki on the web site?
  - SO - There are two points 1) process 2) Release Notes etc
  - DW - can we try the proposed process on an OpenWIS project?
  - SO - Who manages the CI process.
  - DW/JA- CI team using Jenkins.  There is a change to Jenkins which will be a separate issue.
  - DW - what is needed for this action is how we can make the current process accessible.
  - SO - Agreed.
  - WQ - OK
  - BS - OK

  **ACTION JA and SO to investigate what information is available and establish what DW has done in the past**

- [Develop a repeatable process for quality](https://github.com/OpenWIS/openwis-documentation/issues/455)
  SO presented the issue. Does everyone agree that there are the proposed items are OK?
  - JA - Yes, it is a good base-line.
  - SO - Run out of time.

  **ACTION - SO to create a demo for approval by TC and SC**

- [Set up of user forum](https://github.com/OpenWIS/openwis-documentation/issues/468)
  SO - Need understand who will be owner of the IP addresses and DNS for Discourse, to enable the Discourse service to be set up?
  DW - It may have been MFI
  BS - Quite possibly.

**ACTION SO to contact RGb**

- [Deploy the WIS2 PoC on AWS Servers in UKMO](https://github.com/OpenWIS/openwis-documentation/issues/448)
   Agreed that JA should establish whether there are any costs

- [Governance of OpenWIS 3x](https://github.com/OpenWIS/openwis-documentation/projects/8?add_cards_query=is%3Aopen)
All agreed that this will be discussed at the next PMC meeting

**6. Open Discussion**
  - What to do with Bug issues still open, and especially for:
    (https://github.com/OpenWIS/openwis/issues/288)
    (https://github.com/OpenWIS/openwis/issues/293)
    (https://github.com/OpenWIS/openwis/issues/294)
    (https://github.com/OpenWIS/openwis/issues/262)

  Meeting ran out of time.
    Agreed that this should be on the next PMC agenda

 - Proposal for the web site from BS
   - DW - agreed as it build on the agreed process, so can post on the web site.  
   - SO - can you add as an issue in Github?
   - BS - Yes. Also allow SC to comment.
   - ALL - agreed.

   **ACTION - BS to raise the issue on Github**
