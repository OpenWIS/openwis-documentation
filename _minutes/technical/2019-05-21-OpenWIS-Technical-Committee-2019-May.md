---
layout: page
title: OpenWIS Technical Committee 2019 May
minuteOwner: technical
---

#### 29th - 21st May 2019, Washington, USA

---

1. **Welcome and introductions**
    - Steve Olson (SO) (TC chair) welcomed all present.

    *- The attendees were:*
      - SO - Steve Olson, National Weather Service, USA [NWS], Chair
      - BS - Benjamin Saclier, Météo-France, France [MF], Vice-chair
      - RGr - Remy Giraud, Météo-France, France [MF]
      - DP - David Podeur, Météo-France, France [MF]
      - MV - Mikko Visa, Finnish Meteorological Institute, Finland [FMI]
      - MP - Mikko Partio, Finnish Meteorological Institute, Finland [FMI]
      - SD - Sungsoo Do, Korea Meteorological Administration, Republic of Korea [KMA]
      - KL - Kwangjae Lee, Korea Meteorological Administration [KMA]
      - LG - Loïc Le Gallou (LG), Météo France International [MFI]
      - KS - Kari Sheets, National Weather Service, USA [NWS]
      - SS - Stephan Siemen, European Centre for Medium-Range Weather Forecasts [ECMWF]
      - JT - Jeremy Tandy, Met Office, UK [UKMO]
      - JA - Jude Anthonisz, Met Office [UKMO]

    *- Apologies:*
      • WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM]

2. **Layout of agenda Items**
    - All – agreed the content and layout of the agenda.

3. **Technical infrastructure: status and plan for future management and operation (including any costs and costs of improvements for SC approval)**

    *- 3.1 Definition of new CI requirements definition by mid-June 2019.*
      - The following was agreed:
        - Estimates of effort 6 weeks for set up and 2 weeks for audit. Training to be included within the 6 weeks, potentially as a DEVCON activity. Who would want to be part of this activity? We would do remote web sessions that are recorded that are re-usable.
        - A face-to-face 3-day Developer Conference would take place, that focuses on the quality measures in early September with supplier (so travel cost for supplier). Topics – CI env and quality measure themes (#451).
        - The time and location of the of the Developer Conference to be included as part of contract.
        - The location will be Météo France, Toulouse, 23 to 25 September 2019.
        - Ask contractor whether they can recommend system environment, such as a cloud provider (not provision) based on snapshot of previous CI environment.
        - Share RFP by secure means (I.e. to protect commercial issues)

        *ACTION – JA provide the costs from the work done by European Dynamics work as an indicator of cost*
        *ACTION – SO and BS Discuss other topics for Devcon*
        *[ACTION - LL and SO to present options and costs at the Dev Con for approval by SC following TC endorsement](https://github.com/OpenWIS/openwis-documentation/issues/542)*

        - BS and DP – We need for an environment for development without a CI. Agreed that from considering whether to use a virtual environment or a cloud end, that its best to evaluate a third party could build an environment as OpenWIS 3x is in maintenance development.
        - All - agreed.

        *ACTION - SS to incorporate into RFP or recommend a separate RFP*

        RES-OWIS Recommend to the Steering Committee (SC) the proposal to use external resource resource to help set-up a CI CD environment with follow up audits each year for 2 years with the approach and time-scale for defining requirements by mid-June 2019 and using a Developer Conference on 23-25 September 2019.

    *3.2 EOL and Dependencies.*
      - Agreed to adopt the agreements and approach at the PMC on 20 May 2019- please see #538). The target start date for completion of end of September to benefit from the outcome of the CI development.


4. **WIS2 Security charter**
   - Discussion on the status of this project, along with other was opened and it was concluded that the all discuss all Charters at SC.

   RES-OWIS The Technical Committee agreed to wait until the WMO reform per PMC discussion before any marketing is conducted.

   - In respect of the AMQP Project Charter, commissioning resource for implementation within MF and will provide outcome of report by end of calendar year.

   [ACTION - RGr to provide an update report by December 2019](https://github.com/OpenWIS/openwis-documentation/issues/541)

5. **Implications of issues arising from OpenWIS 3x: recommendation to SC**

   RES-OWIS it was agreed to recommend the approach, agreed at the PMC on 20 May 2019, regarding Keep OpenWIS licence free as a proposal to the SC.
   - The following decisions arising from the PMC were agreed by the TC:

   RES-OWIS Ensure that the dependency list is updated regularly.
   RES-OWIS Adopt Wildfly 15, Sol7 and Postgres 11.
   RES-OWIS Only upgrade to the latest version if a security vulnerability exists and upgrade to the relevant version that resolves the security issue.


6. **mplications of issues arising from the PMC for WIS2 studies / projects: recommendation to SC**
   - Agreed that the will SC clarify the procurement approach to TC for items above.

7. **[Code of conduct and CLA compliance: status, review, and recommendations to SC](#456)**
   - SO - presented the updated Code of Conduct.
   - ALL - No issues.
   - [CLA terms are is in discussion with NWS Legal. ACTIONS are here -](#456 (comment))
   - JA - CLA for MFI needed.
   [ACTION - LL to upload or send CLA](https://github.com/OpenWIS/openwis-documentation/issues/456#issuecomment-495164426)
   [ACTION JA to change Board members – Rémy and Nathalie on web site](#544)

8. **[Technical rules compliance: status, review, and recommendations to SC](https://github.com/OpenWIS/openwis-documentation/projects/9)**

    RES-OWIS Agreed to implement changes discussed at the PMC on 20 May 2019 by updating the Association website.

9. **Project design authority, standards compliance, and release management: status, review and recommendations to SC**

    - Agreed that changes to web site for ‘Projects’ tab, quality measures were discussed at the PMC and are to be implemented, i.e.:
        - #449,
        - #450,
        - #451,and
        - #453

    - Agreed that the Release Management process as discussed at the PMC to be updated, i.e. #454

10. **[Outstanding actions](https://github.com/OpenWIS/openwis-documentation/issues?q=is%3Aopen+is%3Aissue+label%3A%22Technical+Committee%22)**
    - JT - These were reviewed at the PMC yesterday. Quite a number will be closed.
    - JT - Are you getting active participation in the telco meetings. Steve and Benjamin?
    - SO - Could be better. Seen a decline in BoM’s participation.
    - MFI - depends on subjects and activities.
    - KMA - operational implementation and testing
    - FMI - Happy to participate in testing and implementation.
    - CS - Is it worth doing a Doodle poll to see the best time slots and schedule.
    - JT - is it the timing or is the subject matter.
    - JT - Are there other topics that would be interesting?
    - SO - The only thing we haven’t been able to do facilitate updates on technical standards, which may increase interest.
    - CS - May be worth recording a session which has enough of a quorum.
    - JA - 4 TC meetings in 15 months. More PMC sessions. What would be a good subject to discuss and gain knowledge rather than having TC meetings?
    - RGr - WIS2 on AMQP is good prospect as it has high future potential. So, a kind of PMC session focused on AMQP.
    - DP - Enable / encourage MSS teams to participate on AMQP testing as it would help them.
    - RGr - Aviation services are adopting AMQP, so awareness, knowledge and testing would help them.
    - MV – We can also participate in AMQP testing

   RES-OWIS recommend to SC that WIS2 and technical updates to be part of TC meetings and encourage MSS team to attend TC meetings.

  *Forum*
  - SO - proposed that a strategic item should be added.
  - JT - Is it possible to use to the Github credentials to log into the forum?
  [ACTION - SO to explore whether the credentials used for accessing Github can be used for accessing the forum (which is based on Discourse) to make it easier to manage both tools](https://github.com/OpenWIS/openwis-documentation/issues/549)
  - MV - Installation and upgrade support documents.
  - ALL - no other suggestions
  [ACTION - SO to add OpenWIS 3x installation and upgtade support documents to forum](https://github.com/OpenWIS/openwis-documentation/issues/546)
  - JT - Add documents as requests are received from MG.
  - BS - Sub categories under ‘documents’
  - BS - ‘OpenWIS Project’ to ‘OpenWIS Core
  [ACTION – SO to make changes to the description of OpenWIS from 'OpenWIS Project' to 'OpenWIS Core'](https://github.com/OpenWIS/openwis-documentation/issues/547)
  - BS - Clarify where to register a bug – on forum or github?
  - JT - Can have discussion in forum re bugs but the store of the bug is GitHub, so GitHub should be referenced when closing a thread.
  - BS - Clarify what can be seen without registering.
  - SO - Private while being set up and public in the future.
  - BS, LL, SS – would prefer to change to public
  [ACTION – SO to change to forum access to ‘public’](https://github.com/OpenWIS/openwis-documentation/issues/548)
  - SO - what tags should be adopted. For example, 3.14.8 is a tag.
  - JT - Let the forum be populated and then decide what tags to add.
  - SS - Installation related questions are usually the most common discussion.
  - RGr - Prefer to see content and then see what happens
  - JT - worth having a category for each project.
  - BS - in MF use a category and no-sub tags.
  - JA – Explore auto-tagging plug-ins
  - RGr - Add Core and Excel2WIS and WIS2 Projects.
  - SO - And other general questions.
  [ACTION – SO to explore auto-tagging plug-ins and Add OpenWIS Core, Excel2WIS, and WIS2 as tags to the forum](https://github.com/OpenWIS/openwis-documentation/issues/549)


**11. Any Other Business**

  *11.1 AISBL - Website domain issues. Two options for resolution:*
   - Sub domain, or
   - Re-direction from HTML page from current website to Github website using HTML (OpenWIS ranking will be low bit the website will be indexed).

   RES-OWIS The Technical Committee agreed that re direction should start immediately and workout the proper solution in slower time.

 *11.2 Met Office GISC site has the word ‘beta’, this should be removed to reflect the operational status of the GISC.*
 ACTION – JA to check with MSS team in UKMO

  *11.3 SO facilitated update of the matrix of OpenWIS implementation*
   - SO - Should the TC share known vulnerabilities and issues to each organisation that has OpenWIS installed?
   - SS - This could be useful in ensuring the service is robust.
-   RGr - A operational GISC would have an interest, but would a DCPC be interested?

**12. Close**
