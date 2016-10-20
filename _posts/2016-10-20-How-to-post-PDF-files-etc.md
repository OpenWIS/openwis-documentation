---
layout: page
title: How to post PDF files etc
---

- Go to https://github.com/OpenWIS/openwis-documentation/
- Select the gh-pages branch - it is this branch you need to update, not the master.
- Click the assets folder
- Upload your PDF to the _assets_ folder
- Click the _posts_ folder to list the posts.
- Click the 'Create new file' button, top right.
- Name the file. You must use this pattern: YYYY-MM-DD-your-file-name.md, where YYYY-MM-DD is the year, month, day of the post, usually today's date, and the file type is .md for Markdown.
- Add the yaml front-matter as shown below, dashes included, but of course with your own post title. This yaml block must be the first thing in the file.

```yaml
    ---
    layout: page
    title: 2016 OpenWIS DevCon Workshop Final Report
    ---
```

- Then write the intro text of your post, using Markdown or GitHub Flavored Markdown (GFM).
- Then insert a link to your PDF, like this:

```
The report in PDF format can be downloaded [here][here].
```

The first [here] is the word that will appear as the clickable link in your article and can be anything you like.  The second [here] is a reference to where the link can be resolved within this document, and can also be any text you want; it will not appear in your rendered document.

```
[here]: {{ site.baseurl | prepend: site.url }}/assets/OpenWIS-Developer-Conference-2016.pdf
```

 The third [here] is the link resolution label and must match the second [here] which is pointing to it.  In this case the link resolution tells Jekyll that your PDF is in the assets folder of the same website, the stuff in curly brackets is placeholders for the site path that are substituted by Jekyll when it renders your document.  The line that resolves the link can also be anywhere in your doc, but it usually makes sense to put the link resolutions at the foot of the doc or some other obvious place you can find them.  Of course the file name of your PDF in the link resolution must match the actual filename in the assets folder.  The entire link resolution line will not appear in your rendered document.

- You can use the Preview button to see how it looks.
- Once you're happy, fill-in the Commit details box below the editor and commit directly to the gh-pages branch.
- Visit the blog to check all is ok, you can re-edit and re-commit as many times as you like to make changes, then you're done!
