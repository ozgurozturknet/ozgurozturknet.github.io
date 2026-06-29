---
layout: default
title: Blog
---

# Blog

Thoughts on cloud-native, DevOps, platform engineering, and building things that work.

{% for post in site.posts %}
<article style="padding: 16px 0; border-bottom: 1px solid var(--border);">
  <span style="font-size:0.9em;color:var(--muted);">{{ post.date | date: "%b %d, %Y" }}</span>
  <h2 style="font-size:1.1em; margin: 4px 0;"><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <p style="font-size:0.9em;color:var(--muted);">{{ post.excerpt | strip_html | truncate: 150 }}</p>
</article>
{% endfor %}

{% if site.posts.size == 0 %}
<p style="color:var(--muted);">No posts yet. Coming soon.</p>
{% endif %}
