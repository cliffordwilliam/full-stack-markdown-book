---
layout: page
title: "Home"
permalink: /
---

# Welcome to My Blog

{% for post in site.posts %}
  * {{ post.date | date: "%B %d, %Y" }} [{{ post.title }}]({{ post.url }})
{% else %}
  No posts found.
{% endfor %}

