---
layout: page
title: OpenWIS Steering Committee 2020 May
minuteOwner: steering
---

#### 26th and 28 May 2020 - BlueJeans video-conference

---
**1. Welcome and introductions**

  - RGr – introduced the meeting and Nicole Brinsmead (NB), Deputy Director of DDG (Data and Digital)
  -	NB- Welcomed everyone and gave good wishes for a productive meeting and confirmed BoM’s ongoing commitment to the Association and hoped to host the OpenWIS annual meeting in Melbourne in 2021.

**2. Attendance**

*2.1 Current members that were present*

  - Rémy Giraud (RGr), Météo France [MF] - SC Chair
  -	Jeremy Tandy (JT), Met Office [UKMO] - SC Vice Chair
  -	Loïc Le Gallou (LG), Météo France International [MFI]
  -	Sungsoo Do (SSDo), Korea Meteorological Administration [KMA]
  -	Kari Sheets (KS), National Weather Service [NWS]
  -	Mikko Visa (MV), Finnish Meteorological Institute [FMI]
  -	Weiqing Qu (WQ), Bureau of Meteorology (BoM)

*2.2 Members not present*

  - Dr. S.L. Singh (SLS), India Meteorological Department [IMD]

*2.3 Other attendees*

  -	Nicole Brinsmead (NM), Bureau of Meteorology (BoM) (Part of 26th)
  - Steve Olson (SO), National Weather Service [NWS]
  - Stephan Siemen (SS), European Centre for Medium-Range Weather Forecasts [ECMWF]  
  - Jude Anthonisz (JA), Met Office (OpenWIS Association Secretariat).
  - Steve Palmer (SP), Met Office [OpenCDMS Project] (Beginning of Day 28th)

**3. Approval of the agenda**

  - RGr - Is everyone happy with the agenda?
	-	JT - Can we discuss OpenCDMS on Thursday?
	-	All - OK
	-	RGr - So this item confirmed for Thursday
	-	All - No other comments

**4. Approval of previous minutes**

  -  All - No changes. Therefore approved.

**5. Election of chairperson ("TC-Chair") and vice-chairperson ("TC-Vice-Chair") of the Technical Committee **

  - RGr - Do we have to re-elect?
	- JT - Yes
	- RGr - Steve are you happy to continue ?
	- SO - Yes
	- JT - Seconded
	- RGr - BS not here but assumed OK

RES-OWIS The Steering Committee agreed that Steve Olson and Benjamin Saclier were the Chairperson and Vice Chairperson for the Technical Committee, respectively.

 **6.0	Recommendations to the Board regarding admission of new Members and Partners (see Articles 6 & 9, and Rules 4 & 5)**

  - RGr - I believe that we do not have any new candidates.  Is everyone else aware of any?
  - JT - I am not
  - All - No

**7.	Project Reports and requests for Financial Support or changes to existing Charters**

*[7.1	OpenWIS 3.x](https://github.com/OpenWIS/openwis-documentation/issues/497)*

  - RGr - Is the current charter working well for you?
  - SO - Yes.  In terms of going forward there is a work plan I have sent to the SC.  In summary,  no monies to support, but a caveat.  There have been problems with access to Geonetwork repositories, this is now OK.  A new charter – for OpenWIS 4.0 with the outcomes of investigating alternatives to OpenAM and DJ security services components along with middleware work which may require funding if external effort is required.
  - RGr - I was wondering whether we should look at agenda item 10 as we are also discussing OpenCDMS on 28 May and give an opportunity for others to discuss the work plan.
  - All - OK
  - SO - presented the work plan.  Key points:
	- CICD: Work now complete and a CICD environment is in place and tested independently with 3.14.9 build.  Post project work is in progress, i.e. a clean-up privileges within Github and updating policy and process documentation for publication on web site (80% complete).
	- Maintaining OpenWIS 3.x: –investigating of security vulnerabilities is in progress. Second aspect is Keycloak – an investigation in its suitability to replace OpenAM and OpenDJ will commence.  Thirdly, an investigation into the upgrade of Geonetwork is considered.  
	- Another item is the exploring ways in which can be pro-active for WIS2 via a workshop to generate topics of interest such as metadata discovery.  This workshop would initially be discussed with the TC. TC will make recommendations to the SC which may require funding.
	- So, in summary - no funding needed at present.  How to approach if funding is needed, via an SC?
  - RGr - Let’s look at each item to see if there are comments.
  - RGr - Firstly, the CICD work was very successful from specification to procurement to implementation. I would like to thank the TC chairs and members involved, UK Met Office for the procurement, and European Dynamics for the delivery of the solution and training.
  - JT - I think it is a very good piece of work that leaves the Association in a good place.
  - 3	RGr - Item two. Any questions? I appreciate the effort that NWS is making.
  - JA - work that is going elsewhere is the Association that may effect the work plan, i.e. most of you would already be aware that MFI were doing some work, so need to avoid duplication
  - JT - Would be useful to have visibility of work in MFI and use of Github to share work
  - LL - The Singapore project work is in progress and the aim is to complete work in August 2020.
  - LL - MFI will share what’s been done to enable a single unified set of code to be available once MFI acceptance tests have been closed.  
  - LL - Regarding technical visibility, I’ll take an action to discuss with Rémy Gibault.

**[ACTION - LL to let the SC know how visibility of the changes to the OpenWIS code by MFI will be provided]( https://github.com/OpenWIS/openwis-documentation/issues/587)**

  - SO - I assume that for the OpenAM and OpenDJ components, the community version is being adopted?
  - LL - Yes.
  - SO - I assume that you are updating the install and documentation?
  - LL - Yes.
  - SO - Can you share this as well?
  - LL - Yes of course. We are committed to be have a unified code base.
  - JT - That’s great.
  - LL - SO, do not hesitate to contact Rémy Gibault.
  - SO - Do you have a sense of timing?
  - LL - Yes, August 2020.
  - RGr - In terms of versions.  Is there divergence in the code that MFI are working on?  So, will the merge be a big exercise?
  - SO - I think that what we will need to do is for MFI to step through its code and the TC would do an analysis to assess what has changed.  My guess is that it is not a straightforward push.  Somethings would have changed but not too difficult.  Light to medium effort.
  - RGr - To summarise, MFI has confirmed that its development will be made available to the Association and the TC will focus on creating a new version.  Is that correct?
  - SO - Yes. We will create a feature branch
  - RGr - We have previously mentioned that in the work to be done by the Association that are things that MFI would not need.  So, we need to look at what this gap and then look at Keycloak.  Is that correct?  So, we will only be able to understand what is needed for middleware upgrade until September/October?
  - SO - Agreed a good summary.
  - RGr - In terms of planning we are consistent and the Keycloak investigation will report back in summer 2020 , i.e. almost similar timescale and decide in autumn?
  - SO - Yes
  - WQ - Yes
  - JT - I’m Interested on why Keycloak is the candidate for replacing security services (i.e. replacing OpenAM and OpenDJ)
  - SO - From internal investigation and the thought of supporting SAML.  It has also been vetted with MFI and ED for viability - both giving positive feedback.  It is an API focused software package which also lends itself for WIS2 concepts.  It is generally well regarded as an open-source software with good support (incl. Redhat)
  - JT - Great.  Thank you.
  - RGr - My understanding is that we discussed 3 years ago the issue of opensource or being chargeable via Forgerock for OpenAM and OpenDJ.  So, it is good to eliminate the messiness of this.  The options were to get rid of the sophisticated method of authentication (not an option at that time as UKMO wanted a centralised authentication method).  The second option of having OA and DJ support is not available.  Third option is to look at different solution.  Keycloak is a good way forward as it is effectively option 3.
  - SO - Yes
  - RGr - I think it’s good to do the evaluation to see what the costs and effort is.
  - SO - Yes.  We are not backed into a wall with Keycloak, there are several implementation options and support.  It also supports several social media applications. I am impressed with initial evaluation so far by NWS.
  - RGr - We don’t want to move from being dependant from Forgerock to being dependant on Redhat.  So, need to look this aspect of Keycloak closely in the investigation.
  - SO - whole heartedly agreed
  - RGr - Any other points?
  - All - Agreed.

**[ACTION – SO and BS to update the existing OpenWIS 3.x Charter with the latest plan and time-scales](https://github.com/OpenWIS/openwis-documentation/issues/584) [and prepare a new Charter for the Keycloak investigation](https://github.com/OpenWIS/openwis-documentation/issues/585)**

  - RGr - 3rd area Geonetwork.  We first looked at Geonetwork several years  ago and concluded that it was not to be pursued due to the amount of effort needed.  So, a bit worried about this. Is it the right time to consider this as          OpenWIS 3.x is in maintenance mode and is Geonetwork proposal is more than  maintenance?
  - SO - The drive to do this that Geonetwork support and repositories have not been available which generated maintenance issues and caused a concern.  Secondly, a third of current Githubbot security vulnerabilities are not to do with Geonetwork and the analysis has shown a lot of customisation and additional OpenWIS coding that meshes with Geonetwork.  So, a good way forward would be to start a fresh to make it easy to manage OpenWIS code.  The proposal is to investigate the level of effort needed and to look at the future. As the closer we get to WIS2, we need to be ready.
  - RGr - Two aspects. Ensuring Geonetwork is available is a major risk to OpenWIS 3.x running. So, is there a way of limiting the risk , such as creating a fork or copy?  Is this possible?
  - SO - Yes. NWS is looking at this using Maven to rebuild with the repo. So yes.
  - RGr - Good. It would be good to put effort into this to reduce the biggest risk
  - JT - When we know more about WIS2 we can then explore.  However,  Steve is saying that doing an investigation would inform WIS2 discussions anyway.
  - SO - Correct
  - JT - Also I think NWS that would see a benefit.
  - SO - Yes
  - JT - So the investigation is at NWS’ risk, which may or may not be adopted by the Association.
  - SO - Yes
  - RGr - To check.  OpenWIS 3.x is using GN2 to be compliant with WIS1.  Not sure whether there is enough interest in OpenWIS 4.x in using GN3 for potential compliance with Wis 2.0.
  - JT - Steve is proposing upgrading WIS1 compliance. A separate piece of work to for WIS2.  It doesn’t mean than we automatically adopt this GN3  for WIS2.
  - SO - Yes.
  - JT - Enough value is upgrading W1S1 software to enable maintenance.
  - SO - We do not want to have service downtime for existing services based on OpenWIS 3.x.
  - WQ - My understanding is the same, i.e. the pressing need is the operational need.  All we do is minimise effort.
  - RGr - Understood.  I want to avoid spending a lot of time on changing OpenWIS 3.x.  But if NWS needs help, we will support.  But should not think of Geonetwork 3 for WIS2 is a good idea.
  - WQ - I agree that work on WIS2 is too early.
  - RGr - agreed. Any comments
  - JT - All Steve is asking for is an investigation
  - LL - All we have done is for middleware upgrade and this is just an investigation and agree that is too early for WIS2.
  - RGr - Share previous work on GN that was done 5 years ago?
  - JT - SO’s approach is different and GN has changed considerably different that it may not be useful.
  - RGr - In summary, preparing NWS for issues re Geonetwork, so is NWS asking for support?
  - WQ - Having the GN repo is still available to the Association.
  - RGr - So, SC welcome work from TC to investigate a back-up plan for OpenWIS3.x regarding Geonetwork and note the work NWS are planning regarding Geonetwork suitability for WIS2.
  - JT - agreed
  - SO - a good summary
  - All - agreed.

RES-OWIS The Steering Committee agreed for NWS to begin work on investigating Geonetwork to support maintenance of OpenWIS 3.x

**[ACTION – SO and BS create a Project Charter for the Geonetwork investigation to support maintenance of OpenWIS W3.x](https://github.com/OpenWIS/openwis-documentation/issues/586)**

  - RGr - the 4th area - workshop.
  - RGr - Any views and pieces of information?
  - RGr - We can share with the WMO Secretariat and the WMO Group are being changed/formed -  Infrastructure Commission (INFCOM) and  Service Commission. JT and I have been designated as Chair and Vice Chair of the INFCOM Standing Committee on Information Management and Technology – which has responsibility for WIS.  So, clearly, we are going to tackle the WIS2 project as part of this and use the Association as the tool for making this happen.
  - JT - At the PMC meeting , I was aiming to indicate that WIS2 will be measured on the impact and benefit it brings on all members everywhere. There was no understanding of the benefit of WIS1 as it was still based on GTS. So, for WIS2 it is important to understand how value will be provided to NMS’ – i.e. in bandwidth limited settings. So, a useful activity would be look at this – a brainstorm to look this to focus on value.
  - RGr - There is a thin line with wearing WMO hats vs OpenWIS hats. Practically, we can use the Association to help and support development of WIS2.  So, better to have this kind of event with a WMO label on it, i.e. for WMO endorsement as the risk is that non-Association members may not accept an Association-only sourced approach.
  - WQ - agreed
  - RGr - Are WMO  looking for sponsors where the Association could support?
  - JT - I may take a different approach. The Association could invite all to share information.  I.e. like the pub/sub workshop.
  - WQ - What is the concern?
  - RGr – pub/sub was a technical workshop that was instigated by Météo France, not the Association. So, if it’s a workshop sponsored by an NMS who is a partner it could work.
  - JT - I see that this a workshop to invite all members that is co-ordinated by the Association.
  - RGr - OK in that case agreed.  Need to avoid confusion as Chair and Co-chair of Standing Committees.
  - JT - A community workshop with an open-invitation and participation.
  - RGr - agreed
  - RGr - Conclusion? TC to propose one or two ideas to be prepared?
  - SO - agree that TC should internalise this?
  - JT - agreed
  - WQ - who will be organising this? One partner first, then followed by another?
  - All - agreed
  - RGr - timescale? Proposal October 2020? Sooner? Later?
  - SO - October is doable.
  - JT  - workshop or thinking about it?
  - RGr - So outcome of approach needs to be known by end of July 2020?
  - SO - agreed.
  - JT - It’s taken longer than anticipated to form WMO teams.  The original plan was to get approval by Summer.  Now October 2020. So, no discussion on timeline.
  - RGr - By end of June 2020 the makeup of the teams will be known. So, lost 4-5 months compared with original plans.

**[ACTION - SO to set up a workshop to a time-scale and format agreed by the SC to gain ideas for potential work that would benefit WIS2](https://github.com/OpenWIS/openwis-documentation/issues/583)**

  - RGr - thanked all who participated in TC work and plans.

*[7.2	AMQP](https://github.com/OpenWIS/openwis-documentation/issues/440)*

  - RGr - The translation of the project has been a bit broader than the Charter that materialised with pub/sub workshop in early March 2020. I’ll re distribute the minutes.  It was quite successful - 2 tracks. First, the experience of use of pub/sub in different locations – Canada, ECMWF,  Germany and MF…. Secondly - what to do next.  I will make sure the documents of the minutes are available to you.
  - RGr - Normally chair of ET will be leading this.  The Chair and Co-chairs will lead on this going forward.  In terms of the Association, this project is closed and transferred to the official WMO structure as we don’t need to replicate what is being done by WMO ETs.
  - JT - are there implementation activities that the Association should focus on?
  - RGr - We have previously discussed cloud resources. Do you mean something like that?
  - JT - Build something or participate in a pilot or something like that.  I.e. rather than develop specifications.
  - RGr - we have an aspect re AQMP1 that is limited, and each software vendor has introduced additional features in addition to the ISO standard AQMP1. So, no assurance that AMPQ1 client from vendor X will talk to server Y. During the workshop, Brazil and Paraguay agreed to work on reference implementation in Java and Python. These Python and Java versions will be reference implementation. So, no other work to be done.
  - JT - OK
  - All - no comments

*[7.3	Trust Model](https://github.com/OpenWIS/openwis-documentation/issues/441)*

 - SO - Not started anything as no resources.  The question I pose is still a piece of work to be done or is it being picked up by an ET or TT?
 - JT - TT and ETs are yet to be formed.
 - RGr - So, now current work in progress.  Security is a key element, so this work is useful.  In terms of timeframe, we are looking at potentially a year’s time in 2021.  SO - we could follow the pub/sub to flesh this out
 - JT – Please summarise the model
 - SO - establish a small active group and involved WMO at key points.  The Association sponsor the activity under WMO’s authority
 - RGr - I was thinking of a different approach.  The workshop on WIS2 in October 2020, this activity could be taken on board on the items of the workshop.
 - SO - I certainly think that a workshop is a good format but not sure it will be part of the same workshop or not.
 - All - agreed to close and cross refer to a new action regarding the WIS2 workshop

RES-OWIS The Steering Committee agreed the closure of the Trust Model Charter.

**ACTION – SO to close the Trust Model Charter and note that it is a potential item for the WIS2 workshop  Meeting closed at 1352 hours UTC on 26 May 2020.**

The meeting closed at 1433 hours UK time.

**8.	Review new proposals for projects that are compatible with the purpose and objectives of the OpenWIS Association and in the interest of Members and Partners**

*8.1	OpenCDMS*

- JT - Introduced and gave an overview of the Charter.
- JT - in terms of governance there is a PMC and is quite autonomous. Engaging the Association to have broader representation and assuring that it remains open source. PMC has representation from WMO.  There is a broad timescale on the Wiki.  Sponsorship and funding via WMO (nothing required from the Association).
- JT - My view is that this project is compatible with the Association and its aims to improve accessibility of meteorological data globally and as an SC member, I support this Charter.  Any questions?
- WQ - Where did the specification referred to come from?
- JT – developed mainly by Denis Stuber and Bruce Bannerman and approved by WMO EC already.
- SP - The difference of approach did not relate to the specification was about implementation.
- JT - We are also attempting to adopt up to technologies, hence the reference to a ‘cloud first’ approach and there is a pro-active response from technology vendors to participate.  Any questions?
- LL - What is happening with hydrology?
- SP - The definition of climate is very wide – hydrology, agro-meteorology etc. Pretty much any environmental observation that has a time-series component.
- JT - some questions I have asked Steve shared by via Bluejeans chat. Any clarifications needed?
- LL - Is there is an indication of the overall funds required for this project?
- SP - In broad terms 3 million USD from several sources.  International Development will be a major source. Other sources include UK VCP.  It would help if a major NMS joins this project as part of their system life cycle evolution.
- RGr -  With regard to funding, we are aiming at opening the door to changes in the Association by-laws.  At present it would be difficult to accept monies, so we need to note this.
- JT - In the meantime, we could use in-kind contributions.  Firstly, the project will start using CLAs and proceed with their work packages to achieve a milestone by 2023. SP anything more to add?
- JA - Who is the Association representative on the PMC?
- JT - Assuming we support, we will discuss at some point. I would like to propose adding this project to the Association, formally.

**[ACTION – The SC to agree Association representation on the OpenCDMS PMC]( https://github.com/OpenWIS/openwis-documentation/issues/588)**

- RGr - Firstly as Chair of the association I am glad that this project is on the OWA goals and support it.  Any questions?
- SSDo - a very good proposal so agree.
- WQ - A very good initiative and expands the Association and very organised and planned.  Fully support.
- LL - Very interesting topic.  MFI have experience in this area warn about the challenges and time-scales.  Agree and support.
- KS - agree as gives a wider perspective
- MV – I support
- RGr – I open the floor for non-official members to comment.
- SS - Interesting approach. We are giving the message that each partner should also adopt OpenCDMS.
- RGr - Like Copernicus in architecture and approach
- SS - very happy to share info from Copernicus.
- RGr - we should formally vote, so anyone against?
- All - no
- Vote - All SC members endorsed.

RES-OWIS The Steering Committee agreed to adopt the OpenCDMS Project.

- JT - happy to act as the Association representative until PMC is formed
- RGr - shall we agree that PMC formation timescale, September 2020?
- SP - Agreed
- RGr - Therefore a Steering Committee is needed in September 2020.

**9. Recommendations to the Board regarding new or amended Projects (incl. creation of any ad-hoc committees or subsidiary bodies (including PMCs for new Projects)**

- RGr - Only recommendation to the Board currently is OpenCDMS, please see item 8, above.

**10.	Report and recommendations from Technical Committee**

- Covered as part of item 7, above.

**11.	OpenWIS Association logistics**

*11.1	Programme management / secretariat function*

- RGr - first thanks to Jude to all efforts for the number of years. Second, is JA and UKMO are OK to carry on.
- JA - OK to continue up to 15%  assuming fit with budget. JT and I will progress confirmation of budget etc
- RGr - Anyone else for this role?
- All - No.

*11.2	Treasurer*

- LL - Nathalie Dureisseix (ND) is happy to continue and MFI are happy to continue.
- RGr - thanked ND. Anyone else to do this role?
- All - No
- RGr - Any special requirements from a by-laws perspective?
- JT - not aware of any.
- RGr - No immediate issue as ND in post only for one year.
- LL - I hope the limit is not 2 years as it takes a long time to handover/learn.
- JT - Confirmed that all Managing Director roles have a maximum term of 4 years (references - Articles 12.6, Internal Rules 7.2)
- RGr - Suggest an action for the review of the byelaws is to consider whether a limited duration or not for the Treasurer function.

**[ACTION - JA to ensure there is an action to review the term of the Treasurer role](https://github.com/OpenWIS/openwis-documentation/issues/553)**

**11.3 	Information Management [from GDPR](https://github.com/OpenWIS/openwis-documentation/issues/459)** 

- JA - This is a routine check as part of the Privacy Policy and GDPR implementation. I am not aware of any issues
- JT - no issues.

**12. Shaping the OpenWIS Association** 

*12.1.  Status of WIS 2.0 and support the implementation and pilot projects (e.g. funding cloud resources)*

- This is covered in 7, above.

*12.2  How/where can/should OpenWIS Association add value?*

- RGr - We touched on this on 26th May already, so not revisit. Please see 7, above). In essence use the Association as a tool make/facilitate WIS2 happening.  Any questions?
- JT - agreed. Main purpose is to stimulate up take on WIS2 and OpenCDMS is well aligned to this aim. SO, looking not just infrastructure but systems as well.
- RGr - Other aspect is the possibility of using OpenWIS funds to enable this.
- JT - Agreed. So, for example, to assist a WMO ET to move things forward.
- RGr - Any comments
- RGr - Many reasons for WMO restructure, mainly to streamline and make things happen faster.  
- RGr - All please check with your PRs and contacts to make sure your names are on the list of forming WMO teams.

*12.3  Review the continuing need for the OpenWIS Association*

- RGr - The Association is a tool to enable WIS2.20

*12.4. Identification of opportunities for engagement with WMO*

- The following was agreed, i.e. via:
	•	Adopting the OpenCDMS project
	•	Having experts in various WMO teams
	•	Facilitation of WMO initiatives such as for WIS2

*12.5 Review the byelaws of the Association*

- RGr - started working on changing by laws a year ago and revised wording is   available. I am awaiting [feedback](https://github.com/OpenWIS/openwis-documentation/issues/553).  What I hear so far is that there are two potential changes:

	•	Expanding scope of association
	•	Accepting funds

- JT - a new item is the changing of terms of Treasurer appointment term
- RGr – Please have a look at the draft byelaws on github, provide feedback to enable this

**[ACTION – All to feedback proposal to change Association by-laws in time for agreement in September 2020](https://github.com/OpenWIS/openwis-documentation/issues/553)**

- RGr - So, I propose a September SC - a 3 hour virtual session focusing on OpenCDMS PMC and Approving changes to the byelaws.

**13.	Review of Strategic Goals and Metrics (3-year horizon) [metrics]**

- RGr handed to JT for items 14 and 15.
- JT - On the website we only have one goal and metric. In Helsinki (2018) we agreed that the goals were focused on the OpenWIS software and so we removed quite a number of goals and one overall arching goals was agreed.
- RGr - The Association has completed the following since:
	•	CICD environment delivery.
	•	OpenCDMS preparation and adoption
	•	pub/sub progress
	•	Some middleware improvement (v3.14.9)
- JT - what we have achieved has been good and will be interesting how we manage working with a new project (i.e. OpenCDMS).  I believe the current goal still stands.
- JT - we should also add some goals such as for OpenCDMS - a successful PMC up and running and contributions to OpenCDMS.
- LL - metrics should be general rather than tied to a specific project
- RGr - OpenCDMS is forA1. A3 for new versions of byelaws published in Belgium gazette.
-	JT- That’s not a goal
-	RGr - More a metric than a goal.
-	JT - anything else we can think of?
-	All - None
- JT - Please give thought on reasons what each organisation getting back to help formulate a Goal(s).
- WQ - Ability to have OpenWIS software operational
-	JT - A goal re supporting existing implementations of Openwis 3x?
- JT - Is there a goal around international collaboration?
- WQ - Yes
- KS - agree with international development and maintaining existing operational service.
- JT - WIS2 as well?
- KS - Probably
- JT - This could be a metric.  We talked about supporting WMO ET - so a metric on this a potential
- LL - a goal on influencing WMO activity – metric or goal?
- JT - This is potential one, too. Any more?

**[ACTION – JT to draft a set of goals to shape the association and circulate to SC](https://github.com/OpenWIS/openwis-documentation/issues/589)**

**[ACTION – All provide reasons/benefits received to respective organisations as a result of participation in the Association](https://github.com/OpenWIS/openwis-documentation/issues/589)**

**14.	Risk review and development of mitigation plans (i.e. material changes to risks since 30 March 2020)**

- RGr - not aware of any.
- JT - Nor me.
- RGr - Having OpenCDMS is some form risk as this is first major software outside of OpenWIS software itself.
- JT – So, a new risk ‘Failure of the OpenCDMS project has a negative impact on the Association’
- JA - new or addition to existing?
- JT - new.
- RGr - the mitigation is for the Association to help as much as possible.
- JT - Pandemic is a new thing.  Has it impacted us much?  
- RGr - meetings are OK.
- JT- Not travelling is not having a risk.
- All - Agreed.
- JT  - also have an existing risk that major project fails to deliver.
- JA - proposed a risk review at the SC in September 2020.
- JT and RGr - agreed
- JA - Suggest keeping OpenCDMS as a new risk to focus and review whether it forms part of major project in September 2020.
- RGr - No other changes to risks since last review
- All - agreed

**ACTION – JA to add a new risk regarding OpenCDMS and add risk review to the SC meeting in September 2020**

**15.	Finances of the OpenWIS Association [Treasurer]**

*15.1	FY2019 expenditure*

- LL shared the expenditure for 2019 prepared by Nathalie.  Key points:
	•	Treasurer function operated by MFI (Nathalie) since 01/01/2019
	•	New bank account opened for and owned by OpenWIS association
	•	Account owned by MFI was still active in 2019 (final transfer done on 31-12-2019)
	•	Income -  member contributions were 184k Euros, 200k euros received from IMD for membership fees.  This gives a healthy total of 399k, which is more than last year
	•	Expenses -CICD environment and legal expenses 54k Euros.  Société Générale bank fees charged were not expected.  ND is chasing to reverse.
	•	Net position is 161k Euros in surplus.  Mainly because of IMD fee income.
- LL - Any comments?
- RGr - Can you remind use of recurring fees, I think is mainly Jude and Nathalie.
- LL - Yes. about 15k Euros
- RGr - Discourse payments may be due?
- JT - is that for 2019 or 2020?
- LL - Maybe we discuss as part of budget for 2020?
- ALL - Yes
- LL - So, the statement of financial position – Gross assets are 547k Euro. Net Assets Net Assets 535k Euros.
- LL - Any questions
- WQ - Are the assets in cash?
- LL - It’s what in the bank account
- LL - Member contributions.  NWS is high mainly due to organisation of the annual meeting in 2019.
- LL - not received any more responses.  Any comments?
- ALL - No.
- LL- There are of course contributions from all but not everyone declaring.
- LL - lets finish with the 2019 budget review.  Key points:
	•	The project costs  80k provision. But only did CICD and spent only 37k euros.
	•	Contingency of 10k was not used.
	•	Bank fees incurred for the MFI account
- Any questions?
- All - No.

*15.2 Review of need for additional finance and Budget for 2020/21*

- LL - So budget for 2020.  Key points:
	•	DropBox duplicated.  Therefore, remove one.
	•	At TC we decided that we would not renew Discourse
	•	KS - 2019 fee for Discourse can be treated as an in-kind from NWS.
	•	LL - therefore to remove discourse fee for 2020 budget
	•	LL - Project costs - Middleware - so we should discuss about how much we should spend on this and other projects.
	•	Other items in budget per slide
- WQ - any ongoing cost for CICD environment?
- SO - no budget required?
- WQ - Any cloud hosting?
- JT - we are using public repos. So. no.
- RGr - thank you.  The budget is in fact a Board issue. So, any questions on the 2019 finance, please report to LL.  I thank - ND and LL.
- All - OK
- RGr - the 2020 budget for agreement and recommendation to the Board.
- RGr - Remove one Dropbox entry. I propose we continue with DropBox but not use hosting.
- RGr - 5 items - domain name, Secretariat, Treasurer, Account fees are recurring.
- RGr - Project costs – middleware and potential Keycloak. Work will be known around October 2020, so is this for 2020 or 2021?
- LL - we should budget for what we are going to spend in 2020.  I agree that we would not be able to spend the budget amount in 2020.
- RGR - What’s your view SO?
- SO - Agree.
- RGr - I don’t think we need any money based on this?
- LL - We can put in allowance or put nothing and use contingencies.
- RGr -what is good practise?
- SO - No expenses expected in 2020 for GN work. Also, the wildcard is the work to integrate work on OWIS3x from MFI.
- LL - Work for the integration would need to be funded.
- RGr - we are not sure on the amount.
- LL- I think we can start this year but not finish so an amount, so a provision could be made and reviewed later this year.
- RGr - I don’t mind. Whatever is best practise?
- LL - My experience it is best to have value to reflect the intention of starting the work and reduce the contingency as it was not used last year.
- RGr - Any views?
- JT - agreed
- All - agreed
- LL - any amount for Keycloak?
- SO - Depends on the outcome of the in-kind initial investigation
- LL - Ok
- RGr - Not include is the figures for Belgian law advice on procurement.  This was a key piece of work and cost 4235 euros.  So, this means that cannot ask MFI for procurement as public regulations are required.  Therefore, I have been asking whether MF can do the procurement and am progressing this and will follow up when the middleware position is known.
- JT - is FMI able to support with procurement activity.
- MV - I can check.  We are doing a competition and will likely have new suppliers in 2021.
- JT - would FMI’s procurement team be able to do for the Association?
- MK - I can ask
- JT- UKMO Procurement team pre-occupied on a big procurement. So, no capacity.
- RGr - The idea is that an organisation does the procurement and charge the Association when complete.  So, when asking FMI to make sure the process is clear to them,
- WQ - if any of the partner can do the procurement as long as its public. Does is it matter if the regulations, for example BoM’s regs may be different to UK for example.

**[ACTION WQ, MV and KS to check to check whether it is possible to undertake a procurement on behalf of the Association and inform the SC]( https://github.com/OpenWIS/openwis-documentation/issues/590)**

- RGr - I believe that is possible as you are public body.
- JA - should be have a 2020 budget allowance for legal work?
- RGr - LL best practise – reserve for project or general contingency?
- RGr- thanked Michael Robbins for advice so far.
- LL - Leave as is.
- RGr - OK.
- LL - keep reserve as 10,000 euros?
- JT - leave as is.

*16.	Recommendations to the Board to make and adopt, alter, supplement or repeal the Internal Rules*

- JT - I’m not aware of any
- All - No

**[17.	Outstanding actions](https://github.com/OpenWIS/openwis-documentation/issues?page=1&q=is%3Aopen+is%3Aissue+label%3A%22Steering+Committee%22)**
- RGr -we have covered risks, CLA, 2019 budget,
- RGr Any further comments?

**ACTION - JA review and close as required**

**ACTION - KS and MV to review actions and decide whether to attend a quick 15 min session before the Board.**

**18.	Next meeting**

- RGr – agenda items - OpenCDMS, Change of Association by-laws and risk review in late September 2020.

**ACTION – JA to set date for next SC as soon as possible**

- JT Next AM in BoM ?
- WQ - All agreed and set

**19.	Any other business 	RGr - any comments?**

- All - no

**20.	Summary of recommendations to the Board**

- Budget
- OpenCDMS
- Info re by laws discussed by end Sep and following Board meeting
- Procurement constraints

**21.	Closure of the meeting**

Meeting closed 1407 UTC on 28 May 2020.
