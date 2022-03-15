---
layout: default
permalink: /dev/grammar/
---

{% assign file = site.data.grammarWIPtest %}
{% assign aud = dev %}

{% include get_rules_for_audience.md filename=file audience=aud %}
