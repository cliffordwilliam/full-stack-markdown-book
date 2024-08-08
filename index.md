---
layout: page
title: "Home"
permalink: /
---

{% for post in site.posts %}
  * {{ post.date | date: "%B %d, %Y" }} [{{ post.title }}]({{ post.url }})
{% else %}
  No posts found.
{% endfor %}
