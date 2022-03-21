---
layout: default
permalink: /marketing/grammar/
title: Grammar
parent: Marketers
audience: mktg
---
# {{page.title}}
{% assign file = site.data.stylerules.grammar %}
{% assign aud = page.audience %}

{% include get_rules_for_audience.md filename=file audience=aud %}