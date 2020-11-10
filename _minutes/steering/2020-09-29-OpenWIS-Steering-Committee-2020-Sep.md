---
layout: page
title: OpenWIS Steering Committee 2020 September
minuteOwner: steering
---

#### 29th September 2020 - BlueJeans video-conference

---
**1. Welcome and introductions**

  - RGr – introduced the meeting.

**2. Attendance**

*2.1 Current members that were present*

  - Rémy Giraud (RGr), Météo France [MF] - SC Chair
  -	Jeremy Tandy (JT), Met Office [UKMO] - SC Vice Chair
  -	Loïc Le Gallou (LG), Météo France International [MFI]
  -	Sungsoo Do (SSDo), Korea Meteorological Administration [KMA]
  -	Kari Sheets (KS), National Weather Service [NWS]
  -	Mikko Visa (MV), Finnish Meteorological Institute [FMI]
  - IMD representative (could not be identified)

*2.2 Members not present*

  - Weiqing Qu (WQ), Bureau of Meteorology (BoM)

*2.3 Other attendees*

  - Steve Olson (SO), National Weather Service [NWS]
  - Stephan Siemen (SS), European Centre for Medium-Range Weather Forecasts [ECMWF]  
  - Jude Anthonisz (JA), Met Office (OpenWIS Association Secretariat)

**3. Approval of the agenda**

  - JA - Could we cover CLA Amendment progress with NWS to AOB?
	- JT - I can cover this item
	- RGr - Yes.  Any other items?
	- ALL - No.

**4. Approval of previous minutes**

  -  All - No changes. Therefore approved.

**5. OpenCDMS PMC**
  - JT introduced OpenCDMS and shared an MS PowerPoint presentation.
  - JT - The key issue that the OpenCDMS project is seeking to address that there is a wide user base that are using legacy software with  no resilience for collection of climate and hydrological data.  Therefore, the two aims are to create an open source reference implementation and develop a migration path from existing legal systems to the new reference implementation.

  - JT - the PMC members are:
	•	WMO Secretariat and Project Advisor Team representative - Peer Hechler (deputy Nirina Ravalitera)
	•	OpenWIS Association representative and member of WMO INFCOM (SC-IMT) -Jeremy Tandy
	•	Member of WMO SERCOM  (ET-DRC) - Denis Stuber
	•	Project Technical Team representative - Ian Edwards
	•	CDMS user representative - Steve Palmer
	•	Hydrology User representative – Vasco Stojov
	•	Future Project Stakeholder Group representative – Vacant

  - JT - There is also larger advisory team of approximately 20 people.

  - JT - The items of work are governance and creating a specification for a web-based API and data model.  The underpinning data model will be specified to enable migration from legacy systems.  There is no work on a GUI, as the approach in the interim is to use the API and data model to interface with legacy systems to maintain familiarity for users.

  - JT - There is a great opportunity for a public-private sector partnership as Amazon Web Services (AWS) are very interested about engaging with this project as a part of is massive (i.e. USD10B) contribution toward combating climate change (https://www.bbc.co.uk/news/business-51539321).  In this regard, AWS  is evaluating whether the best way for them to engage is to join the OpenWIS Association.  The OpenCDMS project team all appear keen to engage with AWS and want to ensure the partnership is constructed in the right way.

  - JT - The request from the OpenCDMS project of the Association are:
	•	Solicit OpenWIS members and partners to help us in this task. Notably NOAA, Korea, Finland and MFI. There are several ways to contribute, i.e.  
	•	the possibility to access the document describing the schema of your NMHS or company database (this has been done by the UK Met Office and France);
	•	Make available a file for the creation of an empty database; or
	•	simply by answering some of our questions. 
  - RGr -The challenge of OpenCDMS is that there is a large install base.  The project is making allowance for this, hence the approach to using an API to deal with the diversity.
  - RGr - any questions or comments?
  - LL - what is the status of the project ? Has any prototyping been going on?
  - JT - Members of the project also working on their local deployments to test and validate designs.
  - JT - There is potential for the data model it to be a central resource that be hosted on the cloud.
  - JT - If you are happy, can Pierre H get in touch with members?
  - MV - OK
  - LL - OK
  - SD - OK
  - KS and SO – Yes

RES-OWIS – SC Agreed the membership of the OpenCDMS PMC

  - RGr - We need to discuss:

	*Approval of OpenWIS Association representative on the CDMS project*
  - RGr  - Are you happy to continue JT? JT -  I am happy to continue
  - RGr - please continue and thank for the work done so far.
  - ALL - OK

RES-OWIS – SC agreed that JT can continue as the representative of the OpenCDMS Project from the OpenWIS Association.

*Proposed changes to CLA for OpenCDMS*
  - JT - The aim is to share documentation via an open source licence
  - RGr - OK if Michael Robbins (MR) is happy with the text
  - JT - No changes to OpenWIS software. So, no need to change CLA.  However, there is a wider point on CLA which may drive a change that needs all to sign an updated CLA.  The SC just needs to decide whether the proposal for OpenCDMS is acceptable.
  - RGr - we need to find  the legal position. i.e. as everyone has signed current version whether there is no need to sign new one?
  - JT - I would say that there is no need to sign unless sharing documentation on OpenCDMS.
  - RGr - If discussions with NWS takes a couple of months then we go for the latest (i.e. updated) version.
  - RGr - Can you check with Michael Robbins (MR) whether the existing CLA needs to be re-signed or not?

  *ACTION - JT to check whether the current CLA needs to be signed again considering the proposed change for OpenCDMS.*

  - RGr - Is SC happy to accept OpenCDMS’ proposals if there is no need for all to re-sign the CLA and then propose recommendation to the Board.
  - All - OK.

RES-OWIS - SC agreed that the CLA changes can be recommended to the Board subject to there being no need for re-signing by all who have already signed the current CLA

*[ACTION - JT to Update issue 601 and create a Pull Request for the changes to the CLA](https://github.com/OpenWIS/openwis-documentation/pull/604)*


*AWS*
  - RGr - I welcome participation and receiving funding.  The downside is the contribution is not big according to the existing Association by-laws.  So, by-laws will need to be flexible/new membership category in this regard, i.e. AWS as a contributing partner.
  - RGr - Do we want AWS to be a partner at all ?
  - JT - let’s review when we have seen the proposed change to by laws viz membership classes.
  - RGr - the question is whether we want this type of organisation in the Association ,i.e. public and private difference in goals.
  - LL - Overall no problem as doing this already in other aspects.
  - MV - We are already participating like this. So, no problem
  - SS - No resistance to join. But need to clarity what position will AWS hold in Association now.  May be another way to join OpenWIS (i.e. via TC) ?
  - SS - can I ask when AWS contribution stops.  Are we sure its money or cloud credits?
  - JT - Yes both cloud credits and contribution in kind.  Accepting AWS doesn’t commit us to use AWS cloud.
  - SS - I would like to hear more about what they are interesting and their drivers.
  - KS - Very supportive of this type of agreement and in use in the USA.  Doesn’t exclude others  joining.
  - RGr - So in conclusion I would suggest that I am involved in discussions with AWS to further understand before deciding on whether to accept and how.
  - JT - very happy to have more people involved.
  - RGr - So the recommendation is for JT and me to have joint discussions with AWS.  
  - RGr - Is that OK?
  - All - OK

  RES-OWIS - SC Decision is to recommend to the Board that joint discussions (JT and RGr) take place going forward to enable decision regarding entering and partnership with the Association and how this will operate.*

**6. Association by-laws**
  - RGr - introduced the context, i.e. include a third type of partner to make it easy to accept contributions.  
  - RGr - Proposals and comments received have all been included in latest version available (0.8).  Work on this started in 2018, so I appreciate the comments from all partners:
  - JT - Happy
  - KS - Happy
  - MV - OK
  - SD - OK
  - LL - fine
  - SS - Look good to me
  - RGr - So shall I make a clean version for approval by the Board on 1 Oct 2020.

  RES-OWIS - SC Agreed that the updates to the by-laws can be recommended to the Board

  - JT - There may also be updates to Internal rules to accompany.
  - RGr - Yes if the Board approve the by-laws, the SC can be tasked with update of Internal Rules.
  - JT - OK
  - JA - Will advise and input be needed by MR?
  - RGr - I  propose that SC approve subject to no significant issues from MR
  - SD - Yes, it’s OK
  - MV - Yes, it’s OK
  - KS - Yes
  - LL - OK
  - IMD - No response
  - JT - Agreed. Really all we are doing is broadening scope not fundamental legal changes.

  RES-OWIS – Agreed that Internal Rules changes that follow on from changes to the by-laws could be made once the by-laws are approved by the Board with input from Michael Robbins.

  *[ACTION - JT to update Internal Rules once the by-laws are approved by the Board](https://github.com/OpenWIS/openwis-documentation/pull/604)*


**7.	Budget Review**
 - JA - I have requested an update to the budget from LL.
 - LL - Credit card from Société Générale is on its way may experience some delay in payment.
 - LL -  we decided for 2020 the overall budget is 39470 euros
 - LL – The Domain name costs will be paid by MFI in kind.
 - LL - All other items have been paid from the bank account.
 - LL - Main point is project costs.  The question is whether we keep the budget as is or will the work be done in 2021?
 - LL - Contingency - no need for this so far.
 - LL - Bank fees- no change
 - LL - So in summary, we have spent 9345 euros

 - JA - Any update from TC on Middleware when and the likely spend as this is greatest uncertainty of budget?
 - SO - largest aspect is Keycloak work.  This will be finalised by end of Oct 2020.  Second driver is when MFI code will be available to be assessed to inform work on middleware, i.e. evaluation will be by November 2020 and merging feature branch in December 2020, with completion of evaluation in January 2021. February 2021 to decide what work is needed via external party.  Alternatively, we wait until  December 2020 to evaluate, meaning ready  in April 2021 instead of February 2021

 - JA - So, no spend in current FY in either scenario

 - LL - So remove project items in 2020?

 - RGr - Yes.
 - RGr - one more item.  Fees for procurement advice (line 21).  In summary, procurement must be within Europe and additional costs after negotiation.  The legal advice for this is an additional 5.2k euros.  So, this amount to be paid, which is about 5k more than in budget.

 - RGr - ALL SC members agree with revised budget?

 - ALL - Yes.

RES-OWIS - SC agreed to recommend to the Board to pay the higher legal cost relating to procurement advise, with the exact value agreed ahead of the Board meeting on 1 October 2020.

*ACTION LL and RGr to double check amount and update budget*

**8.	Risk Review**

- JA - Introduced the [Risk Register](https://github.com/OpenWIS/openwis-documentation/projects/4):
- JT - Risk 591, work has been done to make the OpenCDMS team more cohesive and should be GREEN or close.
- RGr - agree to be GREEN to remind to keep an eye on what is going on.  Alternatively, as JT is directly involved, could close and JT to report to SC on new risks.
- JT - OK with closing and me to monitor.
- RGr - all OK
- RGr - Risk 594 - keep as is.
- ALL - OK
- JA  - Suggest that for risks rated as Green , we do a high-level review and review again at the next SC.
- ALL - Agreed and no changes OK no change and review at next SC.
- JA - Any new risks?
- ALL - No
- JA  - Do any of the closed risk need to be re-opened?
- ALL - No closed risks to be re-opened from high level review.
- JA  - In Summary one risk (591) to be closed and no changes to others.
- All – Yes.

*ACTION – JA to annotate latest position of all risks and close risk 591.*

**9.	Any other business**
- JT - procurement route in Europe only.  So, procurement falls to small number of partners
- RGr - Yes. Finland, France or UK, even if UK is not part of EU.
- JT - Yes even if UK is not part of EU , UK will be compatible with European law.
- RGr - I approached MF and it is not possible.  So, its UK and Finland.
- MV - Should be possible and could do that.
- JT - that is great news
- SO - Do we have a sense which bidder resources can be reached.  
- MV - Open tender but supplier will have been selected by FMI. So, the work will be via a framework.
- JT - We would need a lightweight tender for an independent partner.
- MV- that is different and maybe need more justification in FMI.
- JT- UKMO doesn’t have access to resources for 6 months.
- SO - timelines means that finalise documentation for procurement in January 2021.
- JT - so a risk as restrictive across two orgs.

- RGr - agree and options:
	•	Go with FMI
	•	UKMO to check whether they can help in January 2021
	•	RGr to see whether Belgian Met Office can help.

- RGr - So, an SC in mid-December to decide route and whether UKMO, FMI or Belgium feasible.  Pending the outcome.
- JT - Prefer to check in early December 2020.  Is this OK for FMI?
- MV - Should have suppliers in place by mid November 2020.  
- SO - Would be good to know the core strengths of FMI suppliers to see what shows up to help options.
- RGr - also to check whether sub-contracting is possible.

*[ACTION MV to establish whether FMI can undertake procurement, whether sub contracting is possible; along with timescales and process by end November 2020.
ACTION - JT and JA to establish whether UKMO can undertake procurement along with timescales and process by end November 2020
ACTION - RGr to establish whether Belgium can an undertake procurement along with timescales and process by end November 2020
ACTION -  SO to provide a more certain timeline (including when requirements for enable procurement to start) by end November 2020]
(https://github.com/OpenWIS/openwis-documentation/issues/590#issuecomment-702186355)*


- JA - in terms of risk (593), shall we allow the actions to take place and decide whether risk when actions are complete?
- ALL - OK
- JT - the CLA work with NWS is being progressed.  
- RGr - need to discuss at next SC meeting .

**10. Summary of recommendations to the Board**

- Approval of:
	•	 the OpenCDMS PMC, OWA rep, and CLA update
	•	Joint meetings re AWS for OpenCDMS
	•	Changes to by laws
	•	Changes to budget
  •	Accept Risk assessment

**11.	Next meeting**

- Agreed to be early December for:
	•	Procurement routes
	•	CLA with NOAA
	•	A more refined timeline for middleware

*ACTION – JA to schedule the next SC meeting date late Nov or early December 2020*

**21.	Closure of the meeting**

The meeting closed at 1455 UTC
