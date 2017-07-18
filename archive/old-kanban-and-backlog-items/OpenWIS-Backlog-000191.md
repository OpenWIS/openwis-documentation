---
layout: backlog
title: v4 COM - Improve the development process
kanCategory: analyse
kanSubCategory: in-progress
kanAssigned: UKMO
kanBacklog: 191
kanIssue:
kanPullReq:
kanFeature: Community
kanRelease: 4
kanMetric: 8.1
kanSize: 5
kanPriority: 2
kanRepo: OpenWIS/openwis-documentation
kanProject:
---
Clarify and document the development process so that the remote teams can work together more effectively on version 4.

---
Link to [development process][DP] diagram.


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

We will gather these requirements into a single list, in the Backlog or linked to from there.  They will contain different levels of detail, from detailed bug descriptions in GitHub issues, to high level users stories from WIS 2.0 (epics). Note that we will require entries for those features of GeoNetwork we intend to adopt, because, even though we might not have to develop any code, we will have to develop tests to demonstrate that these features, or the way we have integrated them with OpenWIS4 code, do exactly what we want.

## Define the solution
Once we have the Backlog, we need to agree the priority order of the requirements.  Some requirements will be linked, functionally or technically, so it will be necessary to agree a **technical design** and **feature list** to have a sensible discussion about priorities.  Some aspects of the design will also imply a specific **development sequence** for some interdependent features, so we should make that explicit too.  A well defined feature list and development sequence will also make the allocation of agile development tasks to teams more manageable later. After the first iteration, we will just need to update these documents. Once the first iteration of these documents have been reviewed and agreed by the TC and SC, we will transfer the tasks for our first development release to the Kanban board category ‘analyse and write tests’. We will then assign **feature owners** to each, to assist the developers with refining the requirements/features and designing acceptance tests for each feature. Where practicable, we will automate these tests so that they can be easily rerun and incorporated into the **continuous integration** later, though some tests will necessarily be manual.

## Develop the software components
We will create a fork in the code for each feature (a **feature branch**), into which all changes related to the development of that feature will initially be committed.  This will allow us to easily choose which features are fit for release at any release point and which features we will defer to a later release.  It avoids having a whole tangled mess of code changes that can't easily be made fit for release when the time comes.

As we refine the features, we will convert the Kanban items and/or GitHub issues into tasks for the development team (or, in many cases, just tidy the ones we have already).  The GitHub issues (tasks) for each feature will be grouped into **feature projects**, in effect a mini Kanban board per feature.  This will allow us to track the progress of the tasks and the features that could go into a release.  A feature may consist of a group of functions and may span code from different system components, for example UI code and back-end code.  However, we should avoid making the features too large and monolithic, because we are more certain of delivering value with each release if we keep them small and manageable and deliverable within short iterations.

Features will be developed by **feature squads** (sub-teams).  Each developer within the squad will fork the feature branch and make atomic (indivisible, testable) code changes to their own fork.  Once they are happy each change is ready and passing unit tests, they will issue a pull request to merge their change back into the feature branch. They will continue to iterate in this way, through each change they are required to contribute to the feature.

Feature owners will regularly review and test the new or changed features and provide feedback as they are developed.  In particular, they will run acceptance tests against a feature branch, which must pass before the feature is merged back into the **develop branch**.  This will involve a test review, code review and of course, a pull request.

## Integrate the software components    
The develop branch will be permanently incorporated into the continuous integration suite, so that integration tests are run nightly to verify that changes have been successful.  Any test failures will be fixed by the squad that developed the feature.  If the test failures cannot be quickly resolved, then the develop branch will be rolled back to the previous stable state, in effect removing the broken feature(s).

## Release the software packages
The dates for software releases will be proposed by the Technical Committee and fixed by agreement at the Steering Committee.  The type of releases will also be fixed, that is, **development release** or **production release**.

The release will go ahead with the features that are available at the time, within the stable develop branch.  The develop branch will be merged into the **master branch** by the CM team and the rest of the release package prepared (eg: documentation updates).  All subsequent development will make a clean start with a fork of this master.

[DP]: {{ site.baseurl | prepend: site.url }}/assets/OpenWIS4-development-process.svg
