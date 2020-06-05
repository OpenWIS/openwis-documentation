---
layout: page
title: OpenWIS Technical Committee 2020 May
minuteOwner: technical
---

#### 19th May 2020, Teleconference

---

*19 May 2020*

1. **Welcome and introductions**
    - Steve Olson (SO) (TC chair) welcomed all present.

    *- The attendees were:*
      - SO - Steve Olson, National Weather Service, USA [NWS], Chair
      - BS - Benjamin Saclier, Météo-France, France [MF], Vice-chair
      - DP - David Podeur, Météo-France, France [MF]
      - YG - Yves  Goupil, Météo-France, France [MF]
      - WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM]
      - AA - Anuruddha Abhayasinghe, Bureau of Meteorology, Australia [BoM]   
      - JA - Jude Anthonisz, Met Office [UKMO]
      - JR - Jeyoung Ryu (KMA)
      - SD - Sungsoo Do, Korea Meteorological Administration [KMA]
      - MP - Mikko Partio, Finnish Meteorological Institute, Finland [FMI]
      - SS - Stephan Siemen, European Centre for Medium-Range Weather Forecasts [ECMWF]
      - JT - Jeremy Tandy, UK Met Office [UKMO]
      - FB - Fred Branski, National Weather Service, USA [NWS]
      - KS - Kari Sheets, National Weather Service, USA [NWS]
      - MG - Marc Giannoni, National Weather Service, USA [NWS]
      - ZZ - Zhan Zhang, National Weather Service, USA [NWS]
      - KSr - Kuldeep Srivastava, India Meteorological Department (IMD)

    *- Not present:*

      - RGb - Remy Gibault, Météo-France International [MFI]
      - LG - Loïc Le Gallou (LG), Météo France International, France [MFI]

2. **Technical infrastructure: status and plan for future management and operation (including any costs and costs of improvements for SC approval)**
    - SO - We have a new CICD environment in place with no cost due as the components  are open source.  Therefore, the recommendation to the Steering Committee (SC) is that there is no cost or issues for technical infrastructure.
    - SO - Any questions
    - ALL - No. Therefore approved.

3. **Code of conduct and CLA compliance: status, review, and recommendations.**
    - SO - All CLAs are up to date and in place with exception of NWS.
    - FB - NWS’ position is that there is no issue in signing a CLA. However, there is an issue with language in the current version of the CLA from the perspective of US law that is preventing signing up to the CLA.
	  - FB - So I went back to NWS legal counsel who provided suggestions that were presented UK Met Office legal. The outcome is a stand still.  
	  - FB - I am happy to re-open the discussion to agree a language that serves US and all other partners. So, a negotiation between legal counsels of NWS and UK Met Office is needed to come to an agreement.
	  - JT - I understand the need for the CLA to be legally acceptable to NWS and all partners.  I apologies that if you feel rebuffed.
    [ACTION - JT and FB to start a dialogue with respective legal representatives to reach an agreement]( https://github.com/OpenWIS/openwis-documentation/issues/456#issuecomment-634636455)
    - SO - Any other points.
	  - ALL - No

4. **Technical rules compliance: status, review, and recommendations**
    - SO - In summary, some updates are needed to the development and release processes to reflect the new CICD environment.  These updates are in progress of being made by BS and me.  I will agree the revisions with a future TC and then publish.
    - SO - Any questions?
    - All - None.

4.1. **Review of Rules Supplement (see issue #453)**
     - SO - One area of change is to pull out the project delivery section to focus on new projects as this needs an update. BS and SO in process of editing by adding examples. Any questions?
     - All - No
     [ACTION - BS and SO to revise the project delivery section with addition of examples]( https://github.com/OpenWIS/openwis-documentation/issues/453)

*4.1.1 Review of Goals and Metrics.  (see issue #451)*
    - SO - I propose an additional goal with processes from the new CICD environment. I will update the website and develop further via future TCs.  
    - SO - Any questions?
    - ALL – No.

*4.1.2 Review of Quality Measures (see issue #451)*
    - SO - The new CICD environment enables reporting on testing with the GREN plug-in for change logs.  
    - SO - Any questions on all quality measures?
    - WQ - Are these for the CICD environment or in general?
    - SO - for the CICD environment
    - ALL – Agreed
    [ACTION - SO to add the agreed quality measure to the web site]( https://github.com/OpenWIS/openwis-documentation/issues/451)

5. **Project design authority, standards compliance, and release management: status, review and recommendations**
    - SO - I will provide an update a future TC. I am getting closer to describing a better workflow and guidance for all contributors.   All - agreed.

    [ACTION - SO to propose a workflow and guidance to TC](https://github.com/
    OpenWIS/   openwis-documentation/issues/454 and https://github.com/OpenWIS/openwis-documentation/issues/581#issuecomment-634652718)
  
6. **Key risks and issues of individual OpenWIS Projects: advise the Steering Committee.**

*6.1 	OpenWIS 3.x*
   - SO - EOL risks were discussed PMC on 18 May20. The outcome is that the items in the existing middleware RFP need to remain in scope. A budget for external spend previously approved in 2019.   
   - SO - The only unknown is whether Keycloak is viable replacement for OpenAM and/or OpenDJ and whether the work to replace and migrate will be done with internal or external effort.

   - SO - Any questions?

   - All - No

*6.2 ExceltoWIS *
   - SO - Any questions on ExceltoWIS?  
   - All - No

*6.3 WIS2 prototype*
  - SO - A previous decision was made that if GitHub vulnerabilities arise, we can move the work elsewhere and not update vulnerabilities. So, accept risk or consider alternatives? Any comments?
  - MG - Do we have a category for ‘unsupported’?
  - SO - we would have to formalize this? JT what is your view?
  - JT - Another way is to state that its closed and is not being supported. So, rather than creating a new workflow, label it as a closed project.
  - ALL - Agreed.

  [ACTION - SO to create an issue to draft a statement to reflect WIS2 as being a closed and unsupported repo, for approval by the TC]( https://github.com/OpenWIS/openwis-documentation/issues/581#issuecomment-634652718)

	- WMO Expert/Task Team activities and potential impacts to TC for supporting OpenWIS

  - SO - Following on from the discussions at the 18 May 2020 PMC, I will set up a new workshop.

  [ACTION - SO to set up a workshop to a time-scale and format agreed by the SC to gain ideas for potential work that would benefit WIS2]( https://github.com/OpenWIS/openwis-documentation/issues/583)

**7. Forum**
  - SO - It’s time to renew the forum license with Discourse, so we need to workout the process for renewing with MFI and NWS.  The cost is a an annually recurring 1000 USD.
  - SO - KS what are your thoughts on invoicing MFI ?
  - KS - No process for receiving money that I am aware of.
  - JT - easiest way forward is for the OpenWIS Association to purchase the license going forward as well budget for 2020.
  - JT - is the forum being utilized?
  - SO - not much. I propose that an evaluation of Discourse vs GitHub equivalent or stop using a forum.
  - WQ - I must admit I wasn’t sure what this was for?
  - JT - Discourse was about engaging the users rather than technical software development.
  - SO - license is currently expired.
  - MG - No use has been taken place.
  - JA - My proposal is to decide now rather than an evaluation as they is no current usage and to save management time all round.
  - JT - OK so, the TC take a decision to lapse or evaluation to the vote.
  - All – agreed

**8. OpenCDMS**
  - SO - It would be good to get a brief on what is seen as the role of the TC regarding the OpenCDMS project.
  - JT - Just oversight.  They will have their own GitHub repository, TC could help in implications of licencing choices, architecture review.  Certainly not coding.  They will be self-contained have their PMC.
  - SO - Any onboarding needed?
  - JT - Jude, what is the status of the Charter?
  - JA - The Charter has been updated by Steve Palmer, following clarification sough from a review co-ordinated by Rémy Giraud in January 2020, and has been shared with Rémy Giraud, yourself, Weiqing, the TC and is tabled for approval at the SC on 26 and 28 May 2020.
  - SO - any more questions?
  - All - No. 

**9.  Creation of overall work plan for 2020**

*9.1 OpenWIS 3.x*
 - SO - the current view of the content of the work plan is three potential areas for OpenWIS 3.x middleware, review Geonetwork? Keycloak? and Others? SO - To begin with what are the thoughts re Geonetwork investigation?
 - JT - Geonetwork is scattered throughout OpenWIS. So probably not easy but probably warrants an investigation.
 - MG - A clean sheet of paper approach, i.e. an installation of the latest version of Geonetwork and then craft the OpenWIS data services into Geonetwork.
 - BS - The emphasis more on assessing the latest version of GN is suitable for WIS2.
 - WQ - We don’t know what the metadata is going to be like for WIS2 for WIS2 so how can we know that GN will be good or not?
 - BS - I think WIS2 will be compliant with a form of GN.
 - SO - any more questions?
 - All - No.
 - SO - Will have a proposal for the investigation for the SC to decide on 26-28 May 2020
 - JA - what is the priority of the Geonetwork investigation, compared with middleware and Keycloak?
 - SO - Middleware and Keycloak have a higher priority.
 - ALL - agreed.
 - JA - There is also a need to establish what the position is in MFI regarding OpenWIS 3.x before commencing work.  As previously agreed, at the PMC on 18 May 2020, this is to be raised by JT at the SC on 26 to 28 May 2020.
 - SO - the outcome of the Keycloak investigation will be available by late summer which will inform whether additional external expenditure and procurement is needed.
 - SO - The Geonetwork investigation will be completed by September 2020.

[ACTION – SO and BS to update the existing OpenWIS 3.x Charter with the latest plan and time-scales and prepare new Charters for the Keycloak and Geonetwork investigations]( https://github.com/OpenWIS/openwis-documentation/issues/584 https://github.com/OpenWIS/openwis-documentation/issues/585 and https://github.com/OpenWIS/openwis-documentation/issues/586)

*9.2 WIS2 pieces*
- SO - This is to be determined and will be based on the outcome of the workshop to be scheduled (see action in section 7, above).  

*9.3 Summary*
- SO - A nominal provision for 2020 is as follows regarding spend:
- CICD - zero
- OpenWIS 3x – same as agreed in 2019.
- Keycloak – may be needed, subject to outcome of investigation by NWS and MF.
- Forum - Zero
- WIS2 - subject to outcome of the workshop.

Closed at 1432 UTC
