---
layout: default
permalink: /marketing/grammar/
---

{% assign file = site.data.grammar %}
{% assign aud = "marketing" %}

{% include get_rules_for_audience.md filename=file audience=aud %}