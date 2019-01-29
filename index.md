---
title: Home
---
{% for rule in site.rules %}
  {{ rule | jsonify }}
{% endfor %}
