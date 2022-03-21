---
layout: default
permalink: /dev/grammar/
title: Grammar
parent: Developers
audience: dev
---
# {{page.title}}
{% assign file = site.data.stylerules.grammar %}
{% assign aud = page.audience %}

{% include get_rules_for_audience.md filename=file audience=aud %}