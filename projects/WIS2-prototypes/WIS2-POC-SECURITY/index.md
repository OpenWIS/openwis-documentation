---
layout: page
title: WIS2 Project Charter for Security investigation
wis2Owner: WIS2-POC-SECURITY
---

# Aim

As the WMO and draft WIS 2.0 technical specification contemplates a move to an open internet-based connection for great public access and retrieval of DAR data, this charter defines the security measures needed to preserve the Confidentiality, Integrity and Availability of existing and new DAR data as well as a simple, secure pub/sub method to disseminate it.

There are a number of technologies and techniques that could be used to disseminate DAR data in a pub/sub manner.  We’re looking for a contractor to conduct an Analysis of Alternatives (AoA) and make recommendations on what is the most efficient and effective publication/subscription approach.

# Scope

1. Define and confirm actors participating in WIS content distribution
 - An actor is a person or other entity, external to the system being specified, who interacts with the system (includes the actor that will be initiating this Use Case and any other actors who will participate in completing the Use Case). Different actors often correspond to different user classes, or roles, identified from the customer community that will use the product. The OpenWIS Association envisions three distinct groups of actors:
2. Analyze methods for promoting public dissemination of WIS content
  - Assuming three distinct groups of actors, the OpenWIS Association envisions supporting two distinct dissemination use cases (trusted and untrusted).   The distinguishing feature here is that the trusted category is a vetted member that has come to some formal agreement prior to being granted membership.  
  - For the Trusted GISC Member, the technical details of the dissemination protocol can be a negotiated issue reserved for the vetting process.  Either an exact specification that new members must implement or else a range of technical options that can be negotiated.  Furthermore, the trusted Member has publication authority granted by virtue of the new members consent to the rules of conduct.   
  - The Identified Public Content Consumer category represents the general public where some form of authentication using open standards, oAuth or  OpenID, provides a mechanism for identifying the actor.  Here there is no vetting process, but the identity of the actor provides a means to control behavior allowing subscription services to be measured and controlled. 
  - The Anonymous Public Content Consumer category represents the general public where the dissemination would require the use of open standards such as Search Engines, RSS Syndications, Atom Feeds [..other]   Anonymous public access has no vetting process and no identifying attributes where constraints on behavior and service utilization can be controlled so only Ad-Hoc, user initiated dissemination implementations that can limit service utilization would be appropriate.
  - For the trusted member, the technical details of the dissemination protocol can be a negotiated issue reserved for the vetting process.  Either an exact specification that new members must implement or else a range of technical options that can be negotiated.  Furthermore, the trusted Member has publication authority granted by virtue of the new members consent to the rules of conduct.   
  - The untrusted Content Consumer category represents the general public where the dissemination would require the use of open standards such as Search Engines, RSS Syndications, [...others].   Public access has no vetting process where constraints on behavior or protocol implementations can be negotiated.
 
The contractor should analyze and assess a variety of options for promoting public dissemination of WIS content.  An outcome from this evaluation should be the recommended approach.
3. Analyze ways to secure the interaction between WIS providers and consumers

For the Trusted group, the vetting process becomes the point of interest in erecting the trust model and establishing the service level for the dissemination.  The OpenWIS Association envisions:
 
1.      Establish chain of trust with central authority: OpenWIS Consortium
2.      Obtain consent of the members to adhere to the rules of conduct
3.      Establish service level agreements between members.
4.      Establish/Publish technology/software stack for trusted dissemination
 
The OpenWIS Association envisions the following Publication and Subscription Operations Requirements for Trusted Members:
 
1.      Add/Delete/Manage Message Queue
2.      Member utilization / quota
3.      PKI Certificate Management: Create/Revoke
 
For the public group, the commercial authentication platforms such as Google or Facebook allow for a limited framework of trust to be established, enough to support content subscription but probably not content publication.   Here, with the identity of the new untrusted member established by the authentication platform, subscriptions could be established and quotas controlled.   However the dissemination protocols would need to be common open standards.
 
The OpenWIS Association envisions Public (untrusted member ) Authenticated Subscription Operations requirements:
 
1.      Subscribe/Unsubscribe: Atom, RSS
2.      Support for Member utilization quotas:
3.      PKI Certificate: Authentication Platform PKI or SAML
 
Finally, the anonymous untrusted public would probably not be a welcomed member to the subscription service.   Since no single identification token is available, there is no mechanism to enforce a quota.  Anonymous public access is more suitable to use cases where utilization quotas are not an issue and discovery and dissemination issues are paramount, changing the focus from Subscription to Discovery and Search.  The OpenWIS Association would strongly encourage untrusted public actors to become untrusted members.  
 
Untrusted Public Actors and requirements support:

Untrusted public actors have no relationship to the organization and have no claim to any form support, however the larger goal of promoting public dissemination and discovery of WIS content addresses this group of actors.   Anonymous public search and discovery of WIS content is best implemented by integration with leading search platforms.   The anonymous public lacks any vetting process and is without identifying attributes where constraints on behavior and service utilization can be controlled.   Therefore only Ad-Hoc, user initiated interactions with the service that are designed to limit utilization would be appropriate.
 
The contractor should analyze and assess the pros and cons of different ways to secure the interaction between WIS providers and anonymous consumers.  An outcome from this evaluation should be the recommended approach for the interaction by actor as well as supported operations by actor.
 
1.  	Untrusted Public
Untrusted public actors are anonymous content consumers.  Untrusted public are individuals and/or organizations just interested in discovering, and potentially in the retrieval of metadata and data.
 
2.  	Untrusted Members
Untrusted members actors that are identified but un-vetted content consumers.  Untrusted members are individuals and/or organizations outside of DCPCs/NCs/GISCs that want to consume data and metadata
 
3.  	Trusted GISC Members
Trusted GISC members are fully vetted and trusted content publishers.
 
The contractor should analyze and assess if this is the correct set of actors, and tie what each of the actors can/cannot do with respect to retrieval of DAR information.  An outcome from this evaluation should be the recommended set of actors.
4. Analyze ways to ensure these secure interactions between WIS providers and consumers are simple
  -Recommended pub/sub approach and protocol must also serve as message broker, able to speak/translate all protocols.
  - Recommended pub/sub approach must address the right sizing of a total number of queues to implement at GISCs giving the broad spectrum of weather data and products supported today.  Goal must not be to overly complicate this or inhibit performance due to an insufficient amount of queues.
  - Recommended pub/sub approach should factor in ability to support vulnerability patching and subsequent version builds.
  - Recommended pub/sub approach should be easy to implement and be light weight for system administrators
  - Recommended pub/sub approach should take into account data provider environment:  Mostly mission critical, 24x7 operational Met Centers
  - Recommended pub/sub approach should  be easy for trusted members, untrusted members to implement.  Goal is not to discourage use of GISCs by consumers!
 
The contractor should analyze and assess the pros and cons of how these secure interactions between WIS providers and consumers are simple and not complex.  The above bullets are suggested guidelines for doing this analysis of alternatives.  An outcome from this evaluation should be the recommended approach for these simple, secure interactions.

# Deliverables


# Sponsor and funding source

This project will be funded by OpenWIS Association.

# Milestones and Schedule

|  Project Milestone  |  Begin Date  |  End Date  |
|  -----------------  |  ----------  |  --------  |
|  Define and confirm actors participating in WIS content distribution  |  TBD   |  One month after contract start up   |
|  Analyze various methods for promoting public dissemination of WIS content  |  TBD   |  Two  months after contract start  up   |
|  Analyze ways to secure the interaction between WIS providers and consumers  |  TBD   |  Four months after contract start up   |
|  Analyze ways to ensure these secure interactions between WIS providers and consumers are simple  |  TBD   |  Five months after contract start  up   |
|  Generate report on recommend approach  |  TBD   |  Six months after contract start  up   |
| |||
|  Project Closure  |||
|    |    |    |

# Roles and Responsbilities

|  Resource Name  |  Organization  |  Role  |  What this person will be do in relation to a milestone  |  Time period needed for resource  |
| Steve Olson  |  National Weather Service (NWS)   |  Co-lead WIS 2.0 Security PoC   |  Chair of TC, Technical lead for WIS 2.0 Security PoC   |  2019-2020   |
| Marc Giannoni  |  National Weather Service (NWS)   |  Co-lead WIS 2.0 Security PoC   |  Chair of TC, Technical lead for WIS 2.0 Security PoC   |  2019-2020   |

# Communication and Reporting

State the communication and reporting arrangements for interactions with:

Regular update to the Steering Committee 

# Configuration Management Process

 - State how any of artefacts needed for each of the deliverables will be managed, referring to the relevant rules and rules supplements of the OpenWIS Association.
