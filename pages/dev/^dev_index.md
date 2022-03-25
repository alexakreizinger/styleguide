---
layout: default
permalink: /dev/
title: Developers
has_children: true
audience: dev
---
# {{page.title}}

{% assign file = site.data.stylerules.grammar %}
{% assign aud = page.audience %}

{% include get_featured_rules_for_audience.md filename=file audience=aud sectionname="Grammar" %}