---
layout: page
title: OpenWIS Technical Committee 2017 August
---

#### 10th August 2017, WebEx - meeting minutes

---

1. **Understanding what's meant by maintenance mode in support OpenWIS 3 going forward**
    1. SO - I would like to start by discussing what it means to have OpenWIS v3 in maintenance mode.
    2. PR - It means that we do maintenance tasks on OpenWIS v3 as required. We have taken some time to get a work plan together, mainly because we have been discussing the WIS 2.0 pilots, but it was always intended that we would do maintenance tasks on OpenWIS v3.14. We have a Kanban board specifically for OpenWIS Core Maintenance work as well as for development [here](http://openwis.github.io/openwis-documentation/kanban/). DP has been doing some work on the ForgeRock issue, but he is almost finished now. He could be free to do other OpenWIS 3 maintenance work if we wish. Just put some tasks on the Kanban and we can take it from there.
    3. SO - MG, could you bring us up to date on the work you've been doing.
    4. MG - It turns out that upgrading to Java 8 and Wildfly isn't a big deal, but it has broken JNDI, so we're looking at that. I would like to speak to LM about that.
    5. MG - Also we're looking at the Spring framework.
    6. PR - Ok, so add some Kanban tasks and we can help out where required.
    7. MG - Ok, there, I'm adding them.
2. **Proposed Pilot Studies**
    1. SO - MF emailed to say they are unable to attend the meeting due to holidays, but that they will add some pilot proposals on their return. We may need to schedule another meeting to discuss those.
    2. PN - I note there is no pilot proposal suggesting that we use cloud platforms, eg: Azure AD as SAAS for authentication. Since it is free and easy, I expect to be discussing using these services for the PoCs.
    3. SO - Do you have any idea how we would go about prioritising the proposals?
    4. PN - I assume the SC would do that.
    5. PR - No, the SC delegated the selection of individual pilot proposals to the TC.
    6. PN - So would we welcome a cloud based pilot?
    7. JT - Part of the WIS 2.0 strategy is to look at cloud and external ID management services; so it would be useful.
    8. JT - But, if we look at the email from RGr, he makes the point that the pilots should focus on something to present at TECO in March and demonstrate some benefit to Users, rather than just infrastructure concepts. Infrastructure and User outputs are two facets of the pilots.
    9. PN - It doesn't take long to spin up a cloud based demo showing discovery, atom feed and access to data, half a day rather than 60 days. I just wonder why the current list of proposals don't include that.
    10. PR - The proposals are agnostic, you could use cloud.
    11. PN - Ok, I want to present a cloud pilot and am already speaking to people in UKMO about some of the patterns we have developed here.
    12. PR - That's fine, it's in the email from RGr, he says: 'the technical framework is not imposed'.
    13. SO - How would we decide on the relative priority of the proposals?
    14. PR - I think we ask who wants to work on which pilots; if no-one wants to work on a pilot then selecting it is academic.
    15. DW - Yes, we could poll that question and it probably won't be hard to decide which ones will get done.
    16. SO - Ok, so we'll need to do similar things to those I suggested for OpenWIS v5.
        1. Have a Charter: I'm about done with the Charter for OpenWIS; I've narrowed the scope and will probably share tomorrow - so then I hope to get some feedback.
        2. Team composition: I like the concept of squads we were discussing when we talked about the OpenWIS v5 work before.
        3. So shall we look at the [proposals](https://github.com/OpenWIS/openwis-documentation/issues?q=is%3Aissue+is%3Aopen+label%3A%22OpenWIS+Pilot+Proposal%22) we have?
    17. JT - I think there is a topic missing from the proposals: how you might publish metadata about stuff we're exposing through WIS 2.0
    18. PR - Is this the [Open Weather](https://github.com/OpenWIS/openwis-documentation/issues/188) Charter?
    19. JT - No, here I'm talking about things like how commercial search engines will find our data.
    20. PR - If I recall correctly, we discussed that at a scrum meeting in relation to one of the current proposals; I think it was the Dashboard.
    21. JT - I'm not seeing it explicit in any of them. It would, for example, mean an end to ISO 19115 metadata and synchronisation of catalogs. Instead we might publish web pages with structured markup.
    22. PR - Ok, add a proposal to our list on GitHub.
    23. SO - Should we revisit the metadata profile as part of that?
    24. JT - Yes, we'd need to change that. Some people are moving to simple web page catalogs rather than complex XML. Look at the skills available to maintain complex catalogs, they are rare.
    25. PR - I think we should get on and _do_ at least one pilot; we have been talking and not-doing for a long time, since March.
    26. SO - What does anybody else think?
    27. LM - I agree with the approach PR mentioned earlier; let's ask who will do the work on which pilots, it's the most practical.
    28. DW - We could just give the [Security pilot](https://github.com/OpenWIS/openwis-documentation/issues/300) to European Dynamics; we all agree the modularity is a key aspect.
    29. LM - Yes, if we're putting together tutorials on OSGi, then that would be a good one to experiment with.
    30. PR - To come back to the points RGr made: if we did that one, what would we actually demonstrate at the TECO meeting?
    31. SO - This would be the first demonstration of the modular approach.
    32. PR - Who is the TECO audience?
    33. JT - It will be a combination of management and technical people who are responsible for the implementation of WIS. So the intent should be to explain the benefits of the approach and why they should invest in it. There will be some people there who will understand the technology, but not all.
    34. WQ - It's very difficult to cover both ends in one demonstration, especially by March next year. We can focus on what we really need to do and look at what we have that we can demonstrate a couple of weeks before the meeting. LM suggested [OPP-2](https://github.com/OpenWIS/openwis-documentation/issues/300) and I would be happy with that.
    35. SO - I think what grabs my attention with OPP-2 is that it provides the base level groundwork for other things in the OpenWIS stack, for example, LDAP, User Groupings, making products available. Also, [OPP-5](https://github.com/OpenWIS/openwis-documentation/issues/303), the Dashboard, could use the outcome to provide LDAP credentials. So for me OPP-2 is the groundwork.
    36. WQ - I agree, but the question is: what will we demonstrate in March.
    37. SO - Right, this is a nuts and bolts thing, not a demonstration.
    38. DW - For a show and tell, the [Dashboard](https://github.com/OpenWIS/openwis-documentation/issues/303) is the one to go for.
    39. PN - I could do the [OPP-2](https://github.com/OpenWIS/openwis-documentation/issues/300) demonstration on SAAS in half a day, so we would want to build something on top of that.
    40. PR - I thought the modularity concept would be best shown by the [widget](https://github.com/OpenWIS/openwis-documentation/issues/303) demonstration. I recall discussing the use of search widgets, for example, as well as System Administration tools.
    41. WQ - For this PoC it is the modularity we want to show rather than the Security.
    42. JT - I can imagine RGr saying this would be difficult to sell to the User community and why would they be interested in it?
    43. JT - WIS 2.0 is about making it easier to publish data and discover it using public search engines, then processing the data in situ, rather than having to download it. The pilot should enable the Users to do something.
    44. WQ - That is not a technical issue. Lots of problems can be solved with different processes; but that is not for us to solve. How many people complain about WMO headers? We could get rid of them and make them happy, but that is not a technical problem. What we can do is the technical work that enables us to get rid of the WMO headers later.
    45. JT - When you put together these pilots, were you thinking of GISCs or NCs?
    46. DW - They were really based on discussions with European Dynamics about current issues and needs, but adding modularity and simplifying things; using COTS components.
    47. JT - The reason I asked is: when I look at WIS 2.0, I am hoping as much of the GISC infrastructure as possible will be COTS, instead of building our own. The costs of operating GISCs are largely caused by synchronisation of the global cache. So, can we make those disappear? How can we make data accessible to a small NMS in a developing state, without a GTS, but also provide efficient infrastructure for a large centre like Washington?
    48. WQ - You say the burden comes from the infrastructure, but hardly anything is built from scratch anymore, even if you are a central broker: you put many things together to do what you want to do. We have to have OpenWIS v5 to provide some functions and an underlying system to support that.
    49. WQ - I would like to see how we make modularity work and make things more flexible.
    50. SO - We may not have the technical skills to develop the infrastructure ourselves. We want to support interoperability via a standard set of web services, to support all of the above.
    51. JT - Yes, it has to work for big and small centres, but small centres are technically constrained.
    52. PN - Are they constrained to internet or private networks?
    53. JT - They are constrained to the internet. Djibouti for example, has no fixed or mobile networks, so they rely on satellite. Imagine DW's counterpart in Djibouti: he doesn't understand WMO metadata but has been asked to share some files, what is the minimum he can do?
    54. WQ - Right now they send by email to us.
    55. JT - Ok, let me outline some rough ideas I have about WIS 2.0:
        1. JT - Say WIS 2.0 will have a set of standards you can layer on top of each other: TCP/IP, HTTP, URL.
        2. JT - Then, if you're publishing data, you could just publish some web pages that are human-readable.
        3. PN - And the actual data could be in an S3 bucket on AWS.
        4. JT - OK, but how would you discover that data? You can use the S3 bucket to hold the base data and combine with a human-readable web page to provide the catalog.
        5. WQ - Isn't that how OpenWIS works?
        6. JT - Yes, but it is complex.
        7. PN - S3 bucket with Elastic Search on top; you could get notified of new data that comes in.
        8. JT - That's jumping to Elastic Search as the solution and inferring that you're indexing by crawling the files.
        9. WQ - An expert can find the model data without metadata; no need for the web page.
        10. DW - Is that just because the metadata is already in the filename?
        11. PN - That's all we're currently doing with our S3 NetCDF files, storing files with WMO headers.
        12. JT - We're getting rid of WMO headers; when the data is visible on the internet you won't need local addresses on private networks.
        13. PN - We'll still need some metadata.
        14. JT - I agree. We've talked about commercial search engines; you want them to crawl web pages to find some structured markup. It is metadata, but not as we employ it currently, which is painful!
        15. PN - That metadata is not our responsibility.
        16. PR - How does the metadata get into the human-readable web pages?
        17. JT - These pages use [schema.org](http://schema.org/) and the metadata is usually implemented as [JSON-LD](https://json-ld.org/) inside the pages. Simplest way to generate web pages, if the service endpoint is static, is write web pages with tags, or generate by parsing. The [ESIP](http://www.esipfed.org/) convention tells you what you should include in NetCDF so you can populate web pages. On Copernicus, ECMWF is managing the metadata in GeoNetwork, then taking it and publishing a web page, not publishing the metadata catalog itself.
        18. SO - What is exposed? How easy do you make it for the end-user?
        19. JT - You only put in what makes it easy to distinguish between the types of data available. If we rely on commercial search engines, they will use sitemaps and crawlers, old technology. One of the things we need to be able to do is retain an authoritative view of what data is published by WIS centres. We would need a simple register to create a list of what data is available. Jumping to solutions again, but maybe we could use Elastic Search to do that.
        20. PR - We are short of time to get a demo ready, and since it's only a pilot, we _should_ jump to some solutions.
        21. JT - So we would need to create a list of data available from the WIS centres. We could test how centres would make their data available: for example - _my site map is here, come harvest my data_.
        22. PR - This sounds as if it would make a good proposal for the demo - OPP-JT.
        23. DW - Could we include subscriptions?
        24. JT - Interesting point: so we might have HTTP URLs, maybe through S3 buckets; so now we have to put files on a queue to be subscribed to, even if it is a simple file or a web service.
        25. SO - It is something tangible; pub-sub is an extension to this.
        26. JT - Yes, we could layer the pub-sub on top.
        27. SO - A hybrid of OPP-2 and OPP-JT.
        28. WQ - I can't see a link between that PoC and OpenWIS v5.
        29. JT - What does OpenWIS become if we strip out the infrastructure?
        30. PR - Cheaper.
        31. JT - Yes, cheaper, easier, etc.
        32. JT - So we do some components that do pub-sub and some that form the metadata. Sounds like I need to write something down.
        33. PR - I could draft OPP-JT from the notes I've taken and you can edit it:
            - [Action-TC-2017-22 Add pilot proposal OPP-JT](https://github.com/OpenWIS/openwis-documentation/issues/304)
        34. JT - Make sure we're clear on the purpose: to publish data as static files.
        35. PR - So refer to the Djibouti User Story?
        36. JT - Yes, a User Story not framed in WIS 1.0, GISCs, global hubs etc.
        37. SO - We could modify the OPP template to bring in how the proposal ties into something we can demonstrate and also relate to Users.
        38. PR - Ok, so a section of the proposal could describe the high level User Story.
3. **Developer Conference**
    1. LM/WQ - We have agreed to host the Developer Conference.
    2. DW - Did anyone fill in the poll?
    3. LM - Just DW and myself so far.
    4. PR - I'm not clear what the objectives are for the Developer Conference this time. It should be hard-core development of pilots, so I probably don't need to be there in person.
    5. JT - So a hackathon.
    6. PR - Yes, not just a meeting we could do by WebEx.
    7. JT - Yes and we also need to consider the cost.
    8. PR - I think September is too close; I don't think we'll have developed the pilot ideas sufficiently.
    9. JT - Early next calendar year then?
    10. PR - Yes, the Annual Meeting isn't until April.
    11. SO - Ok, let's push out the Developer Conference to early next year.
4. **Date of next meeting**
    1. SO - We'll need to get together again once MF are back, so another TC last week in August ok?
    2. PR - Yes, I'll be around then but not the first 2 weeks of September.
    3. SO - Ok, we'll go for last week of August.


---

#### Participants
- SO - Steve Olson, National Weather Service, USA [NWS], Chair
- LM - Leon Mika, Bureau of Meteorology, Australia [BoM], Vice-Chair
- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM]
- DW - Dominic Woollatt, Met Office, UK [UKMO]
- PN - Paul Nelson, Met Office, UK [UKMO]
- PR - Paul Rogers, Met Office, UK [UKMO]
- MG - Marc Giannoni, National Weather Service, USA [NWS]
- JT - Jeremy Tandy, Met Office, UK [UKMO]

#### Apologies

- MC - Michael Claudon, Meteo-France, France [MF]
- BS - Benjamin Saclier, Meteo-France, France [MF]
- RGb - Remy Gibault, Meteo-France International [MFI]
- SD - Sungsoo Do, Korea Meteorological Administration, Republic of Korea [KMA], [delegate]
- MP - Mikko Partio, Finnish Meteorological Institute, Finland [FMI], [delegate]
- CS - Cassie Stearns, National Weather Service, USA [NWS]
- DJ - Duncan Jeffery, Met Office, UK [UKMO]
- NM - Nassos Michas, European Dynamics, [UKMO]
- GT - Giorgios Triantafyllidis, European Dynamics, [UKMO]
- DP - Dimitris Papadeas, European Dynamics, [UKMO]
