---
layout: default
title: Home
---

# Welcome to My Food Blog

{% for post in site.posts %}
## [{{ post.title }}]({{ post.url }})
{{ post.date | date: "%B %d, %Y" }} | {{ post.cuisine }} | {{ post.city }}
{% endfor %}