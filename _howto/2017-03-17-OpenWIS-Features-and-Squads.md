---
layout: page
title: OpenWIS-Core - Features and Squads
---

Link to [development process][DP] diagram.

[DP]: {{ site.baseurl | prepend: site.url }}/assets/OpenWIS4-development-process.svg

---

# Features

I propose that we categorise the OpenWIS Core functionality according to the primary functions of WIS itself.

- So these are:
    - **Discovery**
    - **Access**
    - **Retrieval**
- plus
    - **System Admin**
    - **Community**

...so that these are the high-level **Features**.

System Admin is the stuff that goes on behind the scenes that the end-users don't normally see but that we need to do to provide the service.

Community is all the stuff that surrounds any group activity, eg: packaging up a release, improving our processes or tools etc.

This will help us to focus our attention on specific areas of improvement.  With OpenWIS v3.14 we did a lot of architecture work; for OpenWIS4 I think we are expecting to focus more on improvements for the end-users, though we will still have to do _some_ back-end work.  

<br/>

---

# Squads

In agile development, a squad is a multi-disciplinary development sub-team that is dedicated to a specific category of tasks.
I propose that we assign a Squad to each Feature, except for Community, which everyone contributes to.

- So we would need 4 Squads:
    - **Discovery Squad**
    - **Access Squad**
    - **Retrieval Squad**
    - **System Admin Squad**

---

# Squad composition

- Ideally, each Squad would have:
    - A Feature Owner: responsible for making sure the Feature does the right thing and does it right. This will involve guiding the rest of the squad and testing/reviewing the Feature regularly as it is being developed and ultimately, accepting it.
    - A Lead Developer: responsible for producing quality code and a solution that works well (eg: has good performance).
    - A second developer from a different member organisation, so that we can improve quality and knowledge sharing through pair-programming across the Association.

Note that Features cut across Releases and Versions; for example, if a bug is found in the Discovery Feature of both v 3.14 and v4.1, then the Discovery Squad would fix it in both, even if the solution is not identical in both versions.

### Question: Can a Squad work on more than one feature?

### Answer: Not at the same time. Once a Squad finishes work on its own Feature, it can be assigned to another.
This maintains the focus required to finish what we have started so that we have at least some features finished for a release.
It also reduces complexity and pressure, which improves quality.  All Squad members will engage in Community activities,
which could include, for example, answering a query from another Squad.
