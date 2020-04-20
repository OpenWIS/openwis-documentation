---
layout: page
title: OpenWIS Technical Committee 2020 March
minuteOwner: technical
---

#### 20th and 27th March 2020, Teleconference

---

*20 March 2020*

1. **Welcome and introductions**
    - Steve Olson (SO) (TC chair) welcomed all present.

    *- The attendees were:*
      - SO - Steve Olson, National Weather Service, USA [NWS], Chair
      - BS - Benjamin Saclier, Météo-France, France [MF], Vice-chair
      - WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM]
      - JA - Jude Anthonisz, Met Office [UKMO]
      - JR - Jeyoung Ryu (KMA)
    *- Not present:*
      - DP - David Podeur, Météo-France, France [MF]
      - MV - Mikko Visa, Finnish Meteorological Institute, Finland [FMI]
      - MP - Mikko Partio, Finnish Meteorological Institute, Finland [FMI]
      - KL - Kwangjae Lee, Korea Meteorological Administration [KMA]
      - SS - Stephan Siemen, European Centre for Medium-Range Weather   
        Forecasts [ECMWF]


2. **Discussion of Governance surrounding future OpenWIS builds**
    - SO - gave an overview of the proposal and key points.
    - WQ - Is it clear which aspect of the code need updating and is this
      covered as part of the CICD work?
    - BS - We have a list of the areas that need updating and I get Zhang
      to present.
    - JA - Can we sign-off now as not much attendance at this meeting?
    - All - Agreed some amendments for the proposed governance arrangements
    - JA - We can suggest that this meeting was agreed in principle and
      give recommendations on 27 March 2020
    - All – Agreed the content and layout of the agenda.

3. **Discussion about timing and what to include in middleware upgrade now
     that we have a new 3.14.9 build with Java 8, Centos7, Wildfly 15, etc**

    - WQ - All listed items seem to be that should be done.
    - SO – In term of the process, there needs to be an open process for
      the wider community.
    - BS – Re security service, the key one is to replace OpenAM and   
      OpenDJ with an opensource identity server - Keycloak.
    - SO- does it work with Sonar Cloud?
    - BS - also works with auto registration. Everything is configurable.
    - SO - Postgres 10 vs 11? As we have been with version 9 for a while?.
    - SO - If CentOs7 adopted then Postgres 10 comes with it.  Postgres    
      11 requires a separate build.
    - BS - we don’t use much Postgress functionality, so shouldn’t be any
      difficulty.
    - SO - agreed but if you are managing a system, it is much easier to
      patch items that come natively.
    - BS - We should change the RFP to ask for CentOS 8.
    - WQ - we use Redhat.
    - SO/BS - CentOS is a branch of Redhat but free.
    - WQ - In process of moving to Redhat so CentOS is going to be in use
      for a while.
    - BS - We can ask the RFP to say able to run on CentOS 7 and 8.
    - BS- All OK with this?
    - All - Yes.
    - BS - time-scales?
    - WQ - RFP is as it with the amendments proposed.
	  - BS -another TC is needed.
	  - SO – the next session will be on 27 March 2020. 

*27 March 2020*    


4. **Discussion on new CI/CD environment for builds**

    - SO gave an overview of the CI/CD work:
      - Quick brief out (tools: travis-ci, sonarcloud)
      - Videos for Day 1 and Day 2
      - Presentations used during training.  This was emailed to TC mailing
        list
      - Successfully built a 3.14.9 release with Java 8.  It’s available in
        github
      - Build Team established.  It’s not too late to join!
      - Discussion of Governance surrounding future OpenWIS builds

    - SO – presented the proposed governance arrangement.
    - ALL – agreed 


5. **Discussion about timing and what to include in middleware upgrade now
     that we have a new 3.14.9 build  with Java 8, Centos7, Wildfly 15, etc (Timing for RFP)**

     - It was agreed that the updated RFP document will be available by
       June or July 2020. 
     - The aim if to consider alternatives to openAM/OpenDJ. 
     - Both MF and NWS staff will team up to look at this alternative. 
     - The benefit to the Association is that, if this can be done within
       the partnership, it will greatly reduce the middleware refactor effort that would need to be done via a third party supplier.
     - Depending on the length of the procurement process for work that  
       needs to done by a third party, all refactoring is forecast to be complete by December 2020.
     - At present, indicative budget of 50k Euros is envisaged for work to
       be done by a third party.
 
6. **Close**
