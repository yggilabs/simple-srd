---
title: Home
---
{{ site.rules | inspect }}
{% for rule in site.rules %}
  {{ rule | inspect }}
{% endfor %}
