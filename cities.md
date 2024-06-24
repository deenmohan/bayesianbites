---
layout: default
title: Cities
---

# 

{% assign citys = site.posts | map: "city" | uniq | sort %}
{% for city in citys %}
## {{ city }}
{% for post in site.posts %}
{% if post.city == city %}
- [{{ post.title }}]({{ post.url }})
{% endif %}
{% endfor %}
{% endfor %}