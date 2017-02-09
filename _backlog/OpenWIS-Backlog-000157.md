---
layout: backlog
title: Remove FTPReplication Tool
kanCategory: backlog
kanSubCategory: 
kanAssigned:
kanBacklog: 157
kanIssue: 105
kanPullReq:
kanFeature: Quality software
kanRelease: 5
kanMetric: 2
kanSize: 1
kanPriority: 10
kanRepo: OpenWIS/openwis
---

Deferred until OpenWIS 4

This is to fix issue #105.  See issue #106

As part of this fix, only the actual FTP replication tool is removed. Nothing in the data services have been changed, which means that the "fromReplication" directories can still be used.
