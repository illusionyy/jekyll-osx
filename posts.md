---
layout: default
title: Posts
permalink: /posts/
---

# Posts

<ul class="posts-list">
{% for post in site.posts %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <div class="post-date">{{ post.date | date: "%B %-d, %Y" }}</div>
    {% if post.excerpt %}
    <div class="post-excerpt">{{ post.excerpt | strip_html | truncate: 160 }}</div>
    {% endif %}
  </li>
{% endfor %}
{% if site.posts.size == 0 %}
  <li style="color:#888; font-size:11px;">No posts yet. Add <code>.md</code> files to <code>_posts/</code> to get started.</li>
{% endif %}
</ul>
