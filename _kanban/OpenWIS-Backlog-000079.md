---
layout: backlog
title: DDS4 Direct download via HTTP
kanCategory: analyse
kanSubCategory: pending
kanAssigned: UKMO
kanBacklog: 79
kanIssue:
kanPullReq:
kanFeature: Integrated catalogue
kanRelease: 4.2
kanMetric: 5.2
kanSize: 5
kanPriority: 4
kanRepo:
kanProject:
---
Enhancement DDS4: Direct download via HTTP

This task was part of the OpenWISv4/GeoNetworksv3 [work package][WP] assigned to GeoCat in 2015.  The [documentation][doc] produced as part of that work describes the new functionality delivered.

[WP]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Workpackage.pdf
[doc]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Documentation.pdf

The outcome for this feature was:

2015 status: **MO Test**; Percent complete: **60**; Priority: Normal; Questions outstanding: 100% OR 60% Done?;

Extra info:

GeoNetwork shall be amended such that a user with the appropriate permissions may download data product instances that are currently available from the OpenWIS Data Service directly from the portal via HTTP.

The portal will provide a web-based user interface enabling a user to configure their download request for the specified dataset; allowing them to select specific data product instances from the currently available setError: Reference source not found and specify how these are to be packaged for download (e.g. as a single compressed file, or concatenated according to a WMO-specified scheme).
Direct downloads are then processed identically to ad-hoc requests; the portal will package the user supplied information and the relevant product metadata record (retrieved via the ProductMetadataService SOAP web-service) into an ad-hoc request object and send it for validation and processing to the OpenWIS Data Service using the createRequest operation from the RequestService SOAP web-service.

Note that by re-using the existing services for ad-hoc requests, all the necessary usage statistics and download history are automatically gathered for that user. The absence of dissemination information within the request object means that no further action will be taken within the OpenWIS Data Service once the data products have been extracted, packaged and moved to the Staging Post.

The asynchronous nature of the ad-hoc request process means that it is not straightforward to determine when the packaged data products have been moved to the Staging Post ready for download. For the purposes of this technical design the monitorExtraction operation of the ProcessedRequestService SOAP web service can be used to poll for completion.
Once the ad-hoc request process has completed, the portal will be updated to provide a hyperlink to the location of the packaged data products within the Staging Post. The URL is determined by concatenating the Staging Post URL (retrieved from configuration) and the URI for the data product package (retrieved using the getUri() operation on the processed request object returned from the getProcessedRequest or getProcessedRequestForAdhoc operations from the ProcessedRequestService SOAP web-service).The user is then able to download the packaged data products.

_OpenWIS shall notify the relevant Groups that the dataset has been downloaded according to the notify permission defined for the metadata record associated with the downloaded dataset._
