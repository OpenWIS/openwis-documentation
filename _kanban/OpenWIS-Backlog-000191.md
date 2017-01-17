---
layout: backlog
title: v4 - Improve the development process
kanCategory: analyse
kanSubCategory: in-progress
kanAssigned: UKMO
kanBacklog: 191
kanIssue:
kanPullReq:
kanFeature: Good documentation
kanRelease: 4
kanMetric: 8.3
kanSize: 5
kanPriority: 1
kanRepo: OpenWIS/openwis-documentation
kanProject:
---
Clarify and document the development process so that the remote teams can work together more effectively on version 4.

---
[development process][DP]


# The Development Lifecycle of OpenWIS Core version 4
The purpose of the next top-level development cycle of the OpenWIS Core Project is to deliver the next major upgrade to the OpenWIS core software, version 4 (OpenWIS4), in a form that is suitable both for release as an open source package and for operational deployments to GISCs, DCPCs and NCs around the global WIS network.

The development lifecycle consists of 5 main cycle stages, most of which are themselves cyclic in nature:

- Gather the requirements
- Define the solution
- Develop the software components
- Integrate the software components
- Release the software packages

The development lifecycle is not linear, it iterates through these stages a number of times until the purpose is achieved.  Also, there are lower level, agile, cycles within each of these stages, as well as parallel running of some activities.  So, for example, we could be releasing a version 4.1.1 (development release) while we are already developing software components for version 4.1.2 and also refining requirements for version 4.1.3.

## Gather the requirements
We are not building OpenWIS4 from scratch; it will be derived from 2 key products that already exist:

- OpenWIS v3.14, and
- GeoNetwork v3.2

We have already developed some code for OpenWIS4, based on a gap analysis between OpenWIS v3,  GeoNetwork v2.6 and GeoNetwork v3. We have combined this code with GeoNetwork v3.2 and released this as OpenWIS v4.0, which we will use as a test and demonstration system to further refine the requirements for OpenWIS4.  The intention is to iterate through a number of development releases of OpenWIS4 (v4.1.1, v4.1.2... v4.1.x) until we have a production ready version, OpenWIS v4.2.  The way this code has been integrated (thanks to European Dynamics) is also very important, because it uses a set of design patterns that we intend to use going forward for all integrations between OpenWIS and GeoNetworks.  These patterns make it possible to develop OpenWIS as plug-ins to GeoNetwork and frees us from many of the complexities and constraints of working directly in the GeoNetwork code or our forks of it.

So our list of requirements will come from:

- our combined assessments of what we should and shouldn’t use GeoNetwork 3.2 for in OpenWIS
- our original requirements for OpenWIS, which we can think of as WIS 1.0 compliance
- new requirements from emerging thinking on WIS 2.0, including cache-in-the-cloud, better metadata modelling etc
- existing bugs and issues with OpenWIS v3
- security accreditation issues
- new features or improvements to existing functions or the UX

We want these requirements to be in a single list (in the Backlog or linked to from there) and contain sufficient detail for discussions of the relative priority of each; but they don’t have to be in fine detail until we decide we will actually develop them, or, even better, we develop comprehensive tests for them rather than detailed specifications. Note that we will require entries for those features of GeoNetwork we intend to adopt, because, even though we might not have to develop any code, we will have to develop tests to demonstrate that these features, or the way we have integrated them with OpenWIS4 code, do exactly what we want.

## Define the solution
Once we have the Backlog, we need to agree the priority order of the requirements.  Some requirements will be linked, functionally or technically, so it will be necessary to agree a technical design and feature list to have a sensible discussion about priorities.  Some aspects of the design will also imply a specific development sequence for some interdependent features, so we should make that explicit too.  A well defined feature list and development sequence will also make the allocation of agile development tasks to teams more manageable later. After the first iteration, we will just need to update these documents. Once the first iteration of these documents have been reviewed and agreed by the TC and SC, we will transfer the tasks for our first development release to the Kanban board category ‘analyse and write tests’. We will then assign feature owners to each, to assist the developers with refining the requirements/features and designing acceptance tests for each feature. Where practicable, we will automate these tests so that they can be easily rerun and incorporated into the CI, though some tests will necessarily be manual.

As we refine the features, we will decide whether the Kanban items and/or GitHub issues are adequate to describe the tasks for the development team; if not, we will set up a project in GitHub to manage the work.

Feature owners will regularly review and test the outputs from the development team as they develop the features.  

### OpenWIS4

### Purpose
To deliver the next major upgrade to the OpenWIS core software, in a form that is suitable both for release as an open source package and for operational deployments to GISCs, DCPCs and NCs around the global WIS network.

*Composition:* A description of the major sub-products to be delivered by the project, for example the major features or epics.

*Derivation:* The source products from which this product is derived, for example:

  - Existing products to be modified
  - Design specifications
  - A feasibility report
  - A project mandate

*Development skills required:* The skills required to develop the products or areas that should supply the development resources.

*Customer's quality expectations:* A description of the quality expected of the project's product and the standards and processes that will be applied to achieve that quality.  They will impact on every part of the product development and thus on time and cost.   The quality expectations are captured in discussion with the Customer and should be prioritized.

*Acceptance criteria:* A prioritized list of criteria that the project product must meet before the Customer will accept it.  That is, measurable definitions of the attributes the product must have to be acceptable to the key stakeholders, in particular, the Users and the Operations and Maintenance organisations.  For example: ease of use, ease of support, ease of maintenance, appearance, major functions, development costs, running costs, capacity, availability, reliability, security, accuracy or performance.

*Project-level quality tolerances:* Tolerances that apply to the acceptance criteria.

*Acceptance method:* The means by which acceptance will be confirmed.  May simply be a case of confirming all the project's products are approved or may involve complex handover arrangements, including any phased handover.

*Acceptance responsibilities:* Define who will be responsible for approvals and acceptance.

---

### Project Product Description

#### Purpose:
The Project Product Description defines what the project must do to gain acceptance; it is the 'Definition of Done' for the entire project.

#### Composition:
*Title:* Name by which the project is known.

*Purpose:* Defines the purpose that the project's product will fulfil and who will use it.  Helpful in understanding the product's functions, size, quality, complexity, robustness, etc.  It should focus on the outcomes and benefits of the project, not describe a solution.

*Composition:* A description of the major sub-products to be delivered by the project, for example the major features or epics.

*Derivation:* The source products from which this product is derived, for example:

  - Existing products to be modified
  - Design specifications
  - A feasibility report
  - A project mandate

*Development skills required:* The skills required to develop the products or areas that should supply the development resources.

*Customer's quality expectations:* A description of the quality expected of the project's product and the standards and processes that will be applied to achieve that quality.  They will impact on every part of the product development and thus on time and cost.   The quality expectations are captured in discussion with the Customer and should be prioritized.

*Acceptance criteria:* A prioritized list of criteria that the project product must meet before the Customer will accept it.  That is, measurable definitions of the attributes the product must have to be acceptable to the key stakeholders, in particular, the Users and the Operations and Maintenance organisations.  For example: ease of use, ease of support, ease of maintenance, appearance, major functions, development costs, running costs, capacity, availability, reliability, security, accuracy or performance.

*Project-level quality tolerances:* Tolerances that apply to the acceptance criteria.

*Acceptance method:* The means by which acceptance will be confirmed.  May simply be a case of confirming all the project's products are approved or may involve complex handover arrangements, including any phased handover.

*Acceptance responsibilities:* Define who will be responsible for approvals and acceptance.

---

## Backlog to Kanban

---

## Allocating Work

---

## Integration

---

## Release

---

[DP]: {{ site.baseurl | prepend: site.url }}/assets/OpenWIS4-development-process.svg
