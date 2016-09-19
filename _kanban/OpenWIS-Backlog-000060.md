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
kanRelease: 4.1
kanMetric: 9.2
kanSize:
kanPriority: 1
kanRepo: OpenWIS/openwis-documentation
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

## Markdown template for new Backlog items

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
    ---

This yaml block defines metadata about the Backlog item.  Fill out the metadata as follows:

- **layout:** is always **backlog**; it defines the html layout for the pages that show Backlog items.
- **title:** is the title you give to the Backlog item.  It is displayed on the Backlog index page and as the title of the Backlog page and browser tab.
- **kanCategory:** is always **backlog** for a Backlog item; it only changes to something else when the item gets moved to the Kanban Board (see below).
- **kanSubCategory:** is almost always left blank for a new Backlog item.  However, it can be one of the following:
  - new project: for a Backlog item that will be a project in its own right,
  - urgent: use this to draw attention to a new item that is, well, urgent!
  - in-progress: shouldn't normally be applied to a new Backlog item, but has cropped up when transferring items from our old spreadsheet,
  - merge: again, shouldn't normally be applied to a new Backlog item, but has cropped up when transferring items from our old spreadsheet that appear to be duplicates,
  - won't do: again, shouldn't normally be applied to a new Backlog item, but has/might crop up when reviewing the Backlog.
- **kanAssigned:** initials of person, group or organisation assigned to the task, eg: KMA; can be left blank.
- **kanBacklog:** next free item number eg: 166; same as nnnnnn in the filename, but without the leading zeroes. Check both the */_backlog/* and */_kanban/* folders for the highest number used so far, then increment.
- **kanIssue:** issue number on GitHub for the one most relevant issue, eg: 46; can be left blank.
- **kanPullReq:** pull request number on GitHub for the one most relevant pull request, eg: 5; can be left blank.
- **kanFeature:** leave blank for now.
- **kanRelease:** target release number, eg: 4.2; can be left blank.
- **kanMetric:** goal.metric eg: 2.1 for goal 2, metric 1.  Or, just 2 for goal 2.  Can be left blank, but all Backlog items should relate to our goals somehow.
- **kanSize:** estimate of task size, for initial planning purposes. See: [link] for an explanation of Size.
- **kanPriority:** task priority - one of: 6, 7, 8, 9, 10, where 6=very-high;  7=high; 8=medium; 9=low; 10=very-low.
- **kanRepo:** the code repository relevant to the Issues or Pull Requests:
    - OpenWIS/openwis
    - OpenWIS/openwis-documentation
    - OpenWIS/open-dj-am-install-scripts
    - OpenWIS/openwis-deploy
    - OpenWIS/openwis-automated-tests
    - OpenWIS/data-harness-Moved-To-Stash
    - OpenWIS/geonetwork-extensions
    - OpenWIS/core-geonetwork
    - or any new repos we create. Can be left blank.

### Body text: Markdown

Text describing the item, written in Markdown or GFM. Can be any length.
