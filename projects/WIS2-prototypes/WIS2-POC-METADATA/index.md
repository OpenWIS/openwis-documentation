---
layout: page
title: WIS2 Project Charter for METADATA investigation
wis2Owner: WIS2-POC-METADATA
---

# Aim

Gain answers to the following:

Can new message queue protocols such as AMQP, MQTT & STOMP address weather data dissemination issues?

In particular, is AMQP (Eurocontrol’s choice) the ideal candidate for other weather wata exchanges
   - would this be a long term solution?
   - how could Message Queue protocol coexist with existing FTP based WIS?

The buiness case is to offer the possibility for internet users to access WIS data cache using publish/subscribe mechanism

# Scope

Proof of concept covering:
 - Pub/sub on 24h cache data, providing data through FTP, getting data through AMQP
 - Pub/sub on French global model (Arpege) , getting link through AMQP (large files demonstration):
   - with direct AMQP dissemination
   - with AMQP “availability” dissemination providing the customers information that data is ready for downloading (possibly using “metalink” files)
 - Pub/sub over an AMQP Cluster (Several nodes in a single location to provide High Availability & High throughput)
 - Pub/sub over an AMQP Federation (Different clusters separated by possibly lossy and high latency WAN links)

# Deliverables

 - Security aspects (use of TLS, messages signatures, certificates)
 - Potential SLAs
 - Candidate architecture how AMQP could coexist with FTP/SFTP based data exchanges

# Sponsor and funding source

This project will be exclusively funded by in kind contribution. No funding is required from the Association. The sponsor is Méteo France.

# Milestones and Schedule

|  Project Milestone  |  Begin Date  |  End Date  |
|  -----------------  |  ----------  |  --------  |
|  Deliverable 1 milestones  |    |    |
|  Deliverable 2 milestones  |    |    |
|  Deliverable 3 milestones  |    |    |
|  Deliverable 4 milestones  |    |    |
|  Deliverable 5 milestones  |    |    |
| |||
|  Project Closure  |||
|    |    |    |

# Roles and Responsbilities

|  Resource Name  |  Organization  |  Role  |  What this person will be do in relation to a milestone  |  Time period needed for resource  |
| David Podeur  | Météo France   |  Project Manager   |  Co-ordination and support acheiving deliverables   |  August 2018 to June 2019   |
| Steve Olson  |  National Weather Service (NWS)   |  TBD   |  TBD   |  TBD   |

# Communication and Reporting

State the communication and reporting arrangements for interactions with:

Regular update to the Steering Committee 

# Configuration Management Process

 - State how any of artefacts needed for each of the deliverables will be managed, referring to the relevant rules and rules supplements of the OpenWIS Association.
