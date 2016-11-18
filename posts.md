---
layout: page
title: Github Page Posts
# This generates a directory /posts/ with an index.html file containing the html output from the for loop below, which list all the files in _posts
permalink: /posts/
---

<div class="posts-index">
	{% for post in site.posts %}
		<li>
			<a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
		</li>
	{% endfor %}
</div>
