---
layout: backlog
title: Fix Code Repositories
kanCategory: analyse
kanSubCategory: pending
kanAssigned:
kanBacklog: 167
kanIssue: 
kanPullReq:
kanFeature: Good development processes
kanRelease: 4.1
kanMetric: 4.2
kanSize:
kanPriority: 7
kanRepo: OpenWIS/openwis
---
At the moment, the OpenWIS and Core GeoNetwork (with OpenWIS mods) is in separate repositories.
This makes it difficult to test the new GeoNetworks with the data/management services within a single
Vagrant setup.  Also, mixing our changes with GeoNetworks is fragile and should be separated as
soon as we can.

We will need to clean this up to make this possible.

Some Ideas:

- Move the OpenWIS extensions out of the core-geonetworks repository, maybe back into the 'geonetworks-extension' repository.
- Add core-geonetworks as a git submodule into the geonetworks-extension repository.
- Add the geonetworks-extension into the OpenWIS repository as a git submodule.

That way, we can track changes separately if we need to, but we will be able to setup a single Vagrant environment
from the OpenWIS repository easily.

An alternative structure is if we just moved the geonetwork-extensions code back into the OpenWIS repository
and add core-geonetworks as a direct git submodule to OpenWIS.
