---
title: Home
---

{% assign rules_urls = site.rules | map: "url" %}

{{ rules_urls | group_by_exp:"item", "item | split: '/' | unshift | unshift " | jsonify }}
