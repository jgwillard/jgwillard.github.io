---
title: Translations
layout: default
---

# Translations

{% for work in site.translations %}
<a href="{{work.url}}">{{work.title}}</a>
{% endfor %}
