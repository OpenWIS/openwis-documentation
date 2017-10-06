---
layout: page
title: OpenWIS Technical Committee 2017 September
---

#### 28th September 2017, WebEx - meeting minutes

---

## Results of poll on pilot project proposals

| TECO Demo Proposal |  Points |  Bonus Points   |   Final Score |
| --- | --- | --- |
| OPP-6: WIS Djibouti   |     60      |     96     |      156 |
| OPP-1: Pub-Sub Notifications  |   43      |     96     |      139 |
| OPP-5: WIS Dashboard | 34      |     84     |      118 |
| OPP-12: End to End Pilot Proposal     |       47     |      60     |      107 |
| OPP-7: Catalog Synchronization Improvements | 34     |      72      |     106 |
| OPP-2: Modularity Demonstration: Security |        26    |       72     |      98 |
| OPP-10: CMS Webportal       |        26     |      72      |     98 |
| OPP-8: Security | 23      |     60     |      83 |
| OPP-3: Distributed Monitoring  | 22     |      60      |     82 |
| OPP-9: Catalog Search Services | 33       |    36      |     69 |
| OPP-4: Excel2WIS Electron      |     20      |     24     |      44 |


| Technical PoC Proposal | Points |  Bonus Points   |   Final Score |
| --- | --- | --- |
| OPP-1: Pub-Sub Notifications   |  45      |     96     |      141 |
| OPP-6: WIS Djibouti     |   28     |      96      |     124 |
| OPP-5: WIS Dashboard | 36      |     84     |      120 |
| OPP-2: Modularity Demonstration: Security    |    47    |       72      |     119 |
| OPP-7: Catalog Synchronization Improvements | 37        |   72     |      109 |
| OPP-10: CMS Webportal       |        33      |     72        |   105 |
| OPP-12: End to End Pilot Proposal      |      43      |     60       |    103 |
| OPP-8: Security | 34   |        60      |     94 |
| OPP-3: Distributed Monitoring |  17   |        60     |      77 |
| OPP-11: Peer2peer   |      21     |      48     |      69 |
| OPP-9: Catalog Search Services |  32     |      36       |    68 |
| OPP-4: Excel2WIS Electron    |       17   |        24      |     41 |

1st – TECO Demo - WIS Djibouti

1st – Technical PoC – Pub Sub

1. **Discussion about the winning pilot proposals**
    1. SO – Maybe work on more than just WIS Djibouti?
    2. JT – could include Pub Sub and use scenarios for pilot/demo
    3. SO – Top 3 the same for TECO and Tech, provides solid foundation from which to work. Everyone ok with doing both and maybe include the Dashboard?
    4. LM – we should do Djibouti and Pub Sub, if we have time maybe work on the Dashboard.
    5. DW – I agree
    6. BS – Ok
    7. SO – Jeremy will add use cases for Pub Sub
    8. JT – ok [Action-TC-2017-23 Add use cases for pub sub](https://github.com/OpenWIS/openwis-documentation/issues/317)
    9. JT - Jeremy discusses his additions to [OPP-6: WIS Djibouti](https://github.com/OpenWIS/openwis-documentation/issues/309)
    10. JT – We want to make WIS accessible to as wide a community as possible. I’ve not tried to be too prescriptive, to allow us to experiment as we go through the pilot. We can play with AWS S3 buckets to put data on web server
    11. NM – Are we providing CSV packaging for users?
    12. JT – If trivial, maybe. But could use OpenOffice to play with CSV files or other tools available to Mouktar. The important part is that datasets are registered on the WIS, approved by the Djibouti Permanent Representative.
    13. JT – WIS 2.0 design should allow commercial search engines to find data. We could have the same process to harvest. Site maps are simpler – proven to work. The catalogue could be just a simple set of web pages. If you have large sets of data, it would be useful to enhance with search APIs. For the demos – Google may change things sometimes so use a recording of the demo to show working.
    14. JT – We need to flesh out Pub Sub and message queues a bit further.
    15. NM – Are message queues maintained by catalogue system?
    16. JT – Should there be some infrastructure, a deployment locally or in the cloud – to allow Mouktar to add data to a queue and Mariam to receive data?
    17. JT - [Action-TC-2017-24 Provide link to Canadian MetPX site with AMQP](https://github.com/OpenWIS/openwis-documentation/issues/318)
    18. BS – what is the difference for WIS 1.0 and OpenWIS?
    19. JT – ISO19195 metadata too complicated for publishers. Portals mainly used by those that know where to look. We need to reduce the infrastructure and make it easier – saves cost. Use a simple web architecture to get better uptake.
    20. SO – Use of standard data formats XML, JSON etc.
    21. JT – Leads to use of web services, therefore, simple rest based web services. If we can provide the components – makes users' life easier, and helps data publisher to do a good job.
    22. NM – We can create a blueprint to capture what we need – then look at specific technology. We can then start allocating work to groups.
    23. SO – How long to do this?
    24. NM – Diagram can be made by next Tuesday (03/10/2017)
    25. JT – I will try and review this next week too.
    26. NM – We’ll use Jeremy’s narrative to create this.
2. **AOB**
    - LM - Leon announced that he is leaving BoM in November.


---

#### Participants

- SO - Steve Olson, National Weather Service, USA [NWS], Chair
- LM - Leon Mika, Bureau of Meteorology, Australia [BoM], Vice-Chair
- DW - Dominic Woollatt, Met Office, UK [UKMO]
- JT - Jeremy Tandy, Met Office, UK [UKMO]
- NM - Nassos Michas, European Dynamics, [UKMO]
- GT - Giorgios Triantafyllidis, European Dynamics, [UKMO]
- DP - Dimitris Papadeas, European Dynamics, [UKMO]
- BS - Benjamin Saclier, Meteo-France, France [MF]
- YG - Yves Goupil, Meteo-France, France [MF]

#### Apologies

- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM]
- PN - Paul Nelson, Met Office, UK [UKMO]
- PR - Paul Rogers, Met Office, UK [UKMO]
- MG - Marc Giannoni, National Weather Service, USA [NWS]
- MC - Michael Claudon, Meteo-France, France [MF]
- RGb - Remy Gibault, Meteo-France International [MFI]
- SD - Sungsoo Do, Korea Meteorological Administration, Republic of Korea [KMA], [delegate]
- MP - Mikko Partio, Finnish Meteorological Institute, Finland [FMI], [delegate]
- DJ - Duncan Jeffery, Met Office, UK [UKMO]
