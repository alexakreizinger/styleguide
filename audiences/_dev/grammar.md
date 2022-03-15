---
layout: default
permalink: /dev/grammar/
---

{% assign file = site.data.grammar %}
{% assign aud = "dev" %}

{% include get_rules_for_audience.md filename=file audience=aud %}