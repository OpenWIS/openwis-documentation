---
title: Technical Rules
layout: default
permalink: /tr/
---

# {{ site.data.tr.title }}

As set out in [Title 11]({{ "/rules/11-technical-rules.html" | prepend: site.baseurl }}) of the [Internal Rules]({{ "/rules/" | prepend: site.baseurl }}), these **Technical Rules** govern the development of software within OpenWIS® Projects.

The Technical Committee is responsible for maintaining and evolving these **Technical Rules**.

## Contents

TODO

## Overview

PREAMBLE

## Scope

- Any code written as part of a project under the collective ownership of the OpenWIS association MUST adhere to the OpenWIS Technical Rules.
- Any code under the collective ownership of the OpenWIS association that was written before the commission or alteration of the technical rules section MAY be in violation of said guidelines until updated.  In other words: these rules are not retroactive.  However, it is RECOMMENDED that said code be updated to meet the technical rules if at all possible.

## Code Style

### Java Code

- Any Java code that falls under the custody of the OpenWIS association MUST adhere to the [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html), with the following exceptions:
    - The block indentation is **3 spaces** (this overrides Section 4.2)
    - The column limit is **120 characters** (this overrides Section 4.4)
    - Continuation lines are to be indented by **6 spaces** (this overrides Section 4.5.2)
- Along with the rules outlined with the [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html), any Java code that fulls under the custody of the OpenWIS association MUST also adhere to the following rules:
    - **Identifiers**: all Java identifiers (such as type names, method names, field names, constants, enums) MUST be named in American English
    - **Javadoc**: all Javadoc must be written in English and SHOULD be written in American English
    - **Comments**: all other comments SHOULD be written in American English

## Test Coverage

- Unit tests SHOULD be written for any _non trivial_ code.

## Contributing To Third Party Projects

- Any code written and contributed to a third-party project MUST adhere to the technical rules and coding style set by the maintainers of the third party project.
- Any code written and contributed to a third-party project SHOULD adhere to the OpenWIS Technical Rules, unless it conflicts with rules set by the maintainer of the third-party project, or it introduces a significant burden on the developer that cannot justify adherence to the rule in question.  This is left to the discretion of the contributing developer.
- If a rule set by the maintainers of a third-party project is in conflict with a rule outlined within the OpenWIS Technical Rules, the former overrules the latter.  This includes, but is not limited to, rules governing code style, code reviews, pull requests, communication, etc.