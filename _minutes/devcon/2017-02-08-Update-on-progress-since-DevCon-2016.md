---
layout:  page
title: Progress since - 2016 OpenWIS DevCon Workshop Final Report
minuteOwner: devcon
---

Progress comments, by Paul Rogers, are inline and preceded by this heading:

### Update Feb 2017:

---


**Report on the 2016 OpenWIS Developer Conference**

**Day 1; Sept 27th, 2016**

**Day 1 Morning Session**

9am: Introductions around the table and on the phone.

Participants in person:  Steve Olson, Bob Bunge, Marc Giannoni, Remy Giruad, Michael Claudon, Paul Rogers, Dimitris Papadeas, Dom Woollatt, Leon Mika, Lee okki,

Participants remote:  Martin G.

**Review of Goals**

Steve reviews goals worked up from the results of the meeting at KMA.  Shows list on screen, asks for other goals.

Remy: Suppose to be a month away from OW 4.x.  Any recommendations to the EC?  Paul thinks it is covered under other parts of the list as presented by Steve.
Dominic: Need to conduct final testing of 3.14 and then put it into support mode.
Okki: 3.14 needs to be solid so it can be more operational.  Should be easy to deploy into the operational environment.
Paul points out they have gotten 3.14 install down to three hours instead of five days; mostly because of the use of Puppet.

### Update Feb 2017:
- v3.14 packages for both development (vagrant) and operations (full-stack) have been released.  The latest operational release is v3.14.8



**Revised Goals:**

Close out remaining 3.14 work and conduct final testing.  Move towards support mode for OpenWIS 3.
Finalize remaining steps for automating, streamlined OpenWIS deployment and installation.  Applies to both OpenWIS 3 and 4.
Adopt a more flexible, agile development methodology that supports development from wide range of developers.  Make onboarding of new developers easier.
Finalize developer community Wiki Documentation
Outline steps and provide roadmap towards being open source
Complete migration to Maven 3 with Eclipse support
Complete initial phase of Geonetwork 3 work (Strategic hackathon session(s))
Define requirements for web page CSS work and sketch out rough design

### Update Feb 2017:
- v3.14 and v4.0 are now open source and available from GitHub, including the wiki/documentation updates for developers and potential collaborators.
- This was announced at CBS in Nov 2016.
- A proposal for improvements to the development methodology has been published, for discussion at the Toulouse meeting.
- Conversion to maven 3 is complete.
- The initial phase of GeoNetwork 3 work is complete.  Two demo instances are available, one being pure Core GeoNetwork 3.2, the other being OpenWIS v4.0, which is built from a combination of GeoNetwork 3, some changes to GeoNetwork 3 we had done by GeoCat, and the OpenWIS v3.14 Data-Services.  This is a development prototype that we will use to establish what further work is needed to complete OpenWIS v4.


Steve reviews the agenda and outlines the talks that have been provided.



Opening Presentation: OpenWIS 101 (Leon)
Nice review of the architecture and components of OW.  Good explanation of the very complex nature of the login auth piece using OpenAM.   Review of Database and Solr.  No questions.

OpenWIS Architecture Presentation


Second Presentation:  Review of data management services (Leon)
Discussion over the boundaries of the data services; as this applies to both operational installation and for security purposes.  Review of the portal environment.  Note there are two portals running in the system (user/admin).  Steve asks about use of SOAP and what what WSDLs are uses in the system.  Review of code organisation.  Good review of the code by directories.  List in slide.  Note:  Since the OpenWIS implementation of SOLR plugin is a bastardized version, should it be reworked?

Introduction to possible architecture of OW 4.x.  Presented some ideas for OW 4, including the use of Spring and Angular.  Outstanding architecture tasks are reviewed, including separating out GeoNetwork with no specific OW code in geonetworks.

### Update Feb 2017:
- The OpenWIS v4.0 demo has the Spring/Angular overlay/plug-in design that allows GeoNetwork and OpenWIS code to be kept separate.  Eurodyn are currently producing the developer docs on how this works and should be used.


Development tasks.  Outlines a series of steps as listed on the slide.  List of tools needed.  KMA pointed out issues with Vagrant versions and its interaction with VirtualBox.  We need to be specific versions used.  Concern if versions in documentation, is they become very stale quickly.  Brief discussion about the use of puppet.

Step two.  Pick your repository.  Description of six repositories on GitHub.  Review of fork and clone processes.  Discussion about merging of forks between members and notifications when code is contributed and the resulting workflow.  Agreement the workflow should be defined.

Step 3: Chose a task to work on.  Kanban board is used to list out the tasks that need to be done.  Select a task, if the task is currently un-owned.  Review of tasks needed to start to work on the task.

Step 4: Code Style, indention (3 spaces and no tabs).  Code comments, strings in UI.

Step 5: testing your changes locally.  A question if some of the tests will be demonstrated.

Step 7: Review and integration.  Comments will be made in the pull request.  Describes the build process and where the artifacts are located.

What a great, detailed review. Ling asks if he could create a video of the build process to include setting up the dev environment.  Ling also asks about doing all this work on Windows.  Leon states it should all work except for the testing which needs to be fixed.  KMA points out in Windows, you need a 64bit environment.  8GB of RAM is recommended.

OpenWIS Development Process Presentation

Day 1 Lunch Break

Day 1 Afternoon Session

Intro by Steve on what’s required in a move to open source; This includes but is not limited too:
Governance
collaboration development environment
Use of gitHub code source repository
Detailed development policies
Developer documentation
Project and association  websites
Access to user forum
Supporting tools needed (e.g. Dashboard for monitoring progress, etc).
This was followed by a whiteboard session and suggestions to move OW more towards open source.

Paul: release that we will make OS; need some rules; make announcements;
Paul: Technical Rules .. Needs work still
Dom: Repository issues. Sorted out.
Leon: how will we do documentation?
We should contribute back to Geonetwork?  Plugin?
Open up mailing lists to those who want to contribute.
An approach towards management the community we hope to form.

Steve asks about charter, Paul points to Association website (on github) that includes a charter and license information.  Discussion around the Contributor License Agreement; getting legal review and agreement from the member states for the association.  A discussion over the CLA and parts of the CLA and what is covered under sections as questions are asked.  After internal review and comment, each Met Office should have its legal team review.

Target is to make a public announcement at CBS.  Fred agrees.

KMA asks what version to release?  Paul says in Seoul, the decision was OW 4 since it is in development and has new contributors working on the new version, not the operations, now closed 3.x code.  KMA makes a motion to have 3.14 be the initial open source version released.  After some lengthy discussion, the workshop recommended to the OpenWIS TC, that OpenWIS 3.14 be the initial open source version.

Leon also recommended that we buckle down and make it easier for contributors to get the data and follow instructions to make it work, but not to make it perfect.

Steve asks about security issues; Fred points out that any security issued raised by a contributor is already an issue for a member.  Fred also points out that the desire is not to accept a liability on behalf of a contributor.

-------------------------------------------

As written on the board by Steve, and recommended by the workshop, the following open source areas need work before they are “ready for primetime”.:

OpenWIS Association Level and OpenWIS Project Level Webpages (Action Item: NWS to take the lead to designing these webpages)
Release and CLA firmed up (Action Item:  Paul has the lead to complete the CLA agreement and distribute for comment).  After internal review and comment period, have each full sponsor’s legal team review (Action Item:  Legal Review by each full sponsor Met Office)
Technical Rules: (Action Item:  Leon will take the lead)
Public Announcement (target CBS; source version).  (Action Item:  Remy will take the lead in creating a poster for CBS meeting)
Repository aspects (packaging, sourcing):  (Action Item:  Review by workshop team at a later date.  Have Paul schedule meeting)
How to do documentation
Open Mailing list.  Probably need to have one administrators of this list.  (Action item:  Remy to review and provide feedback)
Management approach (contributors, forum)
Code of conduct
Governance - rules and responsibilities

### Update Feb 2017:
- The new website has been built as agreed at the DevCon.  
- We are now working towards replacing the Forum so that we can switch-off the old website.
- The Technical Rules, CLA form and CLA process were published for the open source release.  Suggested improvements are topics on the Toulouse agenda.


---------------------------------------

Paul brings up the “posts” section of the website and points out closed and open actions from Seoul.  Some of these posts are around ease of use of the website.   Paul talks about Kanban and the github forum tools to keep the conversations between developers in context with the project and the code.

Steve and Paul point out the Kanban board is a list of issues the association is currently working, where we are going and suggests where a contributor can help out.  Dom and Leon explain kanban and the linkages to it  as part of a discussion about the structure of the website.

Need landing page for website.  Landing page to list GISC centers.  Retain much of the header of the current web pages.  The footer also has good information.    “Get OpenWIS” and “Fork Open WIS”.  Also list of members.  Also how to download the code.  What does a possible contributor want to know if they land on the page;

Home page:

Welcome
Get Code
Fork Code
GISC listing
Association members
Links to each of the member GISC centers;
Short statement of what OpenWIS is.   Intro to OpenWIS;
Contribute; link to GitHub, repository, etc.  -> get involved
Link to WMO at some point
Link to Github
Link to documentation page that links to each of the pieces of documentation
Use header of page wtih addition to home link
Steve envisions a series of drop downs for the header since the list is starting to get long;
Dom raises a quest for a “news” link with recent activities, including links to downloading stable and nightly builds.

Apache software page used as an example.

Fred suggests the header pull downs should be based on the type of users, not topics.

Home
Association (description and more info)
Community (External Contributors and more)
End users (like a DCPC who is using OW)
Documentation (implementation)
Download

Geonetworks website is also used as a good example since Geonetworks contributors may end up be OpenWIS contributors.

Fred pep talk, stresses making it easy to install and use, to push out to the developing world in order to bring in a wider community with more than just the big players.

Day 1 Afternoon Break

Remy presents some slides “OpenWIS Association, Stronger Together”

Background/History
List of members/logos
What it is
Delivery Framework for the delivery of open source software
Why an Association
OpenWIS is complementary to WMO
Roles and management structure
Description of OpenWIS software
What else?  What will we look at?
How to contribute
Stronger together for open source solutions
Joining the Association

Idea is to use the excel to ISO metadata python script as a 2nd project to clearly show how OW is more than just the one software project.

New top menu for Association-Level WebSite

Association 	Projects	Community	Documentation	Download

A long, very free wheeling discussion on the menus for the pages; and about a multi-project environment.  Slowly evolving into having two landing pages, one for the association and another for the project.

Almost 4pm, still talking menu framework for both Association and specific projects.

US to provide developer to build mock up on a NWS website.  Upon tweaking and final version, the developer will move the page over to the Github website.



Bob Bunge has a high resolution version of this image.

Review of the CLA (annex A).  Paul states that Jeremy has some strong feelings about what is in the document and took an action to manage this document enough to go for legal review.

There was general agreement with the workshop team that the rest of the internal rules are in pretty good shape.

External rules:  Paul states these aren’t rule about the association, but more about software development and governance related development.  Noted that dispute resolution is covered in the CLA.   Leon has action to manage changes to the external rules.

Code of conduct discussion:  Discussion led by Paul, but no volunteers to take a lead.  Paul agrees to research to find some examples from other open source projects.

### Update Feb 2017:
- The Code of Conduct was published on the website in time for the open source release.  


Continued review of menu options and discussion about what goes under most.  Download goes to latest stable.

Discussion around how the package is delivered:  Paul, work towards having a v4 package that is easy to download and install to run, but that isn’t where we are now.  Desire is to provide something a developer can get started with to help out with v4.  A polished version isn’t a requirement to make OW open source at this time.

Actions from Day 1:

Creation of video on the build process (Action: Leon)
Technical Rules build out (Action: Leon)
OpenWIS Association Level and OpenWIS Project Level Webpages (Action: Steve)
Complete the CLA agreement and distribute for comment (Action: Paul)
Have full sponsor’s Legal review CLA agreement and comment (Action:  Paul, Leon, Remy, Okki, Steve)
Repository aspects (packaging, sourcing) (Action: Paul to schedule a follow on meeting to discuss this)
Administration of Open Mailing list.  Probably need to have one administrators of this list (Action: Remy)
Code of Conduct.  Need samples from other open source projects (Action: Paul)

### Update Feb 2017:
- Most actions from the DevCon were completed in time for the open source release.  The outstanding actions are listed in the Action Tracker, on the website, and also at the foot of this document.  


Day 2 ; Sept 28th, 2016

Day 2 Morning Session

Participants in person:  Steve Olson, Bob Bunge, Marc Giannoni, Remy Giruad, Michael Claudon, Paul Rogers, Dimitris Papadeas, Dom Woollatt, Leon Mika, Lee Yiokki,

Participants remote:  Martin G, Ling T, Giorgos

Kick off at 8:45, brief discussion on packaging

Presentation on packaging tools (Martin G.)

Martin made a presentation about making the building of OW software easier.  Martin reviews the packaging tools and scripts used and questions why we are using each.  He also reviews the wiki.   Reviews the scripts used to make the build. KMA asks about how the automated the puppet scripts are.  Martin replies with some examples, just as changing the IP addresses.  Steve asks if OpenAM process is automated.  Martin replies there are manual steps.

Presentation on Customizing UI using Geonetworks (Dom W.)

Customizing the UI by Dom.  Home page, search and results page; Admin pages.

For v4; at least  partly driven by changes from new geonetworks.

Homepage: blue icons displayed based on content within in the metadata using tags from the MD.  Green icons also based on MD, but in a hierarchical manner.   Not real clear how these icons are populated, including the numbers displayed beside them.

Search page: Geonetwork shows categories on left bar, but one of those areas displays a number that appears be areas/GISC’s.  Need to be hacked to list the GISC instead of the harvesting number(?).  Lack of keywords or misspelled keywords in the MD start to show up as curious categories and other points in the new menuing system.   In other words, the new interface more clearly displays issues with the metadata content.

Search result for a single product; display of the metadata:  Paul points out the move to new GN, was to open up new options for the UI, but he’s more interested in making it work like v3 in the short term and save major changes for later.  Dom discusses small icons that appear in the metadata search results.  He explores how the MD trigger these icons and what they mean.  Paul also points out some of the MD and icons are a result of Inspire, the EU mandated metadata and search needs.

Reviews questions about how the metadata should be grouped and how this work would improve the searching and display of the MD:  Dom points out current MD is at the product (or “song”) level, but we should be adding MD for additional layers (Album, artist).  Discussion as to how this would work; how these metadata of metadata records would work and how they would be harvested and displayed by none OW systems.

Lee (KMA) asks about how Geonetworks indexes and stores the MD.  Dom explains GN has additional and new options in how the indexing occurs and results displayed.  Many new features.

Bunge Comment:  Nice example of how an engineering change offers new functionality that need to be conveyed to the data owners and higher level management as to how these new features can be used to improve the overall product and user experience.  Should not depend on engineers to make product and program decisions that change the user experience.  Or do we?

Lee (KMA) asks for references to architecture for OW v4 has reviewed by Leon yesterday.

Dom points out the search results interface in new GN (v4) can be changed more easier than older version.    Uses Lucine as engine.  SOLR may not be required.

Admin pages:  Discussion about the URL of the admin page between Martin and Dom and security.  Remy comments that any changes result of GNv4 (or 3?) first need to be weighed against the WIS requirements.  Other tools, including OpenAM may not be required at this time with current requirements, both WIS and Association.

More discussion about child metadata.  Can the MD be built in away that allows a user to subscribe to a custom or pre-defined small area/domain.

Dom comments new GN has a lot of features that we don’t use now and many want to use right away; but could add a lot of value in the future if we can decide how to use it.

Dom reviews features of the admin UI in the new version.  Compares with the admin UI in 3.14.  Points out the new admin UI has a content reviewer profile/role.  Might be very useful for some smaller orgs/DCPC’s.

User set up is similar.  Adding data can allow assignment of icons for different types of data.  Points out UI for setting up sync and other features, but not clear how well these features work.  Steve asks about logs.

Discussion about admin features and Dom reverse engineering what different changes mean and how they impact OW and management of the system.   Dom reviews MD tools, including creating and editing the metadata.  Leon asks about tools for moving metadata.  Some review of tools to batch metadata.

UI Presentation by Dom

### Update Feb 2017:
- The functionality of GeoNetwork 3 and relevance to OpenWIS v4 is a topic for discussion on the Toulouse agenda (Dom to lead).
- Dom will also cover the possibility of using metadata hierarchies to solve some of these issues.

Presentation on JBoss Domain (Mark G./NOAA)

Reviews his history of working with OpenWIS.  Explores how jboss can be used to streamline configuration and operations.  A review of how jboss could work and help OpenWIS.

KMA asks about if there is an issue of using the open source version of JBoss (wild fly).  Talking about coding standards (specifically J2EE standards).  Talk about modular design.

Mark proposes a re-focus on J2EE and then go agnostic.  Paul isn’t sure agnostic is a good direction; brings up that we didn’t want people to have to go out and purchase a container like jboss.  Mark ponders if wild fly from Redhat is a viable option.  Mark repeats goal of allow it to run out of the box is within reach.  KMA points out this is a major engineering effort, but wants to explore how to bring up the data service that would replace the 15 configuration files currently use.

Conclude it is a valid item to put on the list.  Paul, sounds like a little investigation to do.  Leon offers to lead the investigation.  KMA asks about priorities.

### Update Feb 2017:
- This investigation is an outstanding action on the Action Tracker.

OpenWIS and JBOSS Domain


Day 2 Morning Break

Presentation on Kanban (Paul)

Paul presenting on proposed Kanban process review.  Reviews process and current tools for managing the process via the wiki.

### Update Feb 2017:
- We implemented most of the suggestions eg: the Kanban and GitHub projects were used to monitor progress towards the open source release.

Day 2 Lunch

Break out into Geonetwork hack-a-thon

Three tracks.  Discussion over the tracks and what can be done.

Discussion about federated security.  Do we need it?   What are the security requirements today?

Harvest Evolution
Functional gap analysis
Current security requirements

The team broke up into two groups to cover topics 2 and 3.

Review from the groups.    Dom review of security group.  Basic review of some minor issues, but didn’t raise any major problems.

Review from gap group: 8 pass, 3 maybe and the rest (out of 30) fail.  A lot of work to do to make compliant.  Glue needed; data services are fine,  but UI needs much work.  Example is a UI to manage a subscription.  The group goes over five selected issues.

### Update Feb 2017:
- Dom will begin a discussion on this at the TC in Toulouse by exploring what GeoNetwork 3 features we can apply.
- The updated development process recognises that 'WIS 1.0' compliance is still required from OpenWIS v4, and beyond, even as we move to WIS 2.0.  The proposal here is that we need a test package, preferably automated, that we can use to verify compliance every time we make a change.
- We have to choose between which GeoNetwork features we use and which features we develop ourselves; compliance will be key.

Java layer (Geonetworks) thinking of using Spring as the glue.  Desire to build OW pieces with Spring and contribute the changes to Geonetworkrs.  This would ensure the changes will be part of future versions of GN.  This will be more work, but will smooth out changes in the future.  Some question as to if this approach should be approved by the SC.  Related to work from the UK (George) already in progress.  On option is to mod GN to match, but have a one-off.  Another is to start all over using bits of GN and maintain from here on out.  Current approach may require more effort but will be less work in the long run, be cheaper in the long run.  KMA asks if GN has a roadmap?  Unknown, but it is believed that v3 is a recent major re-architecture.

### Update Feb 2017:
- George has completed the work on the overlay/plug-in approach, so we can make any changes we want to the UI without relying on GeoNetwork accepting our changes.
- The issue now is how we share this knowledge with our developers; to be discussed in Toulouse.

Wrapping up.  Steve asks if it is still in range to announce open source at CBS.   Remy recommends SC approval.  Paul thinks current v4 is ok for release, others, including Remy thinks it should be more along and closer to being compliant before being released.    Continued discussion of where the line is.. If current system is good enough for release as a development system.  Paul asks what would be good enough.

Actions from Day 2:

Geonetwork 3 analysis and report due by end of October (Action: Eurodyn)
Work with Geonetwork in understanding users and groups within GN3.  These apply to metadata records.  Can something similar be created for data? (Action: Dom, Paul)

### Update Feb 2017:
- The GN3 analysis is published on the wiki.
- Dom and Paul N are looking at how to apply the GN3 groups concept and Dom will report at the Toulouse meeting.

General examination of extended JBOSS capabilities for portals) (Action: Entire Team, led by Leon)
Seek TC and SC approval of OpenWIS 3.14.7 as stable open source version. (Action: Dom, Paul)
Examination of using GN3 LDAP for user accounts.  Work to understand is how to shoehorn user permissions and groups to data as well as metadata, and the application of this to cache.  (Action: Dom, Leon, Eurodyn)
OpenWIS Public Announcement CBS material for review/comment period (Action: Remy)

### Update Feb 2017:
- JBOSS investigation is an outstanding action
- v3.14.7 was approved by TC/SC.
- LDAP investigation is an outstanding action.
- Material was delivered and the announcement made.



Day 3 ; Sept 29th, 2016

Participants in person:  Steve Olson, Bob Bunge, Marc Giannoni, Remy Giruad, Michael Claudon, Paul Rogers, Dimitris Papadeas, Dom Woollatt, Leon Mika, Lee yiokki,

Participants remote:  Ling T, Giorgos

Steve changes agenda based on yesterday’s Geonetwork hack a thon results.  Some presentations but a focus on CBS messaging and “What’s in open source release, how/when do we get there?”

What’s our message to CBS?

Discussion back and forth about what the message should be.  Dom working whiteboard, broad ranging discussion.

Leaning towards releasing 3.14 as first cut, and is frozen.  With v4 as next generation.  MFi can provide professional support for 3.14 if needed, but limited help from the Assoc at this point in time while we focus on v4.

Whiteboard discussions lead to a blueprint for CBS messaging (See the graphic below)



What is in the open source release?

Discussion about finalizing the CLA and getting it out to members for any legal review.  Needs to be signed by users before they are given the 3.14 code.  Final, frozen version is 3.14-7.  TC to finalize before UK to set this up.  UK to sort out CLA and pass to TC.



Presentation on Geonetwork 3 (George)

About how to make it more easier to change the JS base code.  Talks about how the JS modules are discovered and loaded and how the functions are registered.  Talk about core plus extensions model.  Steve asked if Geonetwork would be ok with this, but George states Geonetwork may not need to be involved.  Mark asks about updates to the code structure and asking how responsive the geonetwork community would be to the proposed changes.  He says it is possible they would be open.  Says it would not be easy and require a lot of testing.  Best model to make GN 3.x more extendable?  George: yes.   Turns into a discussion as to what we will provide to improve Geonetwork.  What can we contribute?


Angular 2 is the “Rolls Royce” option and is off the table.

Discussion about the current Spring approach, with talk about moving to a tags/data service hook approach in the form of OpenWIS Geonetwork extension modules.  Geonetwork has no concept of data, only metadata.  How our extensions, having been provided to the project, could be cloned to use both the OW approach as well as use the data services we will set up, especially for WIS 2.0.  Working towards agreement on the plug in approach that will allow us to do what we need to do, yet contribute back to geonetworks.   More review and talk about how the interfaces for the services will work.  Leon on the whiteboard.   Push to design plug in so we can also use the geonetwork security service and not have to build our own.

Lee and Leon reach agreement on what the components will be developed and how they combine and work together.  Paul wants to break work up into tasks that can be picked up by members.





Day 3 Morning Break

Presentation: Messaging Solution (Dimitris Papadeas)
Overview of subscriptions.  Review of protocols, JMS, AMQP, STOMP, MQTT, Hornet MQ.  ActiveMQ, RabbitMQ.  Good overview.  He recommends use of AMQP and ActiveMQ, but just his view.

### Update Feb 2017:
- Nassos (ED) has built a msg q PoC and will present it at Toulouse.

Discussion around how to use an MQ.  Example is to provide hooks in v4 so an implementer to use with the MQ favor of their choice.  Members could contribute modules using their fav for others to use.  Thus, v4 isn’t tied to a specific MQ flavor.

Messaging Solutions

Day 3 Lunch

Presentation: OpenWIS DCPC (Michael Claudon)
Reviews how they have deployed OW for use by a DCPC with binary NWP data.   Description of file structures and how the data is moved to the cache and the related harnesses.  Leon takes a task to add an action to Kanban regarding a file issue described in the talk and shared with the bureau.

Discussion about how to make it easier to subscribe to related products.  Model data… user doesn’t want to subscribe to 200+ products that make up the model.  Or VAAC products that include  text and also have an image.  How to handle this?  This is just a warning that this is a DCPC issue that will need to be dealt with in the future.

MeteoFrance Openwis 3.14 operational deployment



Review of Kanban list (Paul)

Highest Priority Items Table


Kanban Number
Required for OpenWIS 4.0 release?
Kanban Number
Required for OpenWIS 4.0 release?
40
Yes
61
Yes
41
No
62
Yes
42
Yes
64
Yes
43
Yes
65
No
44
No
66
No
45
No
67
Yes
46
No
68
No
47
No
69
Yes
49
Yes
75
Yes
50
Yes
77
Yes
51
No
79
Yes
52
No
80
No
53
Yes
81
Yes
54
No
85
Yes
55
No
98
No
56
No
127
No
57
No
167
Yes
59
Yes

### Update Feb 2017:
- Kanban board was updated as above at the time; has moved on a lot since.


Paul has the list of actions coming out of this.    One note: deployment guide, this needs to be the docs for the open source release.

### Update Feb 2017:
- The deployment guide was updated and included in the open source release package.


Comment from Paul: twice weekly scrum meetings tuesday and thursday at 11 BST.  Dimitri and George (?) are contractors (Eurodynamics) for UKmet.

Discussion about the scrum meetings and if they can be expanded to include more folks and used to more closely monitor progress and assign tasks.

### Update Feb 2017:
- We have settled into a pattern of Tuesday scrums that are timed to suit BoM and Thursday scrums timed to suit NWS.  Perhaps we should review this in Toulouse?


Talk about strategy for pushing UI changes to geonetworks.  One at a time to gain their confidence.    Also discussion on assigning tasks.   Assigning some of the easier ones to Michael and other new folk.

### Update Feb 2017:
- We have pushed a PR to the Core Geonetwork project to see how they react.  They are very busy with a major release at present so we are giving them some time before we prompt them to respond.

Spent some time helping KMA troubleshooting an indexing problems on VM on laptop.

Actions from Day 3:

Examination of the use of message queues.  This won’t happen in the initial 4.0 release, but occur downstream (Action: Entire Development Team)
Update Kanban list with a set of resources, once its determined a path forward with GN3 (Action: Paul to create in Kanban with support for entire development team)
Update OpenDJ/OpenAM scripts for deployment (Action: Michael Claudon)
Add NWS to bi weekly scrum meetings (Action: Paul)

### Update Feb 2017:
- These actions are complete though the MQ investigation is in progress and will be discussed in Toulouse.

Day 4 ; Sept 30th, 2016


Participants in person:  Steve Olson, Marc Giannoni, Remy Giruad, Michael Claudon, Paul Rogers, Dimitris Papadeas, Dom Woollatt, Leon Mika, Lee Yiokki, Ling T., Fred Branski

Participants remote:  None

Recap and summarization of workshop

Reviewed CBS messaging with Fred Branski.  He agreed with our approach.

Revisited OpenWIS Association and project websites.

Presentation: OpenDJ scripts (Michael):
Michael brought up a locally installed version of OpenWIS on his laptop.  There are scripts in github openDJ area for installing OpenAM/DJ.

Tieing up loose ends

The workshop team recommended the creation of a HW spec document for those wishing to try the OpenWIS SW out.

The workshop team also recommended the creation of a WIS Developer Conference, separate from the DecCon workshop.

The workshop team also polled where to hold the next DevCon meeting in 2017.  Leon suggested that perhaps it can be held in Australia.

Meeting Adjourned!

Thanks you all for a great DevCon 2016!

Steve Olson

## Update Feb 2017 - Developer Conference 2016 (DC) - OUTSTANDING ACTIONS

- Sep ACT-OWIS-DC-2016-01: LM - Creation of video on the build process
- Sep ACT-OWIS-DC-2016-05: PR - Have full sponsor’s Legal review CLA agreement and comment
- Sep ACT-OWIS-DC-2016-07: RG - Administration of Open Mailing list. Probably need to have one administrators of this list
- Sep ACT-OWIS-DC-2016-10: DW - Work with Geonetwork in understanding users and groups within GN3. These apply to metadata records. Can something similar be created for data?
- Sep ACT-OWIS-DC-2016-11: LM - General examination of extended JBOSS capabilities for portals) (Action: Entire Team, led by Leon)
- Sep ACT-OWIS-DC-2016-13: LM - Examination of using GN3 LDAP for user accounts. Work to understand is how to shoehorn user permissions and groups to data as well as metadata, and the application of this to cache.
- Sep ACT-OWIS-DC-2016-15: LM - Examination of the use of message queues. This won’t happen in the initial 4.0 release, but occur downstream (Action: Entire Development Team)
- Sep ACT-OWIS-DC-2016-17: MC - Update OpenDJ/OpenAM scripts for deployment
