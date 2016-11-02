---
title: Welcoming New Contributors and Managing CLAs
layout: page
---

## Instructions for pull request approvers

All contributions to OpenWIS Association Projects, whether code or documentation, should be submitted via a pull request.  Before we accept any pull request from someone who is not a member of the OpenWIS Association, ie: an external collaborator, we must ensure there is a valid contributor license agreement on record.  Please follow the process below to ensure this is so.

### Check GitHub

First, check if the GitHub ID of the submitter is already registered on GitHub as a member of the project organisation, by checking that their GitHub ID is listed on the **People** tab.  So for the OpenWIS Core project check [OpenWIS/people](https://github.com/orgs/OpenWIS/people).  If they are already there, you can go on to review the pull request in the normal way and skip the rest of this process.

### Check for a signed CLA

If they are a new contributor, they should have sent a scan of a signed CLA form to the OpenWIS Community Manager.  [Check for this file]( {{"/static/CLA/CLA-Forms-scanned-DO-NOT-DELETE/" | prepend: site.baseurl}} ).  The filename should include their GitHub ID and the name of the project they are contributing to, for example **rogers492-cdms-2016-11-01.pdf**.  If found, open the file and check the CLA form is complete and relevant to the pull request project.  If it is then you can go on to review the pull request in the normal way and skip the rest of this process.

### Request a signed CLA

If no signed CLA form relevant to the project in question is available, then please ask the contributor to provide one and point them to the CLA page on the website.  Leave the pull request review until they have successfully complied with this request, then repeat this process from the top.

## Instructions for the Community Manager

When a completed CLA form is received by email, check that the GitHub ID provided exists and remind the contributor that one is required if none is found.

## Save a copy of the scanned CLA form

Name the file according to the convention **githubId-projectName-YYYY-MM-DD.ext**, using the information in the form, for example: **lmika-bom-cdms-2016-12-15.pdf**.  Save it to the GitHub repo folder at OpenWIS/openwis-documentation [/static/CLA/CLA-Forms-scanned-DO-NOT-DELETE/]( {{"/static/CLA/CLA-Forms-scanned-DO-NOT-DELETE/" | prepend: site.baseurl}} ).

## Add the new contributor to the project organisation

Raise a request to do this with the [CM-Team](https://github.com/cmteam-metoffice).  Notify the new contributor when this has been done.

## Updates to the CLA and history

Whenever the CLA (appendix A of the Internal rules) is changed, which will only happen as a result of formal approval by the Steering Committee, the old version should be saved to the GitHub repo folder at OpenWIS/openwis-documentation [/static/CLA/CLA-old-DO-NOT-DELETE/]( {{"/static/CLA/CLA-old-DO-NOT-DELETE/#" | prepend: site.baseurl}} ) before the new one replaces it.  Also, the [CLA history table]( {{"/static/CLA/CLAhistory.html" | prepend: site.baseurl}} ) should be updated to reflect the change.
