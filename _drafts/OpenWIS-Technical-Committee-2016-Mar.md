---
layout: minutes
---

# OpenWIS Technical Committee - meeting minutes
7-8 March 2016, Seoul, Korea

#### 1. Welcome and introductions

#### 2. Approval of agenda
1. Approved.

#### 3. Agreement of working arrangements
1. Described by Okki Lee and agreed.

#### 4. Review current development / retrospective

##### 1. OpenWIS 3.14 release
1. MG - v3.14.3 is the current release candidate.  Issues have arisen from security testing.  We have fixed the critical issue.  There is a 3.14.4 release but this is experimental - it is being used to adapt OpenWIS to maven 3.
2. DW has completed User testing and produced a full report. There were some issues for accreditation and some other existing known issues.  DW has made some recommendations in the report.  So, going through the report issue by issue:
3. Test report: UC.B1 - Issue #98; LM is looking at this one and has raised PR#99 - which has been merged.  However it looks like more work is needed.

> A-OWIS-TC-2016-6 UKMO-MG: Raise a new issue.
4. WQ - this will affect when we release.
5. MG - Issue #73...
6. RGir - FMI and MFI have had this issue raised during an audit by Marcus.  It is not against technical regulations so there is a question of whether to fix or accept it?    Meteo-France don't open this function to end-users.
7. JT - we plan to improve metadata management in OpenWIS 4 so I propose that we defer it until OpenWIS 4.
8. MV - the FMI audit was approved with qualifications.
9. RGib - the Qatar DCPC (OpenWIS) was approved by Marcus.
10. WQ - OK, agreed: defer to OpenWIS 4.
11. MG - UC.B1 - The test report contains an extra note on a cross-site scripting vulnerability.
12. MG - UC.B5 - Nothing to add to the test report.
13. MG - UC.B10 Issue #152; LM - I'm testing that now... it works on 3.12, so it's a new issue.
14. MG - Additional observations from the test report include Issue #89 - a bug.
15. LM - looks too involved to sort it quickly - defer.
16. LM - Issues #123,#124 - looks like repeat of old one? Needs research.  Not frequently occurring, so defer.
17. RGir - Issue #32 - think fixed by Francois
> A-OWIS-TC-2016-7 MF-RGir: Check with Francois that #32 is fixed.
18. Issue #44: defer.
19. Issue #93:
20. WQ - Shall we aim to fix all these functional issues or aim to Release soon instead? [Round the room vote unanimous in favour of Release soon]
21. WQ - Ok we aim to release soon and defer these issues to a later release.
22. MG - Ok then, on to the security test issues:
23. MG - Pen testing #3: web service leaks info - not an OpenWIS software issue - a deployment issue - propose that we update the install guide to inform system admins.
> A-OWIS-TC-2016-8 BoM-LM: update the install guide (#3).
24. MG - Pen testing #6: sensitive info sent between client & server in open format.
25. JT - in future UKMO will use https - Strict Transport Security, for all traffic. Once again this is not an OpenWIS software issue, so let's document in deployment guidelines.  UKMO will share experience in how to use https-STS.
> A-OWIS-TC-2016-9 BoM-LM: update the install guide (#6).
26. MG - Pen testing #8: privilege escalation - fixed by BoM, tested and passed by MF in 3.14.2.
27. MG - Pen testing #9: editors able to modify all metadata - should only be able to mod own: propose fix in OpenWIS 4; defer.
28. MG - there have also been some build improvements - notably, the OWASP dependency checker now auto reports on each build.  Demo later.
29. WQ - The release timeline has already been deferred twice.  Can we say we can do 3.14.3 before end of March?
30. PR - Just waiting on response to whether Issue #32 is fixed.
31. RGir - MF have still to test;
32. MG - we have got a cloud accessible version.
> A-OWIS-TC-2016-10 UKMO-MG: send info on how to access the cloud testing to Francois
33. RGir - WMO CMP1.3 is in 3.14.3.

##### 2.              Testing
1.            WQ - How is the parallel testing environment going?
2.            MG - we were making progress but because the environment is inside a VPC we have found it difficult to open out - we are now taking a different approach.
3.            RGir - we have 2 shared servers with OVH using a simple VM environment.  I will say more about it later.
4.            WQ - so do we wait for the parallel testing environment or do our end-to-end testing in our own environment?
5.            [Everyone agreed to do end-to-end tests in own environments for the 3.14 release].
>             A-OWIS-TC-2016-11 ALL: do end-to-end tests in own environments for the 3.14 release
##### 3.              Jenkins & Cloudbees
1.            MG - we can feed OWASP dependency checks into Jenkins.
2.            RGir - that would be useful, but we are getting Jenkins emails into the SC mail list - should we only have them going to the TC mail list? [All agreed on TC only]
>             A-OWIS-TC-2016-12 UKMO-MG: Set up Jenkins emails for the TC mail list only
3.            MG - We need a full set of DNS entries for OpenDJ to work properly.
##### 4.              Deployment
1.            JT - Any comments on environment, technology etc., that we are using?
2.            OL - At KMA we are working on catching up.  We now have in-house Java developers on the team and we hope to contribute more.
3.            WQ - BoM ok with it.
4.            MG - the environment pops up and down; a more stable environment would help.
5.            OL - there are lots of tools so lots to learn. Do we have adequate docs to help new developers?
6.            LM - there is a lack of docs for on-boarding; this has been the experience at NWS; don't think we have anything for eclipse or maven.
7.            MG - the continuous integration environment needs amending to make it suitable for fresh installs; the one we have now was built on the assumption we are patching a 3.13 release, which we were for the 3.14 uplift.
8.            WQ - what would be the effort required to make it reusable for another uplift?
9.            MG - 2 weeks maybe - needs some research.

#### 5. Strategic decisions
##### 1.              J2EE vs non-J2EE (Spring or other framework (Note 1))
1.            For J2EE
    1. What kind of container we are targeting (JBoss, WildFly:)
    2. Should we code strictly to the J2EE standard to be container agnostic or are we happy to mandate a particular container, such as JBoss.
    3. If we mandate a particular container, should we make use of the extensions provided by that container (we currently tied to JBoss in OpenWIS configuration module)
2.            For non-J2EE
    1. Spring?
    2. Google Guice?
3.            WQ - BoM think we stick to J2EE - what do others think?
4.            JT - continue with heavy weight J2EE or go for light weight approach?
5.            MG - familiar with both - what benefit is J2EE? It is dated.  Spring offers easier deployment and configurability.
6.            JT - why are we using full J2EE/JBOSS? It goes back to AKKA; they needed it for exploitation of some J2EE capability eg: Soap and EJBs. You wouldn't design it this way now, but do we want to spend time and effort migrating just to follow a trend? No.
7.            WQ - Don't see benefit of moving now.
8.            JT - lighter weight gives you better deployment and config; Steve Olson at NWS is finding deployment hard - it is hard because we're half-in, half-out.  We do want to make it easier for a wider community to deploy.
9.            WQ - so is the effort/cost of migration worthwhile?
10.          JT - first we need to consider splitting the components.  Currently we have one monolithic build, most of which is not using JBOSS.  We should separate into deployable units, so that while the Data Services makes use of EJBs, all the rest could use a lighter weight server, over time.
11.          MG - We're already using Tomcat on the Security Service.
12.          RGir - we need to focus on features rather than architecture.
13.          JT - yes we do need to show improvements in function - but if we can break down components at low cost it would be good.
14.          RGir - we don't have a reference installation; we each deploy in many ways.
15.          WQ - the framework question does relate to what new features you will be able to provide easily.
16.          JT - so we should write new features so that they exploit light weight containers, or at least don't rely on heavy weight container properties.  The Data Services component is the only one we have to think hard about.
17.          OL - JBOSS is stable; we don't have to be trendy.  There should be clear and significant benefits to any migration.  Also, it is good to have one platform within an organisation.  KMA use Guice, which is based on JBOSS and we're happy with it.  We use JBOSS for OpenWIS.
18.          BR - should OpenWIS be independent of other platforms?  It is difficult for an open source organisation to recommend an enterprise class container.
19.          JT - NWS had to use Enterprise JBOSS because of internal standards, though we are recommending Community Edition (Wildfly).
20.          WQ - ideally all of OpenWIS would be open source, but how far should we go to accommodate organisations such as NWS?
21.          JT - Steve Olson recommends using the enterprise features of JBOSS; it is not appropriate to recommend that to everyone, but we can document that as an option.
22.          WQ - OpenWIS should be container agnostic.
23.          MV - in FMI, JBOSS is only used for OpenWIS, we had more of it 5 or 10 years ago; now we are using Tomcat.
24.          WQ - so for new features, could I build using Spring, but still use Wildfly?
25.          MG - so long as it sticks to the spec for web containers it should be ok.
26.          WQ - so we try to make compatible with main containers eg: wildfly, Tomcat.  What is the difference between JBOSS Community and Wildfly?
27.          MG - they are the same except that Wildfly no-longer uses Tomcat within - it uses solr/undertow instead.
28.          WQ - so if our path is towards lighter containers we should constrain new features to the J2EE spec - not enterprise features.
29.          LM - I am concerned about how much would be involved in mixing light weight and heavy weight together.  So new code would use pure Java and enterprise beans.
30.          JT - if we modify the application so each component is discrete, then only the Data Services needs a heavy weight container.
31.          WQ - and in the short term we stick with moving to Wildfly.
32.          JT - so we need to write down the architectural policy.  Working code is the objective - so always make sure we can deliver in our current architecture, especially where mixing light and heavy might prevent this.
33.          WQ - so the decision is: in the short term, we stick with Community JBOSS.  Longer term, we modularise components, and when we write new features we will try to keep the new framework in mind but fall-back on existing containers if needed.  We don't have to force compatibility with existing containers for new features.
34.          JT - so we use Wildfly, but avoid using the enterprise features.  When we're developing the software we should apply the architectural policy.
> A-OWIS-TC-2016-13 BoM-WQ: document the design pattern policy; still deploy to wildfly in short/medium term
35.          WQ - long term is 'beyond v 4'?
36.          JT - in v 4 I think we can try to: do the modularisation, avoid using container specific extensions and restrict ourselves to the web container spec.
37.          OL - Each Met service can choose to deploy any other container but we don't have to support it; also up to them to replace the container if they wish and if they have the capability to do it themselves.
##### 2. Approaches to automated deployment (Note 2)
1.            There's been a few minor attempts so far:
    1.        The configuration generation tool that came from AKKA
    2.        The set of scripts written for the AWS uplift environment
    3.        The set of scripts written for the Vagrant environment
    4.        UKMO is currently putting together a set of Puppet scripts for their internal purposes.
2.            To avoid the repetitive effort, the TC should decide on a unified approach for fixing this problem:
3.            A specific technology: Shell Script, Puppet, Docker, anything else?
4.            Being strict about choosing dependencies and components: we should only select components that can be deployed and configured from the command line.  No more components like OpenAM, which can only be configured through a web GUI.
5.            Striving to develop a solution that can be used for all environments OpenWIS may be deployed in (development, test, production).
6.            Not being afraid to make architectural changes to the OpenWIS application to make this possible.  This may include things like favouring convention over configuration (e.g. instead of specifying every directory in the "/data/openwis" tree, only specify the top level data directory and assume the default layout unless explicitly dictated within the configuration).
7.            RGir - is this for production or test?
8.            JT - I want to be able to deploy a fresh install of OpenWIS within 1 hour - at present it takes several hours.  To fully automate everything would be very hard.  But we should automate as much as possible.
9.            BR - should your test and operational environments look the same?  Depends on the type of test - so yes the pre-prod should be very similar.
10.          MG slides: [Annex1](MG1)
11.          OL - We need to distinguish between development, test, pre-production and production.  Hard to support everyone's deployment to production.
12.          RGir - Production and pre-production are almost the same.
13.          MG - Some scripts from develop can be reused in the production/pre-production environment.
14.          JT - the puppet scripts can be reused and should be as similar as they can be.
15.          BR - ideally we would get a puppet script to do a new install.
16.          JT - because each environment at each organisation differs in number of VMs etc, it is difficult to have one set of scripts to cover all these scenarios.
17.          BR - puppet and docker can help you install to machines by role.
18.          MG slides on: Benefits of sub system approach: [Annex2](MG2)
19.          MG slides on: Building the Stack: [Annex3](MG3)
20.          WQ - are we recommending puppet etc?
21.          MG - we need to do an assessment of the different environments.
22.          JT - so you're saying you need to modularise the deployment to take advantage of the puppet modularity - is modularising that complex?
23.          MG - no, it's just a question of working through it.
24.          JT - so you could have one portal that you can deploy in Admin mode or User mode?
25.          MG - Yes.
26.          JT - how specific is the puppet script code we are writing at the UKMO to the UKMO environments?  How reusable would it be for everyone else.
27.          MG - would need to see the other environments.
28.          OL - we should choose one of these technologies to use in the test or dev environment so that each organisation can get used to the approach - say puppet?
29.          WQ - we should explore options but it appears that puppet used already by UKMO, ECMWF, BoM, KMA.
30.          RGir - so we could make life easier for the newcomers to the community to do an initial deployment - so it will also make our life easier too.
31.          JT - ok, so UKMO will share its puppet scripts.
32.          RGir - So puppet is number one candidate for provisioning.  So we could use puppet to provide a vagrant deployment.
33.          JT - what about content packaging?  By content I mean subscriptions, users, etc., not stuff you can harvest from elsewhere.
34.          OL - not so easy because content could be in the database or the files etc.
35.          WQ - so we would just update the part we have changed from the old system.
36.          JT - but also thinking about recovery when you have lost the system; we can run scripts to get software back, but how do I get the content back?
37.          OL - this is an architectural issue as well as operational.  Normally we have fault tolerance with duplicate systems so if one dies we just rebuild from the other.
38.          JT - ok but if we're upgrading we might have to shut-down all instances.
39.          JT - so we need a ticket for a content migration strategy.
40.          JT - so in OpenWIS v4 when the Security Service becomes a SAML2 endpoint we will need to migrate LDAP data to GeoNetwork3.
##### 3. Position of OpenWIS software in each partner's operational environment (this will indicate functions that OpenWIS will be required to perform and therefore affect what features need to be developed in future).
1.            RGir - MF - our Transmet MSS and OpenWIS work together and subscriptions are automatically exchanged/updated.  The MSS will disappear at some time but not sure we want MSS features in OpenWIS.  We're using OpenWIS for catalog and user management.  We have built a system which uses OpenWIS to grant authorisation for data access via a WMS. This is fully operational; these users don't use OpenWIS directly or know their ID is being managed in OpenWIS.
2.            JT - UKMO - We use OpenWIS to operate GISC Exeter and soon a number of DCPCs.   Use as an operational service to meet our obligations for metadata, discovery and delayed mode push subscriptions.  OpenWIS is not used to do institutional subscription real time push.
3.            WQ - do you want it to do that?
4.            JT - No, we're happy with our MSS doing that.  Would rather focus OpenWIS efforts on what will come after GTS even if it's a decade away.
5.            WQ - fine for institutional user - but what about a public internet user?
6.            JT - We still think that is a goal; a browsable catalog; self registration for subscriptions; some sort of message queue publish/subscribe with web service endpoints. Targeting users with s/w apps that need data - eg mobile apps etc.  OpenWIS is helping us understand how to manage metadata records.  Like MF we are also trying to harmonise our management of users.
7.            RGir - at MF we have a web service API to access data and the authentication and authorisation token is stored in OpenWIS.
8.            JT - we are not integrating metadata access with data access.
9.            WQ - publish/subscribe could be done without OpenWIS - why use it for this?
10.          RGir - at MF we have a DCPC for our NWP products and we have used the mechanism of cache ingestion on OpenWIS to create JSON files that are pushed to our website where people can access them.
11.          WQ - BoM have done similar but using a local data source rather than cache ingestion.  Agent in local data source does the slice n dice and serves by ftp.
12.          JT - by using the pub/sub queue based approach we can scale and provide a mechanism for the future that could ultimately replace the GTS mechanism but without changing the way OpenWIS operates.
13.          OL - Canadian MSS is using AMQP.
14.          JT - we tried unsuccessfully to build a closer relation between our MSS and OpenWIS - we can't easily because OpenWIS doesn't support channels and if it did life would be much easier.  I want to hand-off delivery from OpenWIS to MSS.
15.          OL - is this essential short term?
16.          JT - no, medium term.
17.          RGir - so this is the future OpenWIS strategy.
18.          OL - KMA is not using OpenWIS for anything else.
19.          MV - FMI - DCPC only, just using OpenWIS for that obligation.  Have our open data interface (OGC) standard.  Could we use OpenWIS for INSPIRE discovery?
20.          MV - FMI - there is a national INSPIRE portal that harvests from the FMI portal; that uses GeoNetwork.  We are also using RabbitMQ in our Forecaster Work Station (Java).
21.          BR - how do we get Obs metadata accessible - Dominic Woollatt mentioned GeoNetwork might be able to do this?  Need to exchange and manage these xml recs.  Might be able to discover a WIGOS metadata service.  The OSCAR system is being set up to handle the Obs metadata management itself.
22.          RGib - MFI - OpenWIS is delivered as part of a solution - as part of the delivery system.  We want to be able to use INSPIRE and OGC View services etc.
23.          JT - you could provide OpenWIS for the metadata/catalog services then include for example a WMS and WFS as different system components.  I wouldn't see the OGC services as part of OpenWIS itself.
##### 4. Future development
1.            adoption of GeoNetwork 3 (including a GeoNework 3 demo from UKMO and enhancements made by UKMO)
    1.        [MG gave a demo of GeoNetwork 3 and some of the enhancements worked on by UKMO and GeoCat]
    2.        JT - even though the GeoNetwork community have improved scalability, what we have with Solr is much more scalable.  They deal with thousands of recs while we deal with 100's of thousands.  We want to help them and demo good open source behaviours.
    3.        JT - 2 types of changes were made by GeoCat:
        1. Core GeoNetwork changes
        2. OpenWIS add-ons.
    4.        JT - However, we're not entirely happy with how GeoCat chose to integrate the OpenWIS code
    > A-OWIS-TC-2016-14 UKMO-JT: Revisit the GeoCat code packaging.

    5.        JT - Authentication and Authorisation can all be done within GeoNetwork 3, or separated by having the authentication provided by an external SAML2 ID provider.
    6.        WQ - can we replace OpenAM/DJ with GeoNetwork to cut down the weight?
    7.        JT - yes, you could deploy OpenWIS 4 without an external security provider.  UKMO want to use the external OpenAM/DJ provider we already have for other purposes (ie: external to OpenWIS).
    8.        RGir - authorisation rules about who can access which data (not metadata) needs to be handled as roles/groups.
    9.        RGib - sometimes you want to restrict which users can see which catalog data, even just to tailor it to user roles.
    10.      RGir - ok but, by definition, all the data should be open to everyone.
    11.      BR - have we looked at CKAN?
    12.      JT - yes, UKMO had a comparative study done a year ago and GeoNetwork was recommended as the most stable and complete at the time.
    13.      RGib - the user role is important - the Admin portal has several dashboards but the User portal has fewer and is focussed on the User portal functions.
    14.      JT - Remy, perhaps you could help with the design by drafting a User Story for the User Portal subscription process.
    > A-OWIS-TC-2016-15 MFI-RGib: draft a User Story for the User Portal subscription process

    15.      JT - we could investigate metadata classification to improve the User experience.
    16.      RGir - for bulk subscriptions - MF have an Admin User way of doing this.
    17.      JT - we could have a single build that can be deployed/configured as either Admin or User portal.
    18.      JT - we will share the GeoCat docs that show the changes we have made. Currently we are working on a suite of automated tests to verify all works as planned.
    > A-OWIS-TC-2016-16 UKMO-JT: share the GeoCat docs.

2.            new features and/or technical enhancement (Note 3)
    1.        Improvements to subscription / ad-hoc data request UI : drive options from information in metadata record
        1.    WQ - we need a way to overcome the current restrictions on the information passed from the UI.
    2.        Bulk subscription
        1.    JT - We've not tried to address this yet under OpenWIS 4 - we know it is work in the hopper.
        2.    JT - we want to put subscriptions into a shopping trolley.
    3.        Deployment simplification : aiming for automated deployment (Note 2)
        1.    discussed earlier.
    4.        Modular deployment : consideration of micro-service pattern? : we might want to replace some components of OpenWIS with bespoke software already in use at the WIS centre
        1.    JT - I don't think we should go as far as micro services at this point, but modularise as discussed earlier.
    5.        Migration of SOAP web service interfaces between components to RESTful web services (that would simplify integration into other software)
        1.    JT - there are some potentially complex implications of moving from SOAP.
        2.    JT - however, we can complement SOAP interfaces between components by adding REST interfaces so that we can deprecate the SOAP services over time.
        3.    RGib - can we make the switched-off service endpoints in GeoNetwork operational again?
        4.    JT - new GeoNetwork 3 has a better set of Angular JS services that we can use.
        5.    OL - it's a major task to change an Interface.
        6.    JT - so we don't change the existing service end-points, we just add REST service end-points as well - over a 2/3 year timescale.
        7.    RGir - What's the benefit for normal users of changing internal services?
        8.    JT - GeoNetwork 3 assumes services it wants to interface with use REST, so we currently turn a REST service into a SOAP service and add complexity that we have to deal with when we develop, configure or deploy.
        9.    BB - What about other standards like CSW?  That's not REST.
        10.  JT - this is just about the internal interfaces between components.
    6.        Eclipse
        1.    JT - NWS have raised the topic of Eclipse - NWS are keen to get OpenWIS working with Eclipse and will take the lead.  Eclipse makes it easier to get other people to join the community and can be shared easily with others.
        > A-OWIS-TC-2016-17 ALL: make NWS aware of our requirements for Eclipse.

    7.        Use of pre-defined 'channels' for subscription / ad-hoc data request; make it easier to integrate with MSS components
        1.    JT - channels make it easier to work with MSS.  Also, setting up subscriptions is much easier because you don't have to keep repeating the destination setup.  However, adding channels into the design would mean refactoring subscriptions etc.
        2.    OL - Canada use AMQP (metpx; python, on source forge) - queuing can be used between users and MSS but this is a medium term objective.
        3.    BR - I think by channel we mean a 'predefined destination' - a channel/queue is a slightly different concept.
        4.    LM - at the moment subscriptions are tied to a single product, so you would need to divorce the one-to-one relationship.
        5.    RGir - subscriptions is a pain - we need a way to make it easier - whether that is a channel or not.  Could be push or pull.
        6.    WQ - we normally mean push when we talk about bulk subscriptions.
        7.    LM - if you start with the separation of products from channels it makes many of these things easier.
        8.    BB - what about pub/sub and self-serve?
        9.    JT - they are similar - if you are allowing people to sub to content as it arrives, mostly involving the routine GTS data.  The feeds work better if they stay light weight, so put the notification on the feed and let people come to get the data.
        10.  BR - it depends, small payloads are better going straight onto the feed.
        11.  JT - there are no implications for OpenWIS because all the data service features are in the data feed service rather than the OpenWIS function that points you to the service.
        12.  BR slides: RabbitMQ queue process types: [Annex4](BR1).
        13.  JT - so we could do some discovery to work out how these queuing patterns could work in OpenWIS.
        14.  OL - ok to change the UX but introducing the channel concept to end users may not be desirable.  KMA have problems with RabbitMQ because we have poor monitoring.  Introducing this queue processing to OpenWIS is non-trivial.
        15.  RGir - issue 1 - improving bulk subs; issue 2 queues etc.  Maybe we could have a separate project to look at the queueing issue - perhaps a harness between metpx and OpenWIS would do the job.
        16.  WQ - from what LM said about the bulk subs issue then we can take a small step to achieving both of these things by divorcing single product from single destination.  Are we talking about a dissemination tool?
        17.  JT - ok, let's add a task about UI improvement for bulk subs task to the plan for OpenWIS.  The other is a separate project.
        > A-OWIS-TC-2016-18 UKMO-JT: Create work package on UI improvement for bulk subs.

        18.  JT - let's discuss the AMQP potential project during the SC.

    8.        Implementation of WMO Core Metadata Profile validation package in OpenWIS 4 (we think Simon Pigot has done much of this already for BoM)
        1.    GeoNetwork 3 supports metadata profiles that can be used to check your metadata is conformant.  It's a relatively small piece of work to package up the profile for GeoNetwork, a few days - probably mostly already done by Simon Pigot. BB has asked for an update).
        > A-OWIS-TC-2016-19 BoM-BB: Ask Simon Pigot for an update.

        2.    BR - the install script should install this for everybody.
        3.    JT - we also want to investigate templates that implement WMO metadata guidance;  we will need a work package for that.
        > A-OWIS-TC-2016-20 UKMO-JT: Create a work package for WMO metadata guidance templates.

    9.        Improved integration with search engines; allowing search engines to index the catalogue.
        1.    JT - wouldn't it be great if we could just use Google or Bing to find the data we are after?
        2.    WQ - this is with the public community in mind rather than the met community - long term.
        3.    BR - low hanging fruit - we need better info in the abstract/metadata.
        4.    JT - is that low hanging fruit? The problem would be in changing our policy around metadata.  Low hanging fruit would be: when changing our pages, make sure we put appropriate info in the html headers etc.
        5.    OL - we have a very limited population who are interested in our data.
        6.    BR - But we are supposed to reach out to a wider community and support more programmes.
        7.    RGir - is this an issue for WIS or OpenWIS?
        8.    JT - the catalogs need to provide html pages that provide the right markup.  Then there is a separate issue of which of all the GISCs that contain this data you are redirected to - another discovery project?
        9.    JT - the expert teams need to work together to solve the metadata problem.
        10.  WQ - the problem is that the way we describe our data is poor.  Maybe we need meta-metadata; that's not within the scope of OpenWIS.
        11.  BB - we are trying to make OpenWIS handle the data delivery, so we end up with this very detailed metadata.
        12.  JT - we only support the WWW programme now, how do we work out how we support other programmes?
        13.  JT - the idea was for these other communities to use WIS to exchange their data, but they don't.
        14.  RGir - to handle NWP data we've packaged the data up into chunks - yet we still had to write 200 metadata records - we could improve OpenWIS by simplifying the metadata.
        15.  WQ - BoM have extended the metadata by putting this info into the Supplementary metadata field.
        16.  JT - it would be better to use metadata aggregates.
        17.  JT - GeoNetwork 3 allows you to describe the extra fragments - one parent metadata record with child records that contain only the fragments that are different.
        18.  JT - you have to know the purpose of the metadata, for example, are you helping discovery or helping ingestion?
        19.  WQ - the way OpenWIS associates data with that metadata would have to change.
        20.  RGir - yes we want 1 metadata for Synop, not 5000!
        21.  JT - so the work package should address how we provide coarse grained metadata that defines fine grained metadata, in a metadata hierarchy.
        22.  BR - but will that work for other GISCs?
        23.  JT - no, but if we can demo it working on our develop branch then we can work to amend the technical regulations.
        24.  WQ - Each GISC implements the association with metadata in a different way, even though all follow the standard.  So, we should do something to demo how WIS can be improved.
        25.  RGir - this would also improve the bulk subscriptions problem.
        26.  JT - sounds like we need to explore more fully exactly what problems we are trying to solve.  Let's have a work package and decide who will participate in that work. Then figure out some possible solutions.  Then submit Papers to WMO committees etc.
    10.      Work through proposals for how roles and governance will work in OpenWIS 4 for accessing / editing (meta)data (we plan to adopt the GeoNetwork methods); can we infer roles from data policy (e.g. WMO Essential); is there a need to harmonise the Groups in GISCs (roles are assigned to a particular Group for a given metadata record)
        1.    [JT - displayed the GeoNetwork manual - the pages on Users, Groups, Roles http://geonetwork-opensource.org/manuals/trunk/eng/users/administrator-guide/managing-users-and-groups/index.html ]
        2.    JT - What Groups should we define?
        3.    WQ - GeoNetwork looks like it has a detailed enough process for what OpenWIS does.  How does this help implement Data Policy?
        4.    JT - you can implement WMO Essential - no access controls - not anything else.  Not sure we have a good way of implementing Data Policy.  This is a part of migration to OpenWIS 4 that still needs further thought.
        5.    WQ - how would GeoNetwork expose these privileges etc to OpenWIS?
        6.    JT - GeoNetwork decides based on permissions whether to show you the buttons for the related actions.
        7.    RGib - we should investigate how to link the data policy in the metadata with the assignment of GeoNetwork privileges - but maybe too complicated.
        > A-OWIS-TC-2016-21 MFI-RGib: Investigate how to link the data policy in the metadata with the assignment of GeoNetwork privileges.

        8.    RGir - We also have a problem syncing access privileges between GISCs or even agreeing a common understanding of roles between GISCs.
        > A-OWIS-TC-2016-22 MF-RGir: Create a work package to review Data Policy and Access Control implications in detail.

3.            new technology (RESTful vs SOAP? More facilities such as a CI testing environment or servers for hosting Vagrant environments?)
    1.        Already discussed above.
##### 5.              Security (OpenAM/OpenDJ vs GeoNetwork built-in security solution)
1.            JT - lets go thru the Use Cases for roles and groups and authorisation
2.            RGir - We currently use the Security Service to control data access (as well as metadata access).  We do need something to do this - maybe GeoNetwork?
3.            JT - that would be part of the Data Policy work package; though we may need to do some implementation work to get GeoNetwork to provide a token to allow a 3rd party service to verify a user can access a piece of data.
> A-OWIS-TC-2016-23 UKMO-JT: Include the requirement for the Security Service to control data access in the Data Policy workpackage.
4.            GeoNetwork accreditation/authorisation options are 1. Local (light weight) 2. LDAP 3. External SAML2 ID provider.
5.            LM - what tech provides that?
6.            JT - Apache Shibboleth for SAML2, Spring for LDAP.
7.            MG - the external provider is configurable through xml.
8.            JT - we had the SAML2 ID provider work done and donated back to core GeoNetwork.
9.            RGir - I can give an update on our progress with the auto deployment of OpenAM/DJ - we have just taken the first delivery of the .org version, which we are currently debugging.  We will hopefully deliver this within the next month, it's written in shell script.
##### 6.              Going open source (governance, collaboration development environment, improvement in use of GitHub, development policies, developer documentation, project website, use of the forum etc)
1.            PR - having observed the development over the last year, I would like to recommend that we adopt the Kanban method to improve our development practices.  Kanban is easy to understand and is effective where the availability of developer capacity and skills is variable.  Kanban is a 'pull' method, where work is added to a hopper or inbox, and then pulled for development when there is capacity and skill to do a particular work package.  Work packages cycle through a number of states eg: ready, develop, test, deploy, and the state of all work is visible to everyone, allowing for prioritisation and coordination.  A key feature of Kanban is that the amount of work-in-progress in each state is deliberately limited.  This ensures that we don't try to progress too many changes at once, which in turn helps to manage workload, complexity and quality and so ensure a smooth delivery of finished features.  The Kanban cycles result in releases that occur at fixed dates and so contain whatever features are ready by that time.  The fixed release dates make it easier to plan local testing and deployment and actually get new features into production through continuous improvement cycles.  Kanban would also work well with GitHub and with the open source community.
2.            WQ - Ok, sounds like it would be worth a look.
3.            PR- I'll make a proposal around the work packages for the v4 release and if everyone is happy with that we'll try it out.
> A-OWIS-TC-2016-24 UKMO-PR: Propose a Kanban workflow for v4 development work.
4.            WQ - so when do we think the v4 release will be?
5.            PR - we're still working to resolve the harvester problem in GeoNetwork 3 and currently estimate June 2016 for a development release of 4.x.
6.            JT - so shall we say 6 months or 9 months to the next Operational release?
7.            OL - seems too short, we still have to finish release v3.14.  Beyond that, KMA would like to begin contributing, but our new developers have to become familiar with the software and the tools first. I think 12 months would be realistic.
8.            WQ - 12 months, that would be March 2017.  Ok, so if we're all happy with that, we agree March 2017 for the Operational release of v4.
> Recommendation 1: Target operational release date for OpenWIS v 4 is 31st March 2017.
9.            JT - I would like to begin using the alternate odd/even minor release number system, in which the development release have an odd minor version (eg: v4.1.x) and the operational/public releases have an even numbered minor version, so, our next operational release would be v4.2.x
10.          WQ - when will we make the open source announcement?
11.          JT - we could announce once we have a development release to show - v4.1.0.
12.          OL - we should have a stable release to go open source.
13.          JT - there would be no point open source developers investing effort in the 3.14 code base, so this way the contributors can install the development version to see where we're going.
14.          JT - we also need docs etc to support an open source release.
15.          OL - it takes time and money to produce docs.
16.          JT - NWS find the code base impenetrable; there is no effective start-up or onboarding process... so we need docs for this ourselves anyway.  So not as polished as a Redhat release, but something to get newcomers started.
17.          WQ - so we set a task to develop a doc set for developers and bear in mind open source users.
> A-OWIS-TC-2016-25 BoM-WQ: TC to set a task to develop onboarding docs set for developers.
##### 7.              Documentations - for user, developer, administrator (how we manage the documents, in what form, where etc)
1.            JT - so our decision last time was to use Github, Markdown, Jekyll, html.
2.            MV - should someone be responsible for the docs?
3.            JT - Yes, the developers, it's not part of the Community Mgr role.
4.            PR - set up a Markdown to html conversion/publication process - see Richard Hattersley in the UKMO AVD team.
> A-OWIS-TC-2016-26 UKMO-PR: Investigate/arrange a Markdown to html publication process.
5.            WQ - where should the docs be published?
6.            JT - on Github and the openwis.io website.
7.            WQ - is any retrospective work needed to convert existing docs to Markdown?
8.            JT/MG - yes, it needs a task.
9.            WQ - do we want to say what docs we need?
10.          JT - initially, docs to onboard new developers such as at KMA, NWS.
11.          JT - for open source we will need a code of conduct/ethics for new developers - don't start from scratch - use another open source project as a template.
12.          JT - we need to write down our development process - understand all the roles and responsibilities we are giving to people - doc manager, release manager, contributors, etc and how you get to be one of these roles.
13.          JT - we need a project website that describes the OpenWIS software, status of the build, status of the project, Kanban board, work packages etc.
14.          MG  - we will also need a style guide for pages, code etc
15.          BB - you also need project communications and governance - SC/TC etc.
16.          JT - yes we should publish the meeting details for TC/SC, agendas, minutes, how you join in.
17.          BB - contributors, IP holders, issue trackers, licences...
18.          JT - also, to help people spin up, we would provide other resources eg: Eclipse tool for project - publish it on our website.  Needed for ourselves as well as the open source project.
19.          WQ - what do we need to do now?
20.          JT - at a minimum translate into markdown.
21.          WQ - install guide?
22.          JT - should the OpenWIS Association budget for a technical author to make a start on this?  We have content but need templates, style sheets etc.
23.          WQ - we should.
24.          JT - we could get the OpenWIS Association to buy that resource in for say 20 days.  Cost about +AKM-400/day?
25.          MG - do we include architecture/design docs?
26.          JT - they might be better on the wiki.
27.          WQ - Ok, agreed - recommend to SC - for about 10k euro. Aim to deliver June 2016.
> Recommendation 2: Hire a technical author to establish an initial guide and style.  Budget about 10k Euro.  Aim to deliver by end of June 2016.
#### 6. Review the 'Melbourne TC plan' and update the (technical) Roadmap.
1.            Release scope (what should be included in the next release)
    1.        PR - doesn't make sense to do this now, since we're going to try the new Kanban approach for v4 and the tasks required to finish 3.14 are well understood and in progress.  So, action on PR follows...
    > A-OWIS-TC-2016-27 UKMO-PR: transfer backlog and Github issues for v 4 to a Kanban board.

    2.        JT - there needs to be a governance process to approve work packages - we'll cover at the SC.
2.            Project scope (e.g. setting up open source community, writing documentation, set up web site)
    1.        PR - should include on the Kanban board.
    > A-OWIS-TC-2016-28 UKMO-PR: Include tasks on the Kanban board to cover: docs, open source community activities, setting up a web site etc.
3.            Time line (schedule vs agile development 'ordered open-ended backlog')
    1.        So aiming for open source release June/July.
4.            Allocation of tasks (task tracking - Waffle Board? GitHub? Trillo? )
    1.        PR - we will continue to use GitHub for code and related issues.
    2.        PR - For the Kanban board - maybe Waffle - we'll see how that looks and have a look at a few other tools.
#### 7. Other Business
1.            Shall we organise another Developer Conference? Propose costs to SC?
   1.        JT - NWS are keen to participate in a Developer Conference this time around - in Sept? NWS might be able to host in Washington.
    2.        RGir - we could invite other people since the development version will be out.
    3.        WQ - Ok, agreed - we recommend to SC that we will have a Developer Conference in 2016 and budget accordingly.
    > Recommendation 3: That we have a Developer Conference in 2016 and budget accordingly.

    4.        The TC acknowledged the good job LM has done as lead developer at the last Developer Conference and ever since.
    5.        RGir - Developer Conference could focus on OpenWIS 4 and GeoNetwork 3.
    6.        JT - we should pass on lessons from the last Dev Con.
>             A-OWIS-TC-2016-29 UKMO/BoM-PR/LM: pass on lessons from the last Dev Con.
2.            Next meeting (routine TC conference call, anything that needs to improve? Move to webex?)
    1.        WQ - Trial TC by Webex.
    > A-OWIS-TC-2016-30 BoM-WQ: Trial TC by Webex.

    2.        RGir - encourage members and partners to attend TCs.
3.            Demonstration of OpenWIS Core 4.x
    1.        Done earlier
    2.        RGir  - We need a point of contact for questions about adding users to Github, cloudbees etc.
4.            Status of cloud servers set up by MF:
    1.        RGir - we have 2 (physical) ProxMox - 32G RAM 2TB Disk - able to create VMs etc - dedicated server within cloud. NAT used to isolate from outside.  Need someone to manage admin: eg have root pwd and manage VMs - who should do that?
    2.        RGir - Create 3/4 VMs per team?  Also have shared VMs.  Struggling with DNS setup for OpenAM.
    3.        JT - more persistent DNS needed for OpenAM - have approved domain openwis.community on AWS.
    4.        RGib - MFI are still managing openwis.io
    5.        WQ - could we run the parallel testing on this system?
    6.        JT - we've been setting up a more durable test environment on AWS - costs about $18000 per year.  The ProxMox servers are much more cost effective to keep running.
    7.        RGir - who would administer the ProxMox environment?  We need a point of contact for it.
    8.        MG - is it locked down or can developers install software?
    9.        RGir - Developers can install software.
    10.      RGib - So the TC should decide what environment you find there? GISC? DCPC?
    11.      WQ - what's the workflow?
    12.      RGir - eg: NWS could have worked out how to install on these servers.
    13.      OL - allows us to put something there for other partners to test.
    14.      RGir - Dom could have shared testing tasks amongst others by running the test systems here.
    15.      WQ - so we might not need the AWS shared test environment?
    16.      MG Yes, that's right.
    17.      WQ - so MF will continue the maintain this?
    18.      RGir - yes. Paid for up to Mar 2017 - decide then if it is still worth having.  MF not expecting reimbursement from Assoc.  Maintainance admins could be in more than one organisation.  You can also create snapshots.
5.            Resources available:
    1.        UKMO - couple of developers, Martin/Andy; Paul Nelson on puppet; CM team; Dom - testing
    2.        BoM - 2 almost full-time resources on OpenWIS
    3.        JT - NWS - not sure what proportion - Steve Olson has 3 guys working for him so thats 4.
    4.        MFI - Only RGib - can bring in developers for work done for customers.  Maybe work on the WIS GISC catalog - other GISCs can put a single report into multi categories so maybe we will develop this.
    5.        KMA - one developer (2x0.5)
    6.        MF - 0.5 java dev for a year, so better than before.
    7.        FMI - have about 2/3 months of a java dev.
#### 8. Meeting closed

###### Participants:
- BoM WQ: Australian Bureau of Meteorology, Weiqing Qu  (chair)
- BoM LM: Australian Bureau of Meteorology, Leon Mika
- BoM BB: Australian Bureau of Meteorology, Bruce Bannerman
- KMA OL: Korea Meteorological Administration, Okki Lee
- KMA HL: Korea Meteorological Administration, Hyekyoung Lee
- KMA SP: Korea Meteorological Administration, Sungeun Park
- KMA CSP: Korea Meteorological Administration, Chung Shin Park
- MF RG: Meteo-France, Remy Giraud
- MFI RG: Meteo-France International, Remy Gibault
- ECMWF BR: European Centre for Medium Range Weather Forecasting, Baudouin Raoult
- UKMO PR: UK met Office, Paul Rogers
- UKMO MG: UK Met Office, Martin Gollogly
- UKMO JT: UK Met Office, Jeremy Tandy
- FMI MV: Finnish Meteorological Institute, Mikko Visa
- FMI MP: Finnish Meteorological Institute, Mikko Partio
###### Apologies:
- NWS RB: US National Weather Service, Robert Bunge
- NWS SO: US National Weather Service, Steve Olson


List of all possible Participants
BoM WQ: Australian Bureau of Meteorology, Weiqing Qu
BoM LM: Australian Bureau of Meteorology, Leon Mika
BoM BB: Australian Bureau of Meteorology, Bruce Bannerman
KMA OL: Korea Meteorological Administration, Okki Lee
KMA HL: Korea Meteorological Administration, Hyekyoung Lee
KMA SP: Korea Meteorological Administration, Sungeun Park
KMA CSP: Korea Meteorological Administration, Chung Shin Park
MF RG: Meteo-France, Remy Giraud
MFI RG: Meteo-France International, Remy Gibault
ECMWF BR: European Centre for Medium Range Weather Forecasting, Baudouin Raoult
NWS PG: US National Weather Service, Pat Gillis
NWS MG: US National Weather Service, Marc Giannoni
UKMO PN: UK Met Office, Paul Nelson
UKMO PR: UK met Office, Paul Rogers
UKMO MG: UK Met Office, Martin Gollogly
UKMO JT: UK Met Office, Jeremy Tandy
FMI MV: Finnish Meteorological Institute, Mikko Visa
FMI MP: Finnish Meteorological Institute, Mikko Partio
NWS RB: US National Weather Service, Robert Bunge
NWS SO: US National Weather Service, Steve Olson
NWS KS: US National Weather Service, Kari Sheets





# Dillinger

Dillinger is a cloud-enabled, mobile-ready, offline-storage, AngularJS powered HTML5 Markdown editor.

  - Type some Markdown on the left
  - See HTML in the right
  - Magic

You can also:
  - Import and save files from GitHub, Dropbox, Google Drive and One Drive
  - Drag and drop files into Dillinger
  - Export documents as Markdown, HTML and PDF

Markdown is a lightweight markup language based on the formatting conventions that people naturally use in email.  As [John Gruber] writes on the [Markdown site][df1]

> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

This text you see here is *actually* written in Markdown! To get a feel for Markdown's syntax, type some text into the left window and watch the results in the right.

### Version
3.2.7

### Tech

Dillinger uses a number of open source projects to work properly:

* [AngularJS] - HTML enhanced for web apps!
* [Ace Editor] - awesome web-based text editor
* [markdown-it] - Markdown parser done right. Fast and easy to extend.
* [Twitter Bootstrap] - great UI boilerplate for modern web apps
* [node.js] - evented I/O for the backend
* [Express] - fast node.js network app framework [@tjholowaychuk]
* [Gulp] - the streaming build system
* [keymaster.js] - awesome keyboard handler lib by [@thomasfuchs]
* [jQuery] - duh

And of course Dillinger itself is open source with a [public repository][dill]
on GitHub.

### Installation

Dillinger requires [Node.js](https://nodejs.org/) v4+ to run.

You need Gulp installed globally:

```sh
$ npm i -g gulp
```

```sh
$ git clone [git-repo-url] dillinger
$ cd dillinger
$ npm i -d
$ NODE_ENV=production node app
```

### Plugins

Dillinger is currently extended with the following plugins

* Dropbox
* Github
* Google Drive
* OneDrive

Readmes, how to use them in your own application can be found here:

* [plugins/dropbox/README.md] [PlDb]
* [plugins/github/README.md] [PlGh]
* [plugins/googledrive/README.md] [PlGd]
* [plugins/onedrive/README.md] [PlOd]

### Development

Want to contribute? Great!

Dillinger uses Gulp + Webpack for fast developing.
Make a change in your file and instantanously see your updates!

Open your favorite Terminal and run these commands.

First Tab:
```sh
$ node app
```

Second Tab:
```sh
$ gulp watch
```

(optional) Third:
```sh
$ karma start
```

### Docker
Dillinger is very easy to install and deploy in a Docker container.

By default, the Docker will expose port 80, so change this within the Dockerfile if necessary. When ready, simply use the Dockerfile to build the image.

```sh
cd dillinger
docker build -t <youruser>/dillinger:latest .
```
This will create the dillinger image and pull in the necessary dependencies. Once done, run the Docker and map the port to whatever you wish on your host. In this example, we simply map port 80 of the host to port 80 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 80:80 --restart="always" <youruser>/dillinger:latest
```

Verify the deployment by navigating to your server address in your preferred browser.

### N|Solid and NGINX

More details coming soon.

#### docker-compose.yml

Change the path for the nginx conf mounting path to your full path, not mine!

### Todos

- Write Tests
- Rethink Github Save
- Add Code Comments
- Add Night Mode

License
----
