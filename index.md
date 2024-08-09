---
layout: page
title: "Home"
permalink: /
---

## Welcome

Start learning from 0 to make a 100% real working website here, everything you need is here. Contents are all based on [Odin Project](https://www.theodinproject.com). This site is free and serves as a summary.

## About Odin Project

The Odin Project is a free open-source community founded in 2013, it provides free knowledge to be an employable and self sufficient web developer. It uses the best resources that is maintained to stay up to date by professionals volunteers, some were Odin Project graduates.

Unlike other courses, Odin Project has a real world approach to learning to get you employed, it gives learner a chance to create real world web applications for portfolio and thus it trains their problem solving skills. There is no certificante since employers value good portfolio over certificates. Consider contributing to Odin Project as it makes your resume looks better.

Odin Project contacts:
- [Email](mailto:theodinprojectcontact@gmail.com)
- [Discord](https://discord.gg/fbFCkYabZB)

## Chapters

{% assign reversed_posts = site.posts | reverse %}
<ol>
{% for post in reversed_posts %}
  <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
{% else %}
  <li>No posts found.</li>
{% endfor %}
</ol>

