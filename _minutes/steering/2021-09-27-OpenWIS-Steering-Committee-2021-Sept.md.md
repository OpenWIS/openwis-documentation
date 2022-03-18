---
layout: page
title: OpenWIS Steering Committee September 2021
minuteOwner: steering
---

#### 27th September 2021 – MS Teams video-conference

---
**1. Welcome and introductions**

  - JT welcomed Alec Slater to the meeting who is taking the minutes for this meeting.
- JT and RGr agreed for JT to chair the meeting.

**2. Attendance**

  - JT Confirmed that 7 out of 8 delegates attending, therefore quorate.

*2.1 Current members that were present*

  - Rémy Giraud (RGr), Météo France [MF] - SC Chair
  -	Jeremy Tandy (JT), Met Office [UKMO] - SC Vice Chair
  -	Loïc Le Gallou (LG), Météo France International [MFI]
  -	Kari Sheets (KS), National Weather Service [NWS]
  -	Mikko Visa (MV), Finnish Meteorological Institute [FMI]
  - Weiqing Qu (WQ), Bureau of Meteorology (BoM)
  -	Sungsoo Do (SSDo), Korea Meteorological Administration [KMA]

**2.3 Other attendees**

  - Steve Olson (SO), National Weather Service [NWS]
  - Alec Slater (AS), (OpenWIS Association Secretariat)
  - Baudouin Raoult (BR) (ECMWF)

**3. Approval of the agenda**

  - JT asked for item 7 to be deferred to the next meeting. The agenda was approved.

**4. Approval of previous minutes**

  -  All - No changes. Therefore approved.

**5. Open WIS 3.x Middleware RFP (scope, costs, timescale and acceptance criteria)**

SO provided an update on the following 4 parts (all points below are by SO unless stated by another steering committee member):

 **i.** **Open WIS 3.15 release**

- Issues worked through, which are  mostly relating to the difference between a DCPC and GISC; both MF and NWS have independently verified a running instance based on v3.15
- There are 6 minor fixes remaining, but they don’t cause operational issues. These will be incorporated into the RFP.
- Also looking to incorporate removal of OpenDJ and OpenAM into the RFP.
- At this time there is no need to update the amount of time. It is still achievable in a 6 month time period.
-The scope is still broadly the same and at the moment and the funds appear to be adequate.
- There is a meeting on Wednesday 29th September to confirm final timescales, scope, costs and making sure that all participants have the same understanding. 
**Action: The steering committee will be updated via the minutes from the meeting.**

**ii.** **Examine GitHub Automation**

David Podeur assessed, and indicates that we don't want to use GitHub automation, so we should stick with current arrangement, which is TravisCI and Sonar.

**iii.** **Travis CI migration**

- Travis consolidating their .org and .com platforms together.
- Successfully moved OpenWIS from .org to .com.

**iv.** **Licensing arrangement**

- There are now 3 different options. We are currently using the free license option with 10,000 units of credit on an annual basis. The credit are used in the following way: 10 credit per very minute of build and OpenWIS build takes approximately 18 minutes per so approximately 200 credits per build. This is affordable, but we may exceed this limit if we have a lot of, say, cybersecurity issues to fix.
- There is an option to be an open source project. Please refer to the link below:

[https://opensource.org/docs/osd](https://opensource.org/docs/osd "https://opensource.org/docs/osd")

BR - was surprised that the code must be being actively maintained (latest commit in the last month)

- We would be considered active - just in managing security vulnerabilities.

RGr - mentioned that this clause is about who may request to become a Travis Open Source project - identifying either the project lead OR a regular committer (who commits at least once per month). From my perspective if we ask and they say no, we have no issue.

- We should ask Travis to become an open source project because there is nothing in the criteria that we don’t comply with.

RGr -  asked if there is any risk because it looks like we are moving from a free limited to a free unlimited license. It looks like a good deal. An entry license is USD70/month if the free unlimited is revoked and we need more credits

- The only issues is future unknowns and when it could change. There are no issues at present.

***Action: SO to request a move from the current license to a free open source license, which removes the 10000 unit credit limit***


**6. **Procurement partner related contracts and payment schedule re OpenWIS 3.x Middleware RFP****

LG -  informed that the framework contract had been created. It is a short document concentrating on the relationship between OpenWIS association and FMI, rather than the whole contractual relationship. The framework contains the following 10 articles:

i. Suppliers obligations
ii. Timescales
iii. Acceptance tests
iv. Terms of payment [payment schedule]
v. Intellectual property - Owned by OpenWIS Association
vi. Documentation
vii. Warranty
viii. Duration
ix. Termination
x. Agreements and Law

MV - advised that he is still waiting for feedback from FMI legal department, which he anticipated today (27/09/21).

JT - said that pending a review from FMI, the contract should be referred to the Technical Committee to assess all the Articles from a technical perspective (i.e. what is being delivered), especially A3 acceptance tests. After this has been completed then it should come back to the Steering Committee for final approval (e.g. payment schedules).

RGr - mentioned that the contract is to protect both FMI and OpenWIS Association. He said that we need to make sure that FMI don't get into the situation of accepting the work (and being liable to pay), and OpenWIS Association not accepting the work - and not paying FMI.

JT - said that we need to be assured that the acceptance criteria are propagated through to the contracts between FMI and E-Work, and E-Work and AKKA. RGr agreed.

RGr - mentioned that the use of the term "supplier" to describe FMI doesn't really fit? The description in the contract doesn't reflect reality. He said that we know that ALL work will be subcontracted by FMI. The real emphasis should be about delegating procurement to FMI with a need for them to follow EU public procurement rules. The contract should be more like a contract between peer organisations (e.g. "legal agent") - not a purchaser-supplier contract.

LG - advised that our aim is to have a reasonably simple document, avoiding describing all parts of the contractual change.

- MV to discuss RGr’s points above with the FMI legal team. He also asked if the acceptance criteria was in the RFP. SO confirmed that it is in the RFP. MV said that we should refer to the acceptance criteria in the contract.

LG - said that the contract should refer to the RFP for the tests and simply state that the tests need to be done. MV agreed.

MV - agreed to update the steering committee on the internal FMI discussions as soon as possible.

LG - advised that he should have the contract document ready to share with the Steering Committee in the next 2 weeks from the date of this meeting (27/09/21).

JT - asked who is the person that will sign the contract on behalf of the OpenWIS Association? 

**Decision** **It was agreed that RGr should sign it as chair of the Board.**

**7. CLA – single version or project specific****

JT - sent a presentation and three supporting documents to all the steering committee members.

JT - shared and discussed a summary of changes to the CLA proposed by Michael Robbins (Met Office) and Derek Hanson (NOAA).

***Action: KS to confirm with Derek Hanson that marking a commit "US Government Work" is sufficient.***

***Action: AS to store advisory note received from Michael Robins as a document of record.***

The steering committee approved the summary of changes proposed by Michael Robbins and Derek Hanson.

***Action: AS to propagate changes for CLA V5 into what’s in publish on the website, then publish the changes for RGr and JT to review.***

JT - shared and discussed a proposal from OpenCDM project who use CLA-BOT.

**Action: SO to assess proposal for CLA-BOT and verified-commit to determine if it is easy to incorporate into OpenWIS projects with the technical committee.**

WQ - asked if the steering committee had to resign the CLA V5. 

**Action: JT to confirm if steering committee need to resign the CLA V5.**


**8.**	**Retention policy for non-personal data**
- This item was deferred to the next meeting.

**9.** **Future meetings (virtual vs face to face)**

RGr - advised that he believed that the notaries included the legal option to have virtual meetings

***Action: RGr to confirm latest articles have option for virtual meetings.***

JT - asked if physical meetings added any value?
RGr - replied that they do add value. It is the additional context and extra-curricular relationship building that makes valuable. He wouldn’t want them to always be virtual.
WQ -advised that it could make travel budgeting more difficult because it is hard to justify the money and carbon impact to travel every year.

**Decision** - **It was agreed and approved that 2022 annual meeting would be virtual. A decision would be made mid-next year about 2023.**

**10.** **Any Other Business**

- JT asked when the invoice for secretariat work for 2020 would be paid. LG confirmed that it would be paid today (27/09/21).
- JT raised the future of the secretariat work. The Met office can continue to support this function with a new person starting in the role to replace Jude Anthonisz in October / November 2021. RGr thanked JT because he said that we definitely need this role.
- RGr asked for feedback on review of projects for WIS2. WIS2 demonstrator pilot project workshop opened the door for WIS2 in a box. He will discuss this with WMO.
- RGr asked if all attendees could remind their board members to send personal addresses for the changes to the articles of the association.

**21.	Next meeting**
**Decision - It was agreed that the next meeting would be in January 2022.**

**Action: Jude Anthonisz to send out a doodle poll for the date of the next meeting.**

SO - asked for the following to be an agenda item at the next meeting: How OpenWIS association can support WIS2 spec development.

**Closure of the meeting**

