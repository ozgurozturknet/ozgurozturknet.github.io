---
layout: default
title: Blog
---

# Blog & Content

I create educational content on cloud-native technologies, DevOps, and platform engineering. You can also find me on [YouTube](https://www.youtube.com/@ayti.tech) and [Udemy](https://www.udemy.com/user/zgrztrk3/).

---

{% for post in site.posts %}
<article style="padding: 16px 0; border-bottom: 1px solid var(--border);">
  <span class="post-meta">{{ post.date | date: "%b %d, %Y" }}</span>
  <h2 style="font-size:1.1em; margin: 4px 0;"><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 150 }}</p>
</article>
{% endfor %}

{% if site.posts.size == 0 %}
<p style="color:var(--muted);">No posts yet. Coming soon.</p>
{% endif %}
