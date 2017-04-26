---
layout: default
discourse: true
discourseid: 0
---
# test-discourse plugin

I am going to attempt embedding a thread from Discourse below:
***
{% if page.discourse %}
<div id='discourse-comments'></div>
<!-- discourseEmbedUrl: 'http://140.90.90.171:4000/test/discourse.html' -->
<script type="text/javascript">

  DiscourseEmbed = {};
  DiscourseEmbed.discourseUrl = 'http://metocean.afvt.mdl.nws.noaa.gov/';
  {% if page.discourseid == 0 %}
      DiscourseEmbed.discourseEmbedUrl = '{{ site.url }}{{ page.url }}';
  {% else %}
      DiscourseEmbed.topicId = {{ page.discourseid }};
  {% endif %}

  (function() {
    var d = document.createElement('script'); d.type = 'text/javascript'; d.async = true;
    d.src = DiscourseEmbed.discourseUrl + 'javascripts/embed.js';
    (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(d);
  })();
function showComments(topic) {
  var comments = document.getElementById('discourse-comments');
  var iframe = document.getElementById('discourse-embed-frame');
  if (iframe) { iframe.remove(); }
  iframe.id = 'discourse-embed-frame';
  iframe.width = '100%';
  iframe.frameBorder = '0';
  iframe.scrolling = 'yes';
  comments.appendChild(iframe);
  iFrameResize({}, iframe);
};
showComments({{ url }});
</script>
{% endif %}
***

