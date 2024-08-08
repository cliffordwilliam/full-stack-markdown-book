---
layout: default
title: "Home"
---

# Welcome to My Blog

{% for post in site.posts %}
  * {{ post.date | date: "%B %d, %Y" }} [{{ post.title }}]({{ post.url }})
{% endfor %}
