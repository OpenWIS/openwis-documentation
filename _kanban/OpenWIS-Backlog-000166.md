---
layout: backlog
title: Link from backlog item to GitHub to edit
kanCategory: done
kanSubCategory:
kanAssigned:
kanBacklog: 166
kanIssue:
kanPullReq:
kanFeature:
kanRelease:
kanMetric:
kanSize:
kanPriority: 1
kanRepo: OpenWIS/openwis-documentation
kanProject: 1
---
There should (automagically) be a link in every Backlog item that takes you to the page on GitHub.com where you can edit the item and save it.

Maybe also for each post?

Maybe also a link to click to add a new post/backlog-item?

Maybe also for all other docs on the site - a link in every page footer?

As a start, let's just get the address of the file on GitHub displayed in the footer of every page.

## Analysis

The url of this page on the local jekyll server site is: http://127.0.0.1:4000/openwis-documentation/backlog/OpenWIS-Backlog-000166.html
The url of this page on this openwis-documentation site page is: http://openwis.github.io/openwis-documentation/backlog/OpenWIS-Backlog-000166.html

The url of the EDITOR page on GitHub that corresponds to this openwis-documentation site page is: https://github.com/OpenWIS/openwis-documentation/blob/gh-pages/_backlog/OpenWIS-Backlog-000166.md

All we want to do is open the editor page on GitHub.  We are not offering the ability to edit the local version of the file, because you would do that through your favourite editor or toolset.

For this page:
 site.url resolves to http://openwis.github.io
 site.baseurl resolves to /openwis-documentation
 page.path resolves to _backlog/OpenWIS-Backlog-000166.md

 So the simplest approach would be to concatenate the string constant https://github.com/OpenWIS/openwis-documentation/blob/gh-pages/
 with the page.path and provide that as a link in the footer of the page.
