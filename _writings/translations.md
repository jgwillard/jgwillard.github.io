---
title: Translations
layout: default
---

# Translations

{% for work in site.translations %}

- [{{work.title}}]({{work.url}})

{% endfor %}

{% include back_to_writings.html %}
