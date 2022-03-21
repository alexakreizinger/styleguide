---
layout: default
permalink: /techdocs/grammar/
title: Grammar
parent: Technical Writers
audience: tw
---
# {{page.title}}
{% assign file = site.data.stylerules.grammar %}
{% assign aud = page.audience %}

{% include get_rules_for_audience.md filename=file audience=aud %}