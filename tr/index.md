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

## Roles in the Develpment Process

- **Lead Developer**
 - The Lead Developer guide the ways in which the team works.  They are proficient in a wide range of technical disciplines and involved in identifying appropriate technology and approaches, deciding when software should be written.  The lead developer contributes to the community, providing technical leadership, coaching and mentoring the team, promoting knowledge sharing and adoption of good practice.  The Lead Developer also ensures that what's being implemented by the team is of the highest quality and has been developed in the shortest amount of time.  Above all, the Lead Developer is responsible for making the team successful!  
- **Developer**
 - A developer is responsible for ensuring that software quality standards and principles agreed is done to the highest possible quality.  A developer must accept that continuously learning is part of what it is to be a software developer, and by improving ones skills goes a long way to consistently delivering value.
- **CI lead**
 - A Continuous Integration (CI) Lead uses a software development practice in which each member of a development team integrates their work with that produced by others on a continuous basis.  
- **Quality control lead**
 - A Quality Control (QC) Lead has to ensure the end product meets  quality and efficiency standards set by the OpenWIS Association
- **Testing lead**
 - The Test Lead role is tasked with overall responsibility for the test effort's success. The role involves quality and test advocacy, resource planning and management, and resolution of issues that impede the test effort.

## Patch Management of OpenWIS Software

Patch Mangement, which is part of the Lifecycle Management, is ultimately how we can demonstrate Patchability.  To be "patchable" means that corrections to software can be applied to the software without altering the expected application behavior or performance.  The OpenWIS application is most certainly "patchable". The entire development process and Continuous Integration environment contributes to the application's "patchability". 

## Software Quality

OpenWIS follows an Agile Development Model and supports a full (https://github.com/OpenWIS/openwis-deploy/wiki "Continuous Integration Environment"). The code resides on (https://openwis.github.io/openwis/ "GitHub") and follows the traditional GitHub revision process. The Continuous Integration Environment performs automated (https://github.com/OpenWIS/openwis-automated-tests/wiki "Testing") using (https://github.com/OpenWIS/openwis/wiki/OpenWIS-Testing-Regime "Jenkins and Cloudbees") tooling.

## Code Style

### C/C++ bute to the community, providing technical leadership, coaching and mentoring the team, promoting knowledge sharing and adoption of good practicepractices

- Have you checked for compiler warnings? Warnings often point to real bugs.
- In C++ code, use nullptr for pointers. In C code, using NULL or 0 is allowed.
- Don't use PRBool and PRPackedBool in C++, use bool instead.
- For checking if a std container has no items, don't use size(), instead use empty().
- When testing a pointer, use (!myPtr) or (myPtr); don't use myPtr != nullptr or myPtr == nullptr.
- Do not compare x == true or x == false. Use (x) or (!x) instead. x == true, is certainly different from if (x)!
- In general, initialize variables with nsFoo aFoo = bFoo, and not nsFoo aFoo(bFoo).
- For constructors, initialize member variables with : nsFoo aFoo(bFoo) syntax.
- To avoid warnings created by variables used only in debug builds, use the DebugOnly<T> helper when declaring them.
- You should use the static preference API for working with preferences.
- One-argument constructors, that are not copy or move constructors, should generally be marked explicit.  Exceptions should be annotated with MOZ_IMPLICIT.
- Use char32_t as the return type or argument type of a method that returns or takes as argument a single Unicode scalar value. (Don't use UTF-32 strings, though.)
- Don't use functions from ctype.h (isdigit(), isalpha(), etc.) or from strings.h (strcasecmp(), strncasecmp()). These are locale-sensitive, which makes them inappropriate for processing protocol text. At the same time, they are too limited to work properly for processing natural-language text. Use the alternatives in mozilla/TextUtils.h and in nsUnicharUtils.h in place of ctype.h. In place of strings.h, prefer the nsStringComparator facilities for comparing strings or if you have to work with zero-terminated strings, use nsCRT.h for ASCII-case-insensitive comparison.
- Forward-declare classes in your header files, instead of including them, whenever possible. For example, if you have an interface with a void DoSomething(nsIContent* aContent) function, forward-declare with class nsIContent; instead of #include "nsIContent.h"
- Includes are split into three blocks, and sorted alphabetically in each block:
-- The main header: #include "Foo.h" in Foo.cpp
-- Standard library includes: #include <map>
-- Mozilla includes: #include "mozilla/dom/Element.h"
-- Include guards are named by determining the fully-qualified include path, then substituting _ for / and . and - in it. For example, nsINode.h's guard is nsINode_h, and Element.h's guard is mozilla_dom_Element_h (because its include path is mozilla/dom/Element.h).

Use the following exact form for include guards. GCC, and clang, recognize this idiom and avoid re-reading headers that use it. To avoid confusing GCC's and clang's header optimization, do not include any code before or after the include guards (comments and whitespace are OK). Do not combine any other preprocessor checks in the #ifndef <guard> expression.
```
#ifndef <guard>
#define <guard>
... All code ...
#endif // <guard>
```

### JavaScript practices

- Make sure you are aware of the JavaScript Tips.
- Do not compare x == true or x == false. Use (x) or (!x) instead. x == true, is certainly different from if (x)! Compare objects to null, numbers to 0 or strings to "", if there is chance for confusion.
- Make sure that your code doesn't generate any strict JavaScript warnings, such as:
- Duplicate variable declaration.
- Mixing return; with return value;
- Undeclared variables or members. If you are unsure if an array value exists, compare the index to the array's length. If you are unsure if an object member exists, use "name" in aObject, or if you are expecting a particular type you may use typeof(aObject.name) == "function" (or whichever type you are expecting).
- Use [value1, value2] to create a JavaScript array in preference to using new Array(value1, value2) which can be confusing, as new Array(length) will actually create a physically empty array with the given logical length, while [value] will always create a 1-element array. You cannot actually guarantee to be able to preallocate memory for an array.
- Use { member: value, ... } to create a JavaScript object; a useful advantage over new Object() is the ability to create initial properties and use extended JavaScript syntax, to define getters and setters.
- If having defined a constructor you need to assign default properties, it is preferred to assign an object literal to the prototype property.
- Use regular expressions, but use wisely. For instance, to check that aString is not completely whitespace use /\S/.test(aString). Only use aString.search if you need to know the position of the result, or aString.match if you need to collect matching substrings (delimited by parentheses in the regular expression). Regular expressions are less useful if the match is unknown in advance, or to extract substrings in known positions in the string. For instance, aString.slice(-1) returns the last letter in aString, or the empty string if aString is empty. 

### Java practices

- We use the (https://www.oracle.com/technetwork/java/codeconvtoc-136057.html "Java Coding Style"). Quick summary:
-- FirstLetterUpperCase for class names.
-- camelCase for method and variable names.
-- One declaration per line:
     ```int x, y; // this is BAD!
     int a;    // split it over
     int b;    // two lines
```
- Braces should be placed like so (generally, opening braces on same line, closing braces on a new line):
```
public void func(int arg) {
    if (arg != 0) {
        while (arg > 0) {
            arg--;
        }
    } else {
        arg++;
    }
}
```
- Places we differ from the Java coding style:
-- Start class variable names with 'm' prefix (e.g. mSomeClassVariable) and static variables with 's' prefix (e.g. sSomeStaticVariable)
-- import statements:
--- Do not use wildcard imports like `import java.util.*;`
--- Organize imports by blocks separated by empty line: org.mozilla.*, com.*, net.*, org.*, android.*, then java.*
--- Within each import block, alphabetize import names with uppercase before lowercase. For example, com.example.Foo is before com.example.bar
--- 4-space indents.
--- Spaces, not tabs.
--- Don't restrict yourself to 80-character lines. Google's Android style guide suggests 100-character lines, which is also the default setting in Android Studio. Java code tends to be long horizontally, so use appropriate judgement when wrapping. Avoid deep indents on wrapping. Note that aligning the wrapped part of a line, with some previous part of the line (rather than just using a fixed indent), may require shifting the code every time the line changes, resulting in spurious whitespace changes.
- For additional specifics on Firefox for Android, see the Coding Style guide for Firefox on Android.
- The (https://source.android.com/source/code-style.html "Android Coding Style has some useful guidelines too").

### Python practices

- Install the mozext Mercurial extension, and address every issue reported on commit, qrefresh, or the output of hg critic.
- Follow (https://www.python.org/dev/peps/pep-0008/ "PEP 8").
- Do not place statements on the same line as if/elif/else conditionals to form a one-liner.
- Global vars, please avoid them at all cost.
- Exclude outer parenthesis from conditionals.  Use if x > 5:, rather than if (x > 5):
- Use string formatters, rather than var + str(val).  var = 'Type %s value is %d' % ('int', 5).
- Utilize tools like (https://pypi.python.org/pypi/pylint "pylint") or (http://pychecker.sourceforge.net/ "pychecker") to screen sources for common problems.
- Testing/Unit tests, please write them.

### Error handling

Check for errors early and often
You need to do this even if you know that call will never fail. Why?

- Someone may change the callee in the future to return a failure condition.
- The object in question may live on another thread, another process, or possibly even another machine. The proxy could have failed to make your call in the first place.

Also, when you make a new function which is failable (i.e. it will return a nsresult or a bool that may indicate an error), you should explicitly mark the return value should always be checked. 

### C++ strings

Use the Auto form of strings for local values

When declaring a local, short-lived nsString class, always use nsAutoString or nsAutoCString. These pre-allocate a 64-byte buffer on the stack, and avoid fragmenting the heap. Don't do this:

```
nsresult
foo()
{
  nsCString bar;
  ..
}
```

instead:

```
nsresult
foo()
{
  nsAutoCString bar;
  ..
}
```

### Java Code (Old version)

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
