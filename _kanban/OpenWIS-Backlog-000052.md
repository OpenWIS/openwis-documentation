---
layout: backlog
title: MM4 Maintain product metadata table
kanCategory: analyse
kanSubCategory: pending
kanAssigned: UKMO
kanBacklog: 52
kanIssue:
kanPullReq:
kanFeature: Integrated catalogue
kanRelease: 4.0
kanMetric: 6.1
kanSize: 3
kanPriority: 4
kanRepo:
kanProject:
---
Enhancement MM4: Maintain product metadata table.

Update - scrum - 2016-11-17: GT - Not mentioned re new v4.0 as part of Kanban 81. v4 - Refactoring to improve modularity.
PR - Ask GT if he is aware of this one.

---


This task was part of the OpenWISv4/GeoNetworksv3 [work package][WP] assigned to GeoCat in 2015.  The [documentation][doc] produced as part of that work describes the new functionality delivered.

[WP]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Workpackage.pdf
[doc]: {{ site.baseurl | prepend: site.url }}/assets/OpenWISv4-GeoNetwork-2015-Documentation.pdf

The outcome for this feature was:

2015 status: **MO/GeoCat Review**; Percent complete: **0**; Priority: High; Questions outstanding: 0% Done? There is a conversation with Jeremy and Leon in Redmine, but not sure how it concluded;

Extra info:

This enhancement is to be implemented as a complementary component to GeoNetwork as the functionality described herein is specific to OpenWIS. Implementation of this enhancement should be loosely coupled with the GeoNetwork code base enabling the source code for this enhancement to be maintained independently. It is highly desirable to be able to bind the capabilities described by this enhancement within GeoNetwork using deployment-time configuration rather than at compilation-time.

The OpenWIS Data Service holds a summary record for each metadata record in the catalogue. This information is stored in the Product Metadata Table and drives the processing of the Data Service on arrival and dissemination of data product instances.

The definition of the summary record, expressed as a complex type within XML Schema, is provided below:
<xs:complexType name="productMetadata">
<xs:sequence>
<xs:element minOccurs="0" name="id" type="xs:long"/>
...
<xs:element minOccurs="0" name="stopGap" type="xs:boolean"/>
</xs:sequence>
</xs:complexType>

Information for the summary record is located within the main metadata record according to XPath statements.

When a new metadata record is added to the OpenWIS catalogue, a corresponding entry in the Product Metadata Table shall be added using the createProductMetadata operation of the ProductMetadataService SOAP web service.

When an existing metadata record is updated within the OpenWIS catalogue, the corresponding entry in the Product Metadata Table shall be updated using the updateProductMetadata operation of the ProductMetadataService SOAP web service.

When an existing metadata record is deleted within the OpenWIS catalogue, the corresponding entry in the Product Metadata Table shall be removed using the deleteProductMetadata, deleteProductMetdataByURN or deleteProductMetadatasWithURN operations of the ProductMetadataService SOAP web service. The latter operation provides for bulk removal.

Note that the obsoleting of subscriptions associated with a deleted metadata record is undertaken by the OpenWIS Data Service.
