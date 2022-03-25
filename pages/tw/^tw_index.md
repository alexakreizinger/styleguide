---
layout: default
permalink: /techdocs/
title: Technical Writers
has_children: true
has_toc: false
audience: tw
---
# {{page.title}}

{% assign file1 = site.data.stylerules.grammar %}
{% assign file2 = site.data.stylerules.tone_and_content %}
{% assign aud = page.audience %}

## Quick tips
{% include get_featured_rules_for_audience.md filename=file1 audience=aud sectionname="Grammar" %}
{% include get_featured_rules_for_audience.md filename=file2 audience=aud sectionname="Grammar" %}