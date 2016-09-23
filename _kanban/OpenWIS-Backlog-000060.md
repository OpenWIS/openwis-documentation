---
layout: backlog
title: Adopt Kanban
kanCategory: develop
kanSubCategory: in-progress
kanAssigned: PR
kanBacklog: 60
kanIssue:
kanPullReq: 3
kanFeature: Good development processes
kanRelease:
kanMetric: 9.2
kanSize:
kanPriority: 1
kanRepo: OpenWIS/openwis-documentation
kanProject: 1
---
Adopt a more flexible development methodology and match with governance changes - eg: Kanban. LM - This needs to be adopted soonish to enable the association to start working on features.

A [project](https://github.com/OpenWIS/openwis-documentation/projects/1) has been set up for this task on GitHub.

The main issue is #56 - Process: Document the process for managing the Backlog and Kanban Board and post it to gh-pages.

I am writing my emerging thinking on this into this Kanban item and will eventually use it to form a post explaining the process.


## Introduction

There are a number of agile development methodologies, Kanban being one of them.  Kanban is a set of principles that can be implemented in different ways and tailored to particular situations.  This is a proposal for how the OpenWIS Association AISBL could improve its development processes by adopting Kanban-style procedures into its existing development and governance arrangements.

But before we describe how we might do that, let's think about what the OpenWIS Association development process is and what it is trying to achieve.

## User story for the development process

- **As** a non-profit association whose purpose is 'to facilitate collaboration on the development, promotion and sharing of open source software for the exchange of global meteorological information'  [article 2.1](http://openwis.github.io/openwis-documentation/articles/2-purpose.html)
- **We** want a development process that, with limited resources, boosts collaboration and expedites the regular delivery of quality software
- **So that** all interested parties can exchange global meteorological information as effectively and as efficiently as possible.

To do this, the OpenWIS Association is running a development programme.  This programme has been running for years and is expected to continue into the future, for so long as the Association retains the objectives above and is succeeding in meeting them through this vehicle. At present this programme develops one key product, OpenWIS Core, but has aspirations to develop others that fit with the purpose of the Association. The Association takes strategic direction from a global WMO programme (WIS) that is itself still unfolding and that is expected to continue into the foreseeable future.  Further strategic direction may come from other WMO programmes.

The OpenWIS Association development programme has run a number of projects over the years to initially develop and then refine the OpenWIS Core software, the last being the upgrade to OpenWIS v3.14 and the next being the re-architecture to OpenWIS v4. There have also been side-projects, such as the project within the UK Met Office to more fully automate the deployment of OpenWIS v3.14 and product extensions such as the project within Australian Bureau of Meteorology to provide WIS Monitoring for OpenWIS Core.

So, the OpenWIS Association is running an ongoing software development programme consisting of a stream of projects and releases.  Most of the new requirements are improvements to the existing product requested by the Users, or come from the evolving WIS strategic programme, or are new technology opportunities.

The modern way to manage such an activity is by using an agile development methodology.  The agile development methodology that fits well with a continuous improvement programme where workflow is constrained is - Kanban.

## Proposed Kanban process overview

### Backlog - product-backlog

Initially, all new requirements, feature requests and issues should be added to a product-backlog.  Now since OpenWIS Association is running a programme that includes multiple products and projects, we'll just call it the _Backlog_ and put every new idea etc in there.  Then we can decide later whether a new idea is worthy of a project in its own right, is a completely new product or how it fits with existing products and projects.

There are instructions below on how to add a new item to the Backlog.  The main thing is to provide information about the idea that will allow it to be assessed by the Technical Committee.  If this information is accessible elsewhere then just link to it from the Backlog item.  This is often the case with something that has arisen as a result of an issue on GitHub.

### Kanban - release-backlog

From time to time, the Technical Committee will review the Backlog and decide which ideas should be taken forward to the next release.  This always happens at least once a year at the Annual Meeting of the OpenWIS Association.  The ideas to be taken forward will be moved to the Kanban Board, which is effectively the release-backlog.  Once an item is on the Kanban Board then contributors can volunteer to undertake the related tasks.  Often, this will involve going through a development lifecycle, so the Kanban Board categories describe our preferred cycle:

- analyse
- design
- develop
- code review
- test
- test review
- release
- done

The other key feature of a Kanban Board is that we set a limit on how many things we try to do at once.  It might sound as if this slows down progress, but actually it has the opposite effect; real progress, ie: valuable improvements getting delivered, is speeded up, because we focus on finishing things before we start something else.  We also avoid the complexity overload that can come with too many things changing at once, which improves quality.

For relatively simple items, the progress can be tracked by just updating the status of the items on the Kanban Board as they move through the cycle.

### Project - sprint-backlog

However, most software development of a sophisticated product like OpenWIS Core is not simple, so we need to track progress at a lower level of granularity.  For example, say we have an item in _analyse_ and as we do the analysis we find that the item breaks down into a number of sub-tasks that involve some design and some development.  What we do then is we break the work down into _sprints_ and we track progress within each sprint using GitHub projects for each.  In effect, we assign the sub-tasks to sprint-backlogs and then work through those, iterating through the work in a controlled way at a lower level.  When the sprint-backlog work is complete we pop back up a level to the Kanban Board to continue the development cycle for the release.

So, by using this approach, we will be able to easily share with each other what progress we are making, where we might work on things together, provide help etc.

## Template for new Backlog items

New Backlog items should be saved as individual Markdown files into the folder *OpenWIS/openwis-documentation/_backlog/*.  The filename format is: *OpenWIS-Backlog-nnnnnn.md*, where *nnnnnn* is the 6 digit item number with explicit leading zeros; so Backlog item 60 has the filename *OpenWIS-Backlog-000060.md*.  Markdown is a plain text format; be sure to use a plain text editor to create the files because word processors introduce spurious characters that can crash the gh-pages processor or lead to formatting errors in the html output.

### Leading block: yaml

Internally, the file consists of a leading block of yaml, followed by the Markdown.  The yaml block must be the first thing in the file. The two lines of 3 dashes that frame the yaml are required.  For example:

    ---
    layout: backlog
    title: Remove PostgresSQL JDBC driver jar dependencies
    kanCategory: backlog
    kanSubCategory:
    kanAssigned: UKMO
    kanBacklog: 38
    kanIssue: 74
    kanPullReq:
    kanFeature: Integrated catalogue
    kanRelease: 4.1
    kanMetric: 1.2
    kanSize: 1
    kanPriority: 7
    kanRepo: OpenWIS/openwis
    kanProject:
    ---

This yaml block defines metadata about the Backlog item.  Fill out the metadata as follows:

- **layout:** is always **backlog**; it defines the html layout for the pages that show Backlog items.   Example - **layout: backlog**
- **title:** is the title you give to the Backlog item.  It is displayed on the Backlog index page and as the title of the Backlog page and browser tab.   Example - **title: My awesome new feature**
- **kanCategory:** is always **backlog** for a Backlog item; it only changes to something else when the item gets moved to the Kanban Board (see below).   Example - **kanCategory: backlog**
- **kanSubCategory:** is almost always left blank for a new Backlog item.  However, it can be one of the following:
  - new project: for a Backlog item that will be a project in its own right,
  - urgent: use this to draw attention to a new item that is, well, urgent!
  - in-progress: shouldn't normally be applied to a new Backlog item, but has cropped up when transferring items from our old spreadsheet,
  - merge: again, shouldn't normally be applied to a new Backlog item, but has cropped up when transferring items from our old spreadsheet that appear to be duplicates,
  - won't do: again, shouldn't normally be applied to a new Backlog item, but has/might crop up when reviewing the Backlog.
  -   Example - **kanSubCategory: new project**
- **kanAssigned:** initials of person, group or organisation assigned to the task, can be left blank.   Example - **kanAssigned: KMA**
- **kanBacklog:** next free item number, same as nnnnnn in the filename, but without the leading zeroes. Check both the */_backlog/* and */_kanban/* folders for the highest number used so far, then increment.   Example - **kanBacklog: 177**
- **kanIssue:** issue number on GitHub for the one most relevant issue, can be left blank. Example - **kanIssue: 46**
- **kanPullReq:** pull request number on GitHub for the one most relevant pull request, can be left blank.   Example - **kanPullReq: 5**
- **kanFeature:** leave blank for now.
- **kanRelease:** target release number, can be left blank.   Example - **kanRelease: 4.2**
- **kanMetric:** goal.metric eg: 2.1 for goal 2, metric 1.  Or, just 2 for goal 2.  Can be left blank, but all Backlog items should relate to our goals somehow.   Example - **kanMetric: 3.2**
- **kanSize:** estimate of task size, for initial planning purposes, using the rough measure of 1 point for every 10 days effort. Can be left blank. Example - **kanSize: 1**
- **kanPriority:** task priority - one of: 6, 7, 8, 9, 10, where 6=very-high;  7=high; 8=medium; 9=low; 10=very-low.   **Do not leave blank** because this is what the Backlog list is grouped by. Note that task priorities 1 to 5 are reserved for items on the Kanban Board; this is explained later. The priority you set here in the Backlog will be used to inform Technical Committee discussions about which tasks should be promoted to the Kanban Board, which is where the tasks we intend to work on in the near future are put. During that discussion, you will have to justify why you assigned a particular priority, so it would be useful to add this justification or supporting evidence to the Backlog item body text, especially for priorities 6-very-high and 7-high. Example - **kanPriority: 8**
- **kanRepo:** the main code repository that contains the Code, Issues, Pull Requests and Projects that are relevant to this Backlog item.  The current repos are listed below.  Example - **kanRepo: OpenWIS/openwis**
    - OpenWIS/openwis
    - OpenWIS/openwis-documentation
    - OpenWIS/open-dj-am-install-scripts
    - OpenWIS/openwis-deploy
    - OpenWIS/openwis-automated-tests
    - OpenWIS/data-harness-Moved-To-Stash
    - OpenWIS/geonetwork-extensions
    - OpenWIS/core-geonetwork
    - or any new repos we create. Can be left blank. Any secondary repositories can be linked to from the body text.
- **kanProject:** usually blank for a new item, this is the project number assigned by GitHub when a project is created.  Example - **kanProject: 2**

### Body text: Markdown

Text describing the item, written in [Markdown](https://daringfireball.net/projects/markdown/) or [GFM](https://guides.github.com/features/mastering-markdown/). This text can be any length and include links and images.

## Changes that transform a Backlog item into a Kanban Board item

The exact same template used for Backlog items is also used for Kanban Board items.  There are only 2 changes that _need_ to be made to a backlog item file to promote the item from the Backlog to the Kanban Board (though there are a few other optional changes you may choose to make right away, or leave until later):

  - The first essential change is to move the file from the **/_backlog/** folder to the **/_kanban/** folder.  The filename stays exactly the same.
  - The second essential change is to update the **kanCategory** in the file yaml header block, from **backlog** to one of the Kanban Board categories. This is required because this is the field which represents the phases of the development cycle and that the Kanban Board items are grouped by:

      - analyse
      - design
      - develop
      - code review
      - test
      - test review
      - release
      - done

For any item that will require significant work you are most likely to be updating the **kanCategory** to **analyse** when first promoting it to the Kanban Board. However, for a very small piece of work like a quick bug-fix, you might move it straight to **develop**.  Another possibility is that you move something directly to **test** to gather test evidence prior to moving it to **analyse**.  There is no enforced restriction or order, it is up to you to put items into sensible categories that fit the situation.

### Further changes for the Kanban Board

The next useful change to make to the item once it is on the Kanban Board is to update the **kanSubCategory**.  This is usually blank for a **backlog** item and is usually updated to _pending_ when an item is first moved onto the Kanban Board. The other option for **kanSubCategory** on the Kanban Board is _in-progress_.  This indicates whether the task is waiting to be assigned resources and for work to begin on it (pending) or is being actively worked on (in-progress). The **kanCategory** and **kanSubCategory** are then taken together to mean one of the following:

  - analyse pending _OR_ analyse in-progress
  - design pending _OR_ design in-progress
  - develop pending _OR_ develop in-progress
  - code review pending _OR_ code review in-progress
  - test pending _OR_ test in-progress
  - test review pending _OR_ test review in-progress
  - release pending _OR_ release in-progress

When the **kanCategory** is _done_ then the **kanSubCategory** is irrelevant, so it can be set to blank.

The other very useful thing to update is the **kanPriority**.  This has a different meaning on the Kanban Board from the meaning it has in the Backlog, which is why the task priority numbering scheme is different. On the Kanban Board the **kanPriority** is in the range 1 to 5, where 1 is the highest priority and:

  - 1 = blocker
  - 2 = must
  - 3 = should
  - 4 = could
  - 5 = blocked

So you can see that, once an item has been promoted to the Kanban Board, we begin prioritising using the common _must/should/could_ scheme, with the addition of _blocker_ and _blocked_.  This scheme helps us organise the tasks into sprints and projects.  Ultimately, it also helps us specify which features will be in specific Releases.  Each of these priorities has the following meaning:

  - 5 - blocked: We had planned to do this task at this time but some obstacle to starting or completing this task is preventing further work, so it is parked until the obstacle is removed.
  - 4 - could: Tasks that we could choose to do when we have completed all the _musts_ and _shoulds_; nice to haves but not essential to the Release/Project/Sprint.
  - 3 - should: Tasks that would add significant value but that we can live without if we have to.
  - 2 - must: Tasks that represent the main purpose and value of the Release/Project/Sprint.
  - 1 - blocker: can be either:

      - Real showstoppers; if we can't do these then there is no point doing the Release/Project/Sprint at all,
      - or a task that is working on removing obstacles that are causing other tasks to be _blocked_.
