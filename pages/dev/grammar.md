---
layout: default
permalink: /dev/grammar/
title: Grammar
parent: Developers
---
# Grammar
{% assign file = site.data.stylerules.grammar %}
{% assign aud = "dev" %}

{% include get_rules_for_audience.md filename=file audience=aud %}