---
layout: page
title: OpenWIS Technical Committee 2016 October
---

#### 26th October 2016 - teleconference - meeting minutes

---

1. **Organise the formulation of an open source release of OpenWIS to be announced at CBS.  This includes the particular version to be released and the contents of the package itself**
	1. WQ - Leon, please summarise what was discussed at the Developer Conference last month.
  1. LM - It was proposed that we release OpenWIS v3.14 as open source in time for announcement at the CBS meeting in November, because v4 won't be ready by then.  Version 3.14.6 is the latest stable release.  I believe v3.14.7 is still in progress. 
  1. SO - Is the Java version security issue resolved in v3.14.6?
  1. LM - No, that's in a branch that would become v3.14.7.
  1. SO - Are there any issues with merging the Java version changes into master?
  1. OL - We have been testing 3.14.6 and it is stable. Ideally we wouldn't want to release it with security issues, but if we can't merge the changes quickly we should release v3.14.6. So, is it doable in 2 weeks?  Is it the XSS issues that get resolved?
  1. WQ - No, the XSS fixes are already in v3.14.6.
  1. OL - The Java version issue is not critical so a v3.14.6 release is safer.
  1. SO - We tested the Java version fix months ago and yesterday GISC-Washington went LIVE running v3.14.7.
  1. WQ - So how much effort would be involved in merging?
  1. LM - If it is just the Java vesion then it would affect the vagrant scripts.
  1. OL - We have modified the vagrant scripts to specify the version of JDK because it was not working with virtual-box, but is was a simple change.
  1. WQ - So shall we say we are aiming to release v3.14.7, depending on the outcome of Leon's investigation?  And if not, then v3/14.6?
  1. OL - How about we go with v3.14.7 if only the vagrant scripts change.
  1. PR - I thought there were some portal code changes.
  1. SO - Ok, I have found the [ticket](https://github.com/OpenWIS/openwis/issues/173).  There are some changes to the portal POMs.
  1. LM - it doesn't look like there should be any conflicts.
  1. ACT-OWIS-TC-48:Action: LM - Check the changes are good and then raise a pull-request. OWIS-ACT
  1. MC - We are deploying v3.14.6 with some of our own fixes into our production environment.  I don't think we will have the time before CBS to apply those changes to v3.14.7.
  1. WQ - You think we should not release v3.14.7 without your fixes?
  1. No, just that we can't push our fixes in time - they fix a few minor issues with Solr and some Javascript.
  1. WQ - Ok, so your changes can wait until v3.14.8.
  1. MC - But will v3.14.8 be open source?
  1. PR - yes, once the repository is made open source all subsequent releases are open.
  1. DW - Will there need to be further testing?
  1. PR - It sounds like NWS have tested it, Steve?
  1. SO - Yes, we have and it is in production.
  1. LM - Are we releasing source or binaries?
  1. PR - Since we are hoping to encourage contributions later, I suggest source.
  1. WQ/OL - Agreed - release the source.
  1. PR - So, on to the rest of the package - at the Developer Conference Okki suggested a hardware spec would be useful.
  1. OL - Yes, say 8GB RAM, 64 bit etc.
  1. ACT-OWIS-TC-49:Action: OL - Document the hardware spec for a typical environment and add to the document pack for the release. OWIS-ACT
  1. PR - Do the install docs we have already mention vagrant etc?
  1. LM - Yes, in the wiki Getting Started guide.
  1. NM - Is there an installation from scratch?
  1. LM - Yes, there are installation instructions in a couple of WORD docs in openwis/docs.
  1. Where do we expect people to access this package from, our website? The GitHub wiki?
  1. LM - Do we have a website?
  1. SO - We're about a week away from a demo.
  1. LM - So we could put a link on our website or put something in our GitHub READ.ME.
  1. ACT-OWIS-TC-50:Action: LM - Review the READ.ME and make it more useful as a starting point for potential contributors. OWIS-ACT
  1. WQ - Do we need a check-list for the tasks required to go open source?
  1. PR - Yes, I'll construct one from my notes.
  1. ACT-OWIS-TC-51:Action: PR - Publish a check-list so everyone can keep track of progress. OWIS-ACT
2. **Approve the draft contributor license that will be released alongside the software.  The SC is currently waiting for this to be agreed on before having their own meeting**
	1. WQ - Paul circulated a draft CLA.
  1. PR - Michael Robbins (UKMO Legal) has checked it and suggested two minor changes, but is happy with it.  I will update the draft with Michael's changes.  Please send me any further suggestions for change.
  1. WQ - Do we all need to ratify the CLA?
  1. PR - Eventually, but we can go open source while that is in progress, because we can change the CLA anytime we like, it says so in the CLA itself.  In any case, we are not expecting a big rush to contribute.
  1. DW - When will the CLA be available?
  1. PR - When we go open source it will be on our website - we need something and this version will cover us.
3. **Any preparation work before CBS in November**
  1. PR - Leon has submitted a pull-request with some Technical Rules.  I had a quick look and they look good, so I will merge the pull-request and everyone can review them on the site.  The only thing that sprang to mind was whether we want to have rules about the documentation standards for website, wiki, etc.
  1. LM - Ok, I'll take a look at adding those in.
  1. ACT-OWIS-TC-52:Action: LM - Add or extend Technical Rules to cover wider documentation standards. OWIS-ACT
  1. PR - There is also the Code of Conduct - not essential, but I'll try to draft something before the announcement.
  1. ACT-OWIS-TC-53:Action: PR - Find a suitable sample and draft a Code of Conduct. OWIS-ACT
  1. PR - At the Developer Conference we assumed MFI would provide commercial support to anyone that wanted that.
  1. ACT-OWIS-TC-54:Action: PR - Check this is ok with MFI and ask how they want to represent that on the website etc. OWIS-ACT
  1. PR - We also need the poster to actually do the announcement.
  1. ACT-OWIS-TC-55:Action: MC - Ask when the poster is expected to be ready and let the TC know. OWIS-ACT
  1. ACT-OWIS-TC-56:Action: WQ - Send the draft poster to SO. OWIS-ACT
  1. PR - The remaining task is to actually switch the GitHub repos to PUBLIC.
  1. ACT-OWIS-TC-57:Action: PR - Arrange for the UKMO CM team to do that once the SC give approval. OWIS-ACT
  1. OL - So what date is the TC recommending we make the repositories open source?
  1. WQ - The week before the CBS meeting.
4. AOB
	- Nil

---

#### Participants

- WQ - Weiqing Qu, Bureau of Meteorology, Australia [BoM], Chair
- LM - Leon Mika, Bureau of Meteorology, Australia [BoM]

- OL - Okki Lee, Korea Meteorological Administration, Republic of Korea [KMA]
- HL - Hyekyoung Lee, Korea Meteorological Administration, Republic of Korea [KMA]

- MC - Michael Claudon, Meteo France, France [MF]

- SO - Steve Olson, National Weather Service, USA [NWS], Vice-Chair
- KS - Kari Sheets, National Weather Service, USA [NWS]

- DW - Dominic Woollatt, Met Office, UK [UKMO]
- PR - Paul Rogers, Met Office, UK [UKMO]

- NM - Nassos Michas, European Dynamics, Greece [UKMO]
- DP - Dimitris Papadeas, European Dynamics, Greece [UKMO]
