---
layout: default
---

# Writings

{% for category in site.writings %}
<a href="{{category.url}}">{{category.title}}</a>
{% endfor %}
