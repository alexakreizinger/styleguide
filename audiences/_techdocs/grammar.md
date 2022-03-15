---
layout: default
permalink: /techdocs/grammar/
---
{% assign file = site.data.grammar %}
{% assign aud = "techdocs" %}

{% include get_rules_for_audience.md filename=file audience=aud %}