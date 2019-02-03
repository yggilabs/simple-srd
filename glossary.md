---
title: Glossary
---
{% assign glossary = site.data.glossary %}
<dl>
{% for item in glossary %}
  {% assign names = item.name %}
  {% assign def = item.def %}
  {% for name in names %}
  <dt><dfn{% if forloop.first %} id="{{ name | slugify }}"{% endif %}>{{ name }}</dfn></dt>
  {% endfor %}
  <dd>

{{ def }}

  </dd>
{% endfor %}
</dl>
