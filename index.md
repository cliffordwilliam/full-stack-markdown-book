---
layout: page
title: "Home"
permalink: /
---

## Chapters

{% for post in site.posts %}
  * {{ post.date | date: "%B %d, %Y" }} [{{ post.title }}]({{ post.url | relative_url }})
{% else %}
  No posts found.
{% endfor %}
