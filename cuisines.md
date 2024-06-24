---
layout: default
title: Cuisines
---

# Cuisines

{% assign cuisines = site.posts | map: "cuisine" | uniq | sort %}
{% for cuisine in cuisines %}
## {{ cuisine }}
{% for post in site.posts %}
{% if post.cuisine == cuisine %}
- [{{ post.title }}]({{ post.url }})
{% endif %}
{% endfor %}
{% endfor %}