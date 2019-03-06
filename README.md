# openwis-documentation

The website at http://openwis.github.io/openwis-documentation/ is where the public documents about the OpenWIS Association AISBL are maintained; this is the project repository for that website.

This project uses [Jekyll](https://jekyllrb.com/) to build HTML documentation from [Markdown](https://daringfireball.net/projects/markdown/). The early stages of this project will concentrate on documenting the governance framework of the OpenWIS Association. More will be added as time goes on ...

For tips on writing [Markdown](https://daringfireball.net/projects/markdown/) see the [GitHub guide](https://guides.github.com/features/mastering-markdown/).

To build the documentation site, we're using the `github-pages` gem from GitHub and [Bundler](http://bundler.io/). More information about using Jekyll with GitHub-Pages can be found [here](https://jekyllrb.com/docs/github-pages/). There is more to building the sources from the command line than simply "bundle exec jekyll build".  First you must clone the "openwis-documentation" sources!

```
git clone https://<user>@github.com/OpenWIS/openwis-documentation
```
For a brand new "cloned" repository, the build is likely to fail with the following message:

```
[mgiannoni@jekyll openwis-documentation]$ bundle exec jekyll build
Could not locate Gemfile or .bundle/ directory
```
For this case run the follwoing:

```
jekyll new . --force
```
Not the sources should build correctly with:

```
bundle exec jekyll build
```

However you will probably wish to examine your changes prior to publishing them to GitHub.  To accomplish this you will need to edit "_config.yml"

```
UNCOMMENT next line before publishing to GitHub!!!  REcomment to run local tests with Jekyll serve
baseurl: "/openwis-documentation"

UNCOMMENT next line before publishing to GitHub!!!  REcomment to run local tests with Jekyll serve
url: "http://openwis.github.io"
```

Then to view the site from "http://127.0.0.1:4000"

```
bundle exec jekyll serve
```

Copyright and License
---------------------
(C) Copyright OpenWIS Association AISBL.

OpenWIS® is free software: you can redistribute it and/or modify it under the terms of the License specified for each OpenWIS® Project (see [LICENSE](./LICENSE)).
