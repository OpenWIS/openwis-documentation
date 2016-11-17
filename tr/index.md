---
title: Technical Rules
layout: default
permalink: /tr/
---

# {{ site.data.tr.title }}

As set out in [Title 11]({{ "/rules/11-technical-rules.html" | prepend: site.baseurl }}) of the [Internal Rules]({{ "/rules/" | prepend: site.baseurl }}), these **Technical Rules** govern the development of software within OpenWIS® Projects.


## Overview

- The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](http://www.faqs.org/rfcs/rfc2119.html).

## Scope

- Any code written as part of a project under the collective ownership of the OpenWIS Association MUST adhere to the OpenWIS Technical Rules.
- Any code under the collective ownership of the OpenWIS Association that was written before the commission or alteration of the technical rules section MAY be in violation of said guidelines until updated.  In other words: these rules are not retroactive.  However, it is RECOMMENDED that said code be updated to meet the technical rules if at all possible.

## Governance

- The Technical Committee is responsible for maintaining and evolving the *Technical Rules* outlined in this document.
- Any disputes regarding the interpretations of the rules outlined in this document will be resolved by consensus of members of the Technical Committee.

## Code Style

### Java Code

- Any Java code that falls under the custody of the OpenWIS Association MUST adhere to the [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html), with the following exceptions:
    - The block indentation is **3 spaces** (this overrides Section 4.2)
    - The column limit is **120 characters** (this overrides Section 4.4)
    - Continuation lines are to be indented by **6 spaces** (this overrides Section 4.5.2)
- Along with the rules outlined with the [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html), any Java code that fulls under the custody of the OpenWIS Association MUST also adhere to the following rules:
    - **Identifiers**: all Java identifiers (such as type names, method names, field names, constants, enums) MUST be named in American English
    - **Javadoc**: all Javadoc MUST be written in English and SHOULD be written in American English
    - **Comments**: all other comments SHOULD be written in American English

## Test Coverage

- Unit tests SHOULD be written for any _non trivial_ code.  What is considered _non trivial_ is left to the discretion of the developer but, in general, includes code that encodes the core "business logic" of OpenWIS and has a direct impact to the successful fulfilment of the requirements imposed on the software.
- Unit tests SHOULD be written to run as part of the Maven build and SHOULD NOT rely on any external dependencies such as an external database or runtime container.

## Contributing Changes Back To The Central Repository

- All changes to be contributed back to the main repository MUST be made in the form of a pull request.
- Any changes that directly relate to any development effort (i.e. new feature or bug fix) MUST comply with the following conditions prior to merge:
    - The target branch MUST be `develop` or another development/feature branch.
    - The target branch MUST NOT be `master`.
    - The changes MUST have been tested locally using the latest version of `develop` with all unit tests passing.
    - The changes MUST NOT have any conflicts prior to review.  These must be resolved by the contributing developer before notifying the reviewer.
    - If updates to the target branch cause merge conflict preventing the merge of the changes from within GitHub, the contributing developer must resolve these conflicts and update the pull request.
    - Any effect these changes have to the stability of the build or the successful execution of the integration tests MUST be resolved by the contributing developer.
- Any changes to be merged from a pull request into the main repository SHOULD be reviewed by another member of the development team.  The developer submitting the pull request is responsible for making the request for review.
- If the pull request is to be reviewed, the reviewer MUST sign off the changes by adding a comment to the pull request stating that the changes are ready to be merged.
- Once the changes have been signed off by the reviewer, the developer submitting the pull request MUST merge the changes from within GitHub.

## Documentation

### Wiki

- The GitHub Wiki is intended for any documentation relevant for developers or contributors of OpenWIS.  This includes, but is not limited to:
    - Getting started guides for developers
    - Architecture and technical documentation
    - Guides for making contributions
  Non-developers MAY view the documents within this section but documentation intended for non-developers SHOULD NOT be added here.
- Documentation published through the Wiki must be written in GitHub flavoured Markdown.

### Website

- The website is intended for any documentation relevant to end users.  This may include, but is not limited to:
    - Installation guide
    - Operation guides
    - Release notes (should this be tracked on the website or should this be tracked somewhere in the repository/wiki?)
    
  Developer documentation MAY be added here but it is recommended to keep all developer documentation located in the GitHub Wiki (a link to the document in the Wiki is preferred over publishing the document in two places).
- All documentation published through the website MUST be written in a text-based format (Markdown, HTML, plain text).  If a "printed" form of a particular document is required, it SHOULD be derived directly from the text-based version.
- All documentation published through the website MUST be tracked within a git repository accessible to all developers, preferably a repository hosted on GitHub.
- Updates to the contents of the website must be submitted in the form of a Pull Request to the documentation GitHub repository.  The contents of the Pull Request SHOULD be approved by the Community Manager before being merged and published to the web.  (Should this be the case?)

### General

- All documentation MUST be written in English and SHOULD be written in American English.

## Release

- Designated members of the "release team" are responsible for the creation of releases of OpenWIS.
- The process of release consist of the following steps, which MUST be followed by a member of the release team:
    - All changes from develop are merged into master.
    - Master is tagged with the name 'openwis-VERSION' where _version_ is the release number.

## Contributing To Third Party Projects

- Any code written and contributed to a third-party project MUST adhere to the technical rules and coding style set by the maintainers of the third party project.
- Any code written and contributed to a third-party project SHOULD adhere to the OpenWIS Technical Rules, unless it conflicts with rules set by the maintainer of the third-party project, or it introduces a significant burden on the developer that cannot justify adherence to the rule in question.  This is left to the discretion of the contributing developer.
- If a rule set by the maintainers of a third-party project is in conflict with a rule outlined within the OpenWIS Technical Rules, the former overrules the latter.  This includes, but is not limited to, rules governing code style, code reviews, pull requests, communication, etc.
