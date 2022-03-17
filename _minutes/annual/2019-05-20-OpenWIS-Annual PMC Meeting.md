---
layout: page
title: OpenWIS Annual Meeting PMC 2019
minuteOwner: annual
---

#### 20th May 2019 - Washington, USA - meeting minutes

---
1. **Welcome and introductions**
    - RGr - introduced and thanked NWS for hosting the annual meetings for 2019.
    - SO - Welcomed everyone and all introduced themselves. SO also explained the PMC and TC agendas.
    - JA - explained the SC and Board agendas.
    - JT - highlighted the need to discus, at some point, the focus of OpenWIS towards WIS2.

2. **Attendees**
    - The attendees were:
    - SO - Steve Olson, National Weather Service, USA [NWS], PMC Lead and Chair
    - BB - Bill Bolholfer, National Weather Service, USA [NWS]
    - KS - Kari Sheets, National Weather Service, USA [NWS]
    - MG - Marc Giannoni, National Weather Service, USA [NWS]
    - ZZ - Zhan Zhang, National Weather Service, USA [NWS]
    - BS - Benjamin Saclier, Météo-France, France [MF]
    - RGr - Remy Giraud, Météo-France, France [MF]
    - DP - David Podeur, Météo-France, France [MF]
    - LG - Loïc Le Gallou, Météo France International (MFI)
    - YL - Yannick Lizzi, representing MFI [AKKA]
    - MV - Mikko Visa, Finnish Meteorological Institute [FMI]
    - MP - Mikko Partio, Finnish Meteorological Institute, Finland [FMI]
    - SD - Sungsoo Do, Korea Meteorological Administration, Republic of Korea [KMA]
    - KL - Kwangjae Lee, Korea Meteorological Administration (KMA)
    - SS - Stephan Siemen, European Centre for Medium-Range Weather Forecasts (ECMWF)
    - JT - Jeremy Tandy, Met Office, UK [UKMO]
    - JA - Jude Anthonisz, OpenWIS Association Secretariat
    - DPa - Dimitris Papadeas, European Dynamics, [ED]

  *Apologies:*
    - WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM]

4. **OpenWIS 3.x**

  *4.1 Change in CI env*
  - DPa joined the meeting remotely.
  - SO - The key issue is the need for clarity of the environment (cloud?) needed for a Travis based CI   environment. What role did cloud play in the process of a building a CI environment previously?
  - DPa - depends on definition of environment – deploy or build?
  - BS - to deploy
  - DPa shared deployment instructions.
  - SO - When building with Cloudbees was a local environment used? Where were things stored? Using 3.14.8 as an example, with code is stored in Github, what is the mechanism and build process?
  - DPa - CloudBees, Jenkins, and Travis are applications that support and automate build and deployment. CloudBees and Jenkins are tools that can confirm that the build and code is working well.
  - DPa - Build is when you create artefacts in a local server.
  - JT - Clarifying process and environments. The process – code would start the build process. Jenkins – creates a build. Another process manages the artefacts that already exists and then how do we deploy?

  - SO - we are talking about the first, i.e. to build.
  - JT - OK
  - DPa - Understood.
  - SO - To recap, - we need to start with knowing how to do a build in Travis and then uploading back into Github for anyone to organise to take the build and then deploy.
  - DPa explained the process in reference to these documents (https://github.com/OpenWIS/openwis/wiki/v3.14.5.1-Deployment-Instructions) and (https://github.com/OpenWIS/openwis/wiki/Getting-Started).
  - DPa - For many developers doing dev, each developer has their own repository and submit their code via a Pull Request.
  - JT - At the point of creating the Pull Request, is there an automated job that processes and does the unit tests?
  - DPa – I can explain process using a local Jenkins build and Issue #285 as an example in OpenWIS Github. After accepting the Pull Request, it is uploaded into Jenkins.
  - SO - A developer will create a Pull Request, test locally (unit tests), then merge the Pull Request, merge the specific and/or other Pull Requests. This executes nightly builds.
  - JT- SO the question what bits of infrastructure are missing in the move from CloudBees to Travis.
  - SO - Yes.
  - SS - where is the build taking place? Cloud?
  - JT - Would use an AWS environment using AWS in Met Office. The issue is that we haven’t been doing nightly builds for some time. Hence its broken.
  - SS - We used Travis
  - JT - We need to look at that.
  - SO - I feel comfortable with what we have to with Travis. Any questions about the process form anyone?
  - All - No.
  - SO - We still need to investigate Travis and see what the difference are vs CloudBees and see what resources we need for OpenWIS Association, i.e. tools and people. So, let’s talk about people resources.
  - RGr - When we look at resourcing from OpenWIS, we need to ask why would OpenWIS need to invest as OpenWIS 3x is frozen.
  - JT - We will need to maintain OpenWIS 3x to ensure it works as a minimum. We are not expecting to evolve or improve OpenWIS 3x.
  - SO - Yes, there are other examples, such as CentOS end of life between now and 2024. So, yes, we need to consider this as a group and therefore who can we count on to be part of maintaining the new CI environment. If we do not feel that we have anyone that can do this, we need to make a proposal to the SC for investing in external resources.
  - SS – If Its linked as part of Travis and is simple, then its easy. ECMWF can help if it’s simple. We do not use Jenkins, we use Bitbucket. If more complicated like hosting, then will not be possible to help.
  - JT - Yes, starting simple is good and we would not have to do this very often,
  - BS - MF will not have spare capacity due to other commitments.
  - JA - we need beware that if we use external resource solely, then things will get done but we would not gain and retain knowledge across the Association.
  - JT - I would be happy if we use external resource for set up and annual audit to make sure we are following the process for say up to two years.
  - SS - This is the model we used in ECMWF.
  - RGr - would the contract be with OpenWIS ?
  - JT - We can discuss the contracting approach in the SC

  RES-OWIS DECISION - proceed with the proposal to use external resource to help set-up a CI CD environment with follow up audits each year. We would have audits for 2 years and review what we need to do.

  *ACTION - SO to develop a proposal along the line of JT’s idea to discuss at the TC to potentially propose to SC*

  *ACTION - SC to ensure that the contracting approach is discussed on 22 May 2019.*

  - JT - are ECMWF happy to participate in the team?
  - SS - Yes
  - BS - Around the table, we are familiar within Jenkins more than Travis.
  - JT - Not sure whether Travis covers the features of Jenkins.
  - SS - We use bitbucket.
  - BS - What would be the approach? Training on Travis and continue to use the experience of Jenkins or bitbucket (i.e. makes use of the best knowledge and practise in the OpenWIS Association)
  - DP - how long can we rely on Travis for?
  - JT - we can’t tell or control what Travis will do. So, when we contract a third party, then we should not make the set up and audit specific to Travis or any other tool.
  - SO - the piece is the system resources. A local resource vs. cloud-based resource or something that can be shared. What do we think? If a shared resource,then a proposal then a proposal to SC.
  - JT - TC can make this decision, subject to a limit set by SC.

  *ACTION - SO to ensure that TC makes a proposal to the SC regarding system resource spend for the CI CD environment.*
  - SS - This is open source. So, shouldn’t be expensive, the longest build I’ve seen is 3-4 hours. As no active development, a shared resource may be most appropriate.

  *[ACTON - JT to explore with AWS what support resource is available](https://github.com/OpenWIS/openwis-documentation/issues/532)*

  - LL - The key point is sustainability. I think RGb (MFI) will be happy with the proposal. We could also look at other contractual options.
  - SS - What assets were considered in the past when tests were run in CloudBees (executables or something that can be taken and run locally?)
  - DPa- If you refer to the guidance documentation, some a library tools and some are code. The document/resource is not accessible as CloudBees was deprecated in December 2018.
  - JT - Thanked DPa for his contribution.
  - DPa - left the meeting
  - SO - We have YL and RGb on-line. We will wrap up and ask you to wait on the line.

  Meeting paused for break.

  - BS - The new CI needs to be functional by end of September 2019.
  - SO - So let’s agree a date for the RFP. What times-scales are you working on.
  - SS - Aim to get a draft proposal by mid-June 2019.

  RES-OWIS DECISION - Agreed that the target is to get the draft procurement proposal by mid-June 2019.

  - JT - We will talk about who and how procurement will be undertaken at the SC.
  - SO - the team will be ECMWF, NWS, MF and MFI.

  RES-OWIS DECISION - the team that work on the procurement of the CI environment is ECMWF, NWS, MF and MFI.

  - LL - will check with RGb and feedback on what help MFO can provide.

  *[ACTION - LL to check with RGb and feedback on what help MFO can provide](https://github.com/OpenWIS/openwis-documentation/issues/533)*

  *[ACTION - SO to co-ordinate drafting requirements of new CI environment](https://github.com/OpenWIS/openwis-documentation/issues/534)

  4.2. **Process documentation**
  - SO - outlined we need to document major and minor builds
  - JT - I think we need look at what we need to if something breaks and work backwards
  - JT - Major = system is different. Minor – a change that impacts a user. Patches – simple changes. The PMC chair will make the decision on whether a specific release, major, minor or a patch.
  - All - agreed.

  RES-OWIS DECISION - Major = system is different. Minor – a change that impact a user. Patches – simple changes. The PMC chair will make the decision on whether a specific release, major, minor or a patch.

  - SO - we need a set of resources to make use more current and documentation ensure it is not out of date. Who can assist with getting release and institution notes up to date? (i.e. in addition to Zhang).
  - SS - We are happy to be testers of documentation and will feedback.
  - MP - We can participate in creating and testing.
  - SO - In summary, FMI, SS, and NWS and assist.

  *[ACTION - SO to co-ordinate updating existing release process documentation with support from ECMWF and FMI based on 3.14.8](https://github.com/OpenWIS/openwis-documentation/issues/535)*

  - SO - Like to understand which version on OpenWIS is installed to help is prioritise maintenance going forward. Please see me later.

  *4.3 OpenWIS 3x risks*
  1.3.1 Review of alternatives to OpenAM and OpenDJ.

  - SO - Using NWS’ experience of this issue, i.e. when needing to upgrade OpenWIS 3.14, the issue of not being able to access Forgerock libraries has prevented creating a build. Handed over ZZ for more detail.
  - ZZ – Wildfly 8 to 15 - unable to patch (ref to Google doc) means a need for OpenDJ 4 and OpenAM 14 (and from 3 and 13, respectively) due to being unable to access libraries in Forgerock. Some options - by requesting the target source at the Service Provider (in this case the Service Provider will the OpenWIS instance) Picketlink, Shibboleth or the Spring Framework.
  - BS - Do we need OpenDJ and OpenAM and we rarely use SSO.
  - ZZ - We have not looked at that option, we focused on replacing something that is simpler than OpenDJ or OpenAM.
  - LL - Can we look at the options that MFI has, so that we have also the options on the table to enable us to make a decision.
  - RGb and YL – presented analysis (here is the document – (#539 (comment)) , so far undertaken by AKKA to resolve the issues caused by middleware deprecation (incl. OpenDJ2.6 and OpenAM 12), based on OpenWIS 3.14. The main constraint is Java8 (i.e. move from v8 to v11) by December 2020.
  - Function of OpenAM for OpenWIS = manage SSO between GISC and DCPC.
  OpenAM status - closed since 2016. Renames to ‘Forgerock Access Mgmt’ i.e. commercial.
  OpenAM OpenSource forks = Open Identity Platform Community – seems to be an outstanding option. Wren- not studied.
  - JT - Can be the alternative source of Java (OpenJDK).
  - YL - If there is an issue will need to migrate to versions of OpenAM., i.e. need to be ready to do this.
  - MG - We’ve using OpenJDK 8 and this working ok with 3.14.8.
  - SO - requesting that authentication of user is required and there is a cost involved. So, if something simpler is acceptable, is SSO needed?
  - JT - Is anyone needing to authenticate credentials for another GISC?
  - ALL - no.

  RES-OWIS DECISION - Recommend to the SC via the TC to keep OpenWIS licence free as a proposal.

  - MG - There is a way to keep SSO feature in OpenWIS and use another method, as ZZ suggested, e.g. via Spring Framework
  - JA - can we do both, i.e. Keep OpenWIS free form payments and adopt Spring framework when there is a need for SSO?
  - SO - go for simplicity
  - JT/MG - discussed various aspects and options of SSO and use of frameworks
  - RGr - another perspective is which is the cheaper option, remove SSO feature and adopt Spring when needed.
  - JT - It can happen, such as with Apache.
  - MG - the heaviest lifting is handling SAML2 in the portal is the greatest task. Cutting out SAML will be the most expensive.
  - ZZ - Portal relies on Tomcat which has its own security features, so this is an option. Could also use a more complicated option is to use picket link with Tomcat.
  - MG - this could be a cheaper option.
  - LL - What about Identify or Wren?
  - MG and ZZ - not familiar with these could investigate these.
  - JT - from UKMO being restricted to a single Tomcat domain is a little too restrictive. Need a centralised authentication provider.
  - MG - What is the domain article in Picketlink mean/referring to? A URL? Look at Spring and Picketlink.

  *SUMMARY*
  - SO - accepting that the strategy to remove dependency from Foregrock (which will need some effort that OpenWIS funds could be used for)
  - JT - Assuming that Met Office is using SAML2 to talk to LDAP so will not work for Met Office.
  - MG - Our apps have to use SAML2. However, if using the SP approach. There could be an option to use LDAP or not.
  - SO - looking at longevity and being and having the flexibility to upgrade, i.e. having a simpler model makes it easier to maintain for next 5 years.
  - RGb - does this mean having the ability to plug in difference LDAPs?
  - JT - Yes.
  - BS - Is this Ok for UKMO?,
  - JT - Yes, this will authentication from a separate service.
  - ZZ - Is SSO featured only in the portal?
  - MG - I believe so, the backend data service is already protected source.
  - ZZ - So why not put two portals in one? Container?
  - MG - Didn’t see a convenient way to do this. But it may be possible. May be possible to put into one container.
  - ZZ - If we consider a simpler approach such as LDAP, we may want to put the Admin and User Portal into a single Tomcat container.
  - JT - Summary Forgerock – out. How much simplicity – rely on Tomcat auth.
  - YL - Spring has libraries that will need to be integrated into existing libraries in the portal.
  - JT - A suitable replacements for OpenAM and OpenDJ need to be identified. Can MFI and NWS do this? The scope of options SAML2.0. Direct LDAP integration, and in-container authentication (e.g. Tomcat or Apache).
  - LL and SO - this is possible.
  - JT - UKMO can validate options identified.
  - All- Agreed.

  *[ACTION - SO and LL assess suitable replacement parts for OpenAM and OpenDJ by exploring options. UKMO will like to validate the options](https://github.com/OpenWIS/openwis-documentation/issues/536)*

  - JT - MF have worked through containerisation and identified difficulties with OpenDJ, OpenAM, and the database.
  - JT- to confirm, this work can restart once Forgerock aspects are removed.
  - SS - database and content will need to be deployed separately and connected, but this should be the only external not outside the container

  *[ACTION – BS and SS Resume work on containerisation once work on removing OpenWIX 3x Forgerock dependency is complete}(https://github.com/OpenWIS/openwis-documentation/issues/537)*

  Other EOL

  - ZZ - in reference to doc [insert link]:
    - Java8 - Tested Java8 successfully. Java8 is supported until 2025. Recommendation is stay with Java8
    - Wildfly8 - tested and gets better with each version.
  - ZZ – The recommendation is to go with Wildfly 15. Suggest go with Sol7. Postgres 11
  - All- agreed

  RES-OWIS DECISION - Adopt Wildfly 15, Sol7 and Postgres 11.

  Dependencies

  - ZZ - ref. to doc. [insert link] analysis done using MAVEN. Majority of dependency analysis done.
  - MG - Upgrade to Geo-network is important, so would be good to do, but likely to be resource intensive.
  - JT - Looking all versions, no need to upgrade to the latest version. To decide, there is a need to assess whether a security issue exists and then only upgrade to the version that resolves a security issue.
  - All - agreed.

  RES-OWIS DECISION - Only upgrade to the latest version if a security vulnerability exists and upgrade to the relevant version that resolves the security issue.

  RES-OWIS DECISION – Recommend to TC to ensure that the dependency list is updated regularly.

  *ACTIONS –
  [JT to review security issues with current version 3.14.8.](https://github.com/OpenWIS/openwis-documentation/issues/538)
  [SO to establish with repos are current using the current dependency list](https://github.com/OpenWIS/openwis-documentation/issues/538)
  [SO and BS (i.e. TC) to ensure that the dependency list is regularly updated](https://github.com/OpenWIS/openwis-documentation/issues/538)*

*5. WIS 2 Prototype Studies*
  5.1 Metadata formats –
  - JT- updated the work in train by the INSPIRE community here - https://webgate.ec.europa.eu/fpfis/wikis/display/InspireMIG/Workshop+on+making+spatial+data+discoverable+through+mainstream+search+engines+-+Call+for+abstracts. This provides an opportunity to OpenWIS members to participate as JT unable to attend.
  - BS - Feedback from this event will provide useful information for TT-WIS.

  5.2 Progress
  - DP - Updated on pub sub WIS2 prototype. Key points - ‘Can help in WIS2 can provide data exchange between different services?’ The standards that are relevant are AMQP and MQTT as there are ISO compliant.
  - SO - Do they support broker services, too?
  - DP - Yes. A broker provides a service to enable pub and sub. RabbitMQ provides support for service implementation. RabbitMQ supports several message queue protocols and AMQP extensions.
  - BS - is RabbitMQ ready for the next version of AMQP?
  - DP - Don’t know, however, it works with AMQP 0-9-1. RabbitMQ enables testing and re run tests easily.
  - SO - Are you investing the optimum number of queues?
  - BS - is it a very mature protocol?
  - DP - Very mature, a lot of on-line banks use it.
  - MV - We have been using it for an out-station for a number of years.
  - JT - CMA use it to manage data inflow from c5,000 sites operationally.
  - RGr - AQMTT will have new features soon and will merge with AMQP.
  - DP - Producers, clients. In the middle AQMP manages data exchanges between queues and subscriptions via RabbitMQ. RabbitMQ is very stable but will crash if memory limits are reached.
  - DP - Unlike FTP, where Apache reads the and doesn’t load it into memory, AMQP loads the file into memory.
  - SO - Do messages persist indefinitely? Or is re-subscription?
  - DP - A queue stops when no longer needed. However, can set up to be ‘durable’/’persistent’.
  - DP - There is also no way to send a message ‘while you are away’.
  - SO - What set of operations are allowed (such as Pause ‘re-send)?
  - DP - You log in and can set options.
  - BS - Can you set priority
  - DP - Its FIFO. A disadvantage is that AMQP is doesn’t work well queues are not working.
  - BS - So if your telecoms are not reliable, like African countries, will latency?
  - DP - Can work with bulk send, so good for low bandwidth. Have done a lot of testing with low bandwidth and works better than FTP.
  - BS - So if you stop and start with gaps will the queue can stop?
  - DP - Can be configured for up to 24-hour gaps. But remember FIFO.
  - JT - So client software needs to be aware of FIFO.
  - DP - If no bindings on a queue, then message is discarded.
  - DP - 4 types of off-routing. There is a key when you send a message up to 255bytes. Direct exchange sends on key match – Fan out – all messages received will be received by all clients – most efficient and predictable.
  - BS - Good tor GISC Caches updates.
  - DP - Topic exchange – based on key word, such as ‘model’.
  - BS - Does not work with a catalogue.
  - DP - Normally needed to generate a list.
  - DP - Header exchange. Routing on headers, payloads. Bigger overhead for RabbitMQ.
  - JT - How does the key get created?
  - DP - By text, user generated.
  - RGr - for the transition.
  - MG - Does the text support Unicode?
  - DP - No.
  - DP - for testing, we used lazy queues which means that all queues are written to disk. Which is recommended in a production environment as the response time is predictable. We also made all queues persistent. Pre-fetch tuning by experimenting– where high latency exists.
  - DP - Can have more than client on a queue and decide which message is sent to which client.
  - LL - A kind of load balancing.
  - BS - when you say a few kilobits. What are the limits? On GTS the message is already bigger.
  - RGr - doesn’t matter as the message is not downloaded.
  - DP - Experiment to manage to make best use of memory (RAM) by using ARIA2.
  - DP - Tests with Canada. Refer to page 15 to 19 on slides
  - ZZ- How do you ensure transactions on each node is successful?
  - DP - HTTP is updated first and then RabbitMQ.
  - RGr - The architecture is important.
  - JT - How do you deal with a node that becomes inconsistent? Kill it?
  - RGr - aim to have architecture that works in WMO. Implementation options vs standardisation.
  - JT - if there are 15 centres will all need to be meshed together?
  - RGr - Only 3 to 4 need to be meshed. At some stage will need to define guidelines. At present it’s a good enough architecture to enable learning and centres who participate are volunteers.
  - BS - In a scenario where the GTS is shared. As a client do I subscribe? Do I need to configure my client to all nodes?
  - DP - You will need to decide to how many nodes you connect to.
  - DP - Test results. See slide no.20 and 21
  - DP - Milestones in reference to Project Charter – see slide 22
  - ZZ - Federation, benefits?
  - DP - Concept on AMQP level. When a WMO message is sent it’s like a federation. It’s a native to replicate with RabbitMQ.
  - ZZ- how much benefit if cluster offers redundancy.
  - BS/RGr -a potential for redundancy in a scenario when all centres are meshed. But we know that all centres will not do this due to the strong binding needed between centres. Therefore, this provides an option.
  - DP - Future steps See slide page 23.
  - SO - how much of this work consistent with W3C and OGC’s approach?
  - JT - WSC recognise this as message distribution channel and have their own which is aimed at updating web sites. Key point here is that HTTP Is being used to transfer data and message protocols.
  - MG - Can the SAML2 token be included to prevent abuse of downloads?
  - SO - Security aspects are for of the pending aspects of the AMQP work.
  - RGr - more range of partners planned for later in 2019 but focus before that is on the Canada study/test. Aviation industry is working on an AMQP type of solution, for example, Euro Control.
  - BS - what happens notifications.
  - JT - The data is not downloaded and managed by software that can automate infrastructure use (i.e. cloud).
  - BS - what work is needed for client software.
  - RGr - only small amount of coding is needed (c10 lines of Python) which can be provided by the RTH.
  - BS - If I want to get GTS data, do I connect to 10 centres or one specific centre?
  - RGr - The idea is that a broker exists that knows all the data. So, can decide a client subscribe to 2   to3 centres for redundancy. We need to define a mechanism, decide for a small number of sites to be a global broker. A decision over the next 2 to 3 years.
  - JT - Specifying an alert. I may decide to publish for my internal needs and have a specific notification need for that. So, by having more than one node can have different rules internally and externally for example.
  - RGr - a lot of things are possible, mixing design and implementation decisions is a challenge.
  - 2.3 Opportunities to demo
  - SO - what are the opportunities?
  - JT - WMO Congress reform – services and an infrastructure commission. CBS will not exist, assuming it is voted through. In first year existing plans will stay live. The new technical commissions will be commencing a year later. A key thing is that regions and members are to be involved so that there is an understanding of implementation.
  - BB - Regional reform will the focus and underpinning theme, likely to start in January 2020.
  - JT - So, in terms of marketing there will not be a TECO or a CBS TECO. So, we need to keep a watch on the developments.
  - SO - Is the expectations for ET and TT to fall under the two umbrellas?
  - JT - Initially, yes. But there are a lot of ET and TT, so there are duplications. WIS2 is about the adoption of technologies rather than using novel and new technologies.
  RGr - So, we don’t know but some ET and TTs are more at risk than others.

  RES-OWIS DECISION - agreed that not a lot to be done until clarity emerges. However, we can continue to influence as part of existing WMO roles.

6. **Outstanding Actions**
  - SO demonstrated a number of updates to actions that relate to the web site, including Code of Conduct, Quality, Coding guidance, Pages for each WIS2 projects, Release Management.
  - SO - also led the discussion to update actions assigned to PMC, i.e. from this list https://github.com/OpenWIS/openwis-documentation/issues?q=is%3Aopen+is%3Aissue+label%3A%22Project+Mgt+Committee%22

  RES-OWIS DECISION – agreed for these to published to the Association web-site as soon as possible.

7. **Close and summary**
  - No other business.
