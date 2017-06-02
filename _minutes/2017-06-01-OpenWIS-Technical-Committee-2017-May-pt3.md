---
layout: page
title: OpenWIS Technical Committee 2017 May - part 3
---

#### 1st June 2017, WebEx - meeting minutes

---

1. **Option 1 versus Option 4 - cost-benefit analysis**
    1. The related action on GitHub is: [Action-SC-2017-23](https://github.com/OpenWIS/openwis-documentation/issues/194)
    2. PR - So we're continuing with agenda item 1. Would GT please tell us where we're at with consolidating the feedback on the requirements spreadsheet.
    3. GT - Ok:
        1. MF have provided their information.
        2. MF have also added some extra requirements, which are at the bottom.
        3. I have added extra columns to the right that show the Version proposed by each organisation.
        4. Also, there is a tab showing the architecture comments from MG.
        5. I have added a function that shows the degree of agreement about Versions.
        6. You can also see information about the Priority, but they are mostly 'medium'.
        7. At the bottom of the sheet I have added a calculation that sums the differences in Version.
        8. So currently, it shows that 137 are not agreed, roughly half of them.
    4. LM - So we had a look at the extra requirements from MF at the scrum earlier in the week and I then emailed MF requesting clarification on some of them.
    5. BS - We have the email here, we can go through them now:
        1. **Usage of Content Management System for web portal**:
            - What kind of capabilities do you have in mind for this CMS?
                - Is it just changing the styling of pages (i.e. changing colour scheme or organisation logo), or
                - Is it changing the content of existing pages (using OpenWIS 3 as an example: the home screen, about screen and help screen), or
                - Is it also adding and removing pages and adjusting the site map (so from the home screen, you go to a help screen which will have seven custom pages, for example), or
                - Something else?
            - Did you have in mind how you wanted these pages changed?
                - Did you want something similar to how things are done now (e.g. edit text files using an editor), or,
                - Did you have in mind something like a web-based page designer like many of the other CMSes out there?
            - I assume also that this CMS feature will only be allowed for certain users, correct?
        2. BS - The goal is to be able to do any change on the web portal. We want to be able to tune the web pages. We want to use something like Joomla or Drupal. We want to add plug-ins, for, say, the harness.
        3. PR - Ok, but using a CMS is a solution; what is the requirement?
        4. BS - Ok, then we want to change the look and feel of the web portal, but without having to use a developer.
        5. **A metadata may belong to several sets**
            - When you say "set", do you mean something like categories (such as WIS-GISC-TOULOUSE, etc).
            - ​If so, did you have in mind support for things like the WIS-CATALOG set that are available on some of the GISCS?  Are these sets to be published as OAI-PMH sets?
        6. BS - We had a problem with the WIS catalog because, in OpenWIS, one metadata can only belong to one category; it would be better if it could be in many categories.
        7. **A user/group is linked to a "category" of metadata and can only add/modify/delete MD linked to this category:**
            - My understanding of this is:
                - The rights that a user or a group of users have for modifying metadata can be restricted to just the set of metadata that lives in one or more categories.
                - The user will only be permitted to create or upload metadata to the categories they have permission to modify
                - The user will only be permitted to edit metadata of the categories they have permission to modify
                - The user will only be permitted to remove metadata from the categories they have permission to modify
            - Is this more-or-less right?
        8. BS - At present you can add metadata to any category, not just your own. We need to link each User to specific categories.
        9. **Possibility to select a group of metadata for actions such as Remove, Change category, Change owner**
            - Is this, what we've called, "Bulk Metadata" operations?  That is, instead of picking and choosing individual metadata records to do something to, the user will:
                - Specify some search criteria
                - Specify some operation
                - Click "Do" and when that happens, the system will perform the operation on all the metadata that matches the search operation.
                - The user does not need to be involved after clicking "Do"
        10. BS - Yes, that kind of thing.
        11. **Improve the user management (search by email, company …), extract group of users.**
            - Does this just cover additional search fields for users within the users and groups screen?  I.e. the ability to search for users based on email, organisation, profile?
        12. BS - We made some changes to our DCPC and we wanted to contact all our DCPC Users, but it is not possible to extract the list of their email addresses.
        13. **​Add information about last activities (last time the user connected to the portal, modify metadata, …) of a user**
            - Would this be covered by REQ098 (i.e. a sear​chable audit log?)
        14. **In case we maintain subscription functionality, monitor and administrate subscription by product and/or user**
            - I assume this means that when the administrator is managing subscriptions with the admin portal, they have the option to search using either the subscribers user account (i.e. the user) or to what they subscribed to (i.e. the metadata URN).  Correct?
        15. BS - The problem we have at the moment is that we can't tell who subscribes to a specific product.
        16. **Each component shall provide API (RESTFULL ?)**
            - Could this be covered by REQ137, REQ139 and REQ220?  (see comments about API)
        17. BS - It would be very useful if all the components of OpenWIS were exposed as services through an API, like they are in GeoNetwork v3, so that we can call them from outside.
        18. **Openwis shall provide a specification of API available (swagger documentation format )**
            - ​Could this be covered by REQ137, REQ139 and REQ220?  (see comments about API)
        19. **3 seconds initial service response time (including getting metadata) / 20 parallel services request by second**
            - Does the "3 seconds initial service response time" relate to users using the portal?
            - Would this be covered by REQ003 to REQ008?
        20. BS - I will need to check the specifics for this one.
        21. **Enable text copy in GUI pages.**
           - Is this for alerts and other dialogs used within the UI?  This to me seems to be related to the widget toolkit used to build the UI.
        22. BS - We would like to be able to copy text from anywhere in the GUI; all you can do right now is take a screenshot.
        23. LM - Do you mean the lists on the Admin screens?
        24. BS - Not only there; also wherever there is User information.
        25. **Have the option to keep the metadata when deleting an harvesting task.**
            - My understanding of this requirement:
                - When the user clicks to "Delete" a harvesting task that has metadata associated with it, the user is asked whether the metadata for that harvesting task should be deleted as well, giving them the option to delete it with the harvesting task or keeping the metadata and simply disassociating that metadata with the harvesting task.
        26. BS - Yes, we need the option to keep the metadata when deleting the harvesting task.
        27. **Possibility to connect the Openwis to external LDAP user and admin server for authentication. Note that the servers may be different for admin and users**
            - Is this similar to/covered by REQ224?
        28. BS - I will need to remind myself of the specifics for this LDAP issue.
        29. LM - Is this about SAML2 authentication?
        30. BS - Is that how we can use an external catalog for authentication? At MF we have already an external repository for SSO.
        31. LM - Yes, that's covered by the SAML2 requirement.
        32. [_The original table of Versions suggested by LM for each new MF requirement is at the foot of these minutes_]
        33. BS - When we discussed the versions at MF we took Version 1 to mean high priority. So, for example, the CMS would be a great improvement, to satisfy the needs of our external customers.
        34. LM - So your Version 1 is a _must-have_?
        35. BS - Yes.
        36. LM - So the way the rest of us were doing it is that Version 1 would be the MVP. The Version 3 would be the full production ready product and would have all the Version 1, 2 and 3 requirements included.
        37. BS - So Version 1 is already here; it is OpenWISv3, which is compliant with WIS 1.0.
        38. PR - We mean a Version 1 based on the new modular, API based design, that would allow you to do some of the things you have requested, such as call OpenWIS functions as services through an API, or flexibly swap components to suit your different customers.
        39. NM - In the new architecture, all the services would be exposed through an API by default, so we would always access the services that way.
        40. PR - And the modularity would make it easier to build different DCPCs, for example.
        41. LM - So it should be easy to customize.
        42. MC - I don't understand this.
        43. LM - Say you want to provide services that differ from the vanilla OpenWIS, it should be a lot easier to deploy your own flavour to suit a specific customer.
    6. SO - I would like to discuss the biggest discrepancies between the Version numbers.
        1. NM - Ok, yes, what shall we do a bout resolving them?
        2. GT - You would need to go through about 130 requirements; do we have the time to do that now?
        3. LM - We could focus on the requirements that we all agreed were Version 1, since that could be the basis of a proposal to the SC.
        4. GT - Ok, but there are many that not yet estimated or included in the total effort calculation. But as it is, the sum of the development days comes to 444.
        5. NM - We need to add in the new MF requirements.
        6. GT - And also the GEOSS requirements.
        7. LM - I propose that one of the options for SC to consider is this Version 1 sum, plus a large dollop of contingency.
    7. PR - Ok, so let's just remind ourselves what the SC wanted; according to the action recorded, they asked for a cost/benefit comparison of Option 1 versus Option 4.
        1. BS - We are currently focused on Option 4.
        2. PR - Yes, although Option 4 is almost a superset and we think we can derive an Option 1 cost from that if we define it carefully. As WQ pointed out in Toulouse, the cost of developing WIS 2.0 will come to about the same in the end, however we get there. Option 4 is the more aggressive, with higher burn rate and higher risk. On the other hand, Option 1 includes the extra cost of further development of OpenWISv3.
        3. LM - So we either put significant effort into OpenWISv3, like we were with OpenWISv4, as well as OpenWISv5, or we just do OpenWISv5 and put all our effort into that.
        4. BS - But we can put OpenWISv3 into maintenance mode.
        5. PR - Option 1, as currently defined, includes further development of OpenWISv3. {You can see the definitions of Option 1 and 4 that were agreed at the Toulouse meeting [here](https://github.com/OpenWIS/openwis-documentation/issues/194)}
        6. BS - Ok, but I think we can put OpenWISv3 into maintenance mode and not do development.
        7. PR - Ok, so you are proposing a new Option, let's call it Option 1.5.
        8. LM - I'm not sure how viable that is. OpenWISv3 is compliant, but it is missing usability features; I'm not sure we can wait around for WIS 2.0 before we see any significant improvements.
        9. PR - To summarize Option 1.5:
            - Put OpenWISv3 into maintenance mode
            - Stop work on version 4
            - Develop WIS2 pilots in « new architecture » and evolve pilots to meet WIS2 Tech-Specs
        10. BS - Option 4 could be up to 10 man years of effort to create something that is not WIS 2.0 compliant, because we don't know what that is yet; that's too expensive.
        11. BS - With Option 1.5 we are working on the WIS 2.0 to-be and just maintaining OpenWISv3.
        12. SO - It's a difficult choice. The focus has been on Option 4 so far.
        13. PR - Ok, NM, could we derive an estimate for Option 1.5 from the work we have done on Option 4?
        14. NM - Yes.
        15. LM - What set of requirements would be a good overlap between WIS 1.0 and WIS 2.0?
        16. SO - If we went with Option 1.5, would Version 1 of Option 4 be the initial baseline of Option 1.5?
        17. NM - We said Option 1 will eventually cost the same as Option 4, but to ensure it is not more expensive, we have to be careful to develop incrementally and not have multiple parallel pilots heading off in different directions.
        18. NM - On the plus side, Option 1.5 has less risk in terms of everyone becoming familiar with the platform.
        19. NM - I think it is better not to think of Version 1 as implementing an initial set of requirements, although of course it will to some extent do that, it is really about choosing a few architectural concepts that we want to explore and demonstrate.
        20. PR - So are we saying that we are not aiming to develop a baseline version that is fully WIS 1.0 compliant?
        21. BS - Yes.
        22. SO - Would we be pulling these new features into OpenWISv3?
        23. PR - No, OpenWISv3 would be maintenance only.
        24. SO - So we'd be tied to OpenWISv3 for a while?
        25. BS - Yes. We'd try to push the WIS 2.0 specification in our direction. We want to think again about how harvesting and subscriptions could work; try different ways eg: similar to the way Twitter works. It's time to start pilots with new protocols and push WMO to adopt these.
        26. PR - I think it's worth adding at this point that the numbers we're getting from the analysis of Option 4 suggest to me that there is no way we could deliver Option 4 in 1 year.
        27. SO - If 2025 is the date for a full version of the WIS 2.0 specification, then that gives us a long time to bring influence to bear, but I'd hate to delay the OpenWIS refresh that long. If we could replicate the core functions, it gives us the opportunity to use it at some point and then evolve to WIS 2.0.
        28. PR - Option 1.5 would allow us to evolve OpenWIS at whatever speed development of WIS 2.0 concepts allows.
        29. LM - Option 1.5 is the best choice in terms of least risk, given where we are with WIS 2.0 and OpenWISv3. There's a risk we might have to do some rework on OpenWISv3, but I'm leaning towards Option 1.5 myself.
        30. SO - How to describe the initial version of Option 1.5?
        31. PR - Can we pick some Use Cases?
        32. NM - How about we start with some architectural concepts? Then we can choose which Use Cases fit those later.
        33. LM - Yes, that sounds good; a suitable architecture we can learn from and adopt for WIS 2.0; Explore the customizability etc.
        34. NM - Such concepts as: an extensible dissemination harness that works via an API, or how we can have data and metadata in a central location. These are just examples. Higher level concepts would be demonstrated through those practical applications.
        35. LM - We should choose some of these concepts.
        36. NM - We will have to create the underlying concepts to realise the Use Cases.
        37. LM - Would be good if the concepts were grounded in Use Cases for things like searching.
        38. GT - These requirements need refining, for example, which are for the new WIS?
        39. NM - So it's now a matter of choosing the focus of the Option 1.5 baseline/version 1.
        40. BS - Yes, we could work together to add the new ideas. A blank page for the concepts. So the new concepts could be functionality or technologies. We should provide the comparison of the Options 4 and 1.5 to the SC. But, is the SC too soon?
        41. PR - SO, shall I ask JT for a postponement of the SC? He is here today.
        42. SO - Yes please.
        43. PR - If JT approves we can use the SC slot next week for another TC
            - PR - [Action-TC-2017-27 Postpone SC and schedule June TC in its place](https://github.com/OpenWIS/openwis-documentation/issues/275)
        44. SO - Is there a way to go through the requirements and say how the concepts map across?
        45. NM - Yes, we could do that.
        46. SO - Ok, thanks, I think that will be needed to help the SC give direction.
        47. PR - So, NM, will you be able to provide some guidance to everyone on what concepts information you would like and how?
        48. NM - Yes, ok
            - NM - [Action-TC-2017-25 Provide guidance on 'Concepts'](https://github.com/OpenWIS/openwis-documentation/issues/273)
        49. PR - So GT, if you could amend the spreadsheet to include a tab for the concepts and circulate that, then everyone provide the feedback to GT via the spreadsheet, before the TC next week if possible
            - ALL - [Action-TC-2017-26 Collate feedback on Concepts and map to requirements](https://github.com/OpenWIS/openwis-documentation/issues/274)


---

#### Leon's email suggestions of Versions for new MF requirements

Feature|Version​​
---|---
​Usage of Content Management System for web portal|3
​A metadata may belong to several sets|1
​A user/group is linked to a "category" of metadata and can only add/modify/delete MD linked to this category|1
​Possibility to select a group of metadata for actions such as : Remove, Change category,Change owner|3 (assuming "bulk metadata" actions).
​Improve the user management (search by email, company …), extract group of users|3
​Add information about last activities (last time the user connected to the portal, modify metadata, …) of a user|3 (although data design and action recording stuff would probably be covered from version 1).
​In case we maintain subscription functionality, monitor and administrate subscription by product and/or user|2
​Each component shall provide API (RESTFULL ?)|3 (this is the delivery of the finished API)​
​Openwis shall provide a specification of API available (swagger documentation format )|3 (this is​ the delivery of the finished API documentation)
​3 seconds initial service response time (including getting metadata) / 20 parallel services request by second|1
​Enable text copy in GUI pages.|1 (to be covered in the choice of UI widget framework)
​Have the option to keep the metadata when deleting an harvesting task|1
​Possibility to connect the Openwis to external LDAP user and admin server for authentication. Note that the servers may be different for admin and users|2​

---

#### Participants
- SO - Steve Olson, National Weather Service, USA [NWS], Chair
- LM - Leon Mika, Bureau of Meteorology, Australia [BoM], Vice-Chair
- MC - Michael Claudon, Meteo-France, France [MF]
- BS - Benjamin Saclier, Meteo-France, France [MF]
- PR - Paul Rogers, Met Office, UK [UKMO]
- NM - Nassos Michas, European Dynamics, [UKMO]
- GT - Giorgios Triantafyllidis, European Dynamics, [UKMO]
- NM - Dimitris Papadeas, European Dynamics, [UKMO]
- KS - Kari Sheets, National Weather Service, USA [NWS]

#### Apologies
- MG - Marc Giannoni, National Weather Service, USA [NWS]
- DJ - Duncan Jeffery, Met Office, UK [UKMO]
- PN - Paul Nelson, Met Office, UK [UKMO]
- YG - Yves Goupil, Meteo-France, France [MF]
- DW - Dominic Woollatt, Met Office, UK [UKMO]
- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM]
- RGb - Remy Gibault, Meteo-France International [MFI]
- SD - Sungsoo Do, Korea Meteorological Administration, Republic of Korea [KMA]
- MP - Mikko Partio, Finnish Meteorological Institute, Finland [FMI]
- CS - Cassie Stearns, National Weather Service, USA [NWS]
