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

The main issue is - Process: Document the process for managing the Backlog and Kanban Board and post it to gh-pages. #56

I am writing my emerging thinking on this into this Kanban item and will eventually use it to form a post explaining the process.

Including:

  1. what the priorities mean
  2. how to add-to/update Backlog
  3. how to move-to/update Kanban
  4. Concepts of product-backlog; release-backlog; sprint-backlog.
  5. Epics and User Stories.
  6. What the Size means.

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

- **layout:** is always **backlog**; it defines the html layout for the pages that show Backlog items.   Example - layout: backlog
- **title:** is the title you give to the Backlog item.  It is displayed on the Backlog index page and as the title of the Backlog page and browser tab.   Example - title: My awesome new feature
- **kanCategory:** is always **backlog** for a Backlog item; it only changes to something else when the item gets moved to the Kanban Board (see below).   Example - kanCategory: backlog OpenWIS/openwis
- **kanSubCategory:** is almost always left blank for a new Backlog item.  However, it can be one of the following:
  - new project: for a Backlog item that will be a project in its own right,
  - urgent: use this to draw attention to a new item that is, well, urgent!
  - in-progress: shouldn't normally be applied to a new Backlog item, but has cropped up when transferring items from our old spreadsheet,
  - merge: again, shouldn't normally be applied to a new Backlog item, but has cropped up when transferring items from our old spreadsheet that appear to be duplicates,
  - won't do: again, shouldn't normally be applied to a new Backlog item, but has/might crop up when reviewing the Backlog.
  -   Example - kanSubCategory: new project
- **kanAssigned:** initials of person, group or organisation assigned to the task, can be left blank.   Example - kanAssigned: KMA
- **kanBacklog:** next free item number, same as nnnnnn in the filename, but without the leading zeroes. Check both the */_backlog/* and */_kanban/* folders for the highest number used so far, then increment.   Example - kanBacklog: 177
- **kanIssue:** issue number on GitHub for the one most relevant issue, can be left blank. Example - kanIssue: 46
- **kanPullReq:** pull request number on GitHub for the one most relevant pull request, can be left blank.   Example - kanPullReq: 5
- **kanFeature:** leave blank for now.
- **kanRelease:** target release number, can be left blank.   Example - kanRelease: 4.2
- **kanMetric:** goal.metric eg: 2.1 for goal 2, metric 1.  Or, just 2 for goal 2.  Can be left blank, but all Backlog items should relate to our goals somehow.   Example - kanMetric: 3.2
- **kanSize:** estimate of task size, for initial planning purposes, using the rough measure of 1 point for every 10 days effort. Can be left blank. Example - kanSize: 1
- **kanPriority:** task priority - one of: 6, 7, 8, 9, 10, where 6=very-high;  7=high; 8=medium; 9=low; 10=very-low.   **Do not leave blank** because this is what the Backlog list is grouped by. Example - kanPriority: 8
- **kanRepo:** the main code repository that contains the Code, Issues, Pull Requests and Projects that are relevant to this Backlog item.  The current repos are listed below.  Example - kanRepo: OpenWIS/openwis
    - OpenWIS/openwis
    - OpenWIS/openwis-documentation
    - OpenWIS/open-dj-am-install-scripts
    - OpenWIS/openwis-deploy
    - OpenWIS/openwis-automated-tests
    - OpenWIS/data-harness-Moved-To-Stash
    - OpenWIS/geonetwork-extensions
    - OpenWIS/core-geonetwork
    - or any new repos we create. Can be left blank. Any secondary repositories can be linked to from the body text.
- **kanProject:** usually blank for a new item, this is the project number assigned by GitHub when a project is created.  Example - kanProject: 2

### Body text: Markdown

Text describing the item, written in Markdown or GFM. This text can be any length.

## Template for Kanban Board items

The exact same template used for Backlog items is also used for Kanban Board items.  There are only 2 changes that _need_ to be made to a backlog item file to promote the item from the Backlog to the Kanban Board (though there are a few other optional changes you may choose to make):
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

The next useful change to make to the item once it is on the Kanban Board is to update the **kanSubCategory**.  This is usually blank for a **backlog** item and is usually updated to _pending_ when an item is first moved onto the Kanban Board. The other option for **kanSubCategory** on the Kanban Board is _in-progress_.  The **kanCategory** and **kanSubCategory** are then taken together to mean one of the following:
  - analyse pending _OR_ analyse in-progress
  - design pending _OR_ design in-progress
  - develop pending _OR_ develop in-progress
  - code review pending _OR_ code review in-progress
  - test pending _OR_ test in-progress
  - test review pending _OR_ test review in-progress
  - release pending _OR_ release in-progress

When the **kanCategory** is _done_ then the **kanSubCategory** is irrelevant.

The other very useful thing to update is the **kanPriority**.  This has a different meaning on the Kanban Board from the meaning it has in the Backlog, so a different numbering scheme is used, to avoid confusion.
