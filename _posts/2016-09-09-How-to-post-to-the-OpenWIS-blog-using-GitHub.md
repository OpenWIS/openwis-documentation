---
layout: page
title: How to post to the OpenWIS blog using GitHub
---

- Go to https://github.com/OpenWIS/openwis-documentation/
- Select the gh-pages branch - it is this branch you need to update, not the master.
- Click the _posts folder to list the posts.
- Click the 'Create new file' button, top right.
- Name the file. You must use this pattern: YYYY-MM-DD-your-file-name.md, where YYYY-MM-DD is the year, month, day of the post, usually today's date, and the file type is .md for Markdown.
- Add the yaml front-matter as shown below, dashes included, but of course with your own post title. This yaml block must be the first thing in the file.

```yaml
    ---
    layout: page
    title: How to post to the OpenWIS blog using GitHub
    ---
```

- Then write the body text of your post, using Markdown or GitHub Flavored Markdown (GFM).
- You can use the Preview button to see how it looks.
- Once you're happy, fill-in the Commit details box below the editor and commit directly to the gh-pages branch.
- Visit the blog to check all is ok, you can re-edit and re-commit as many times as you like to make changes, then you're done!
