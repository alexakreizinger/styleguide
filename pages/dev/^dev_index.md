---
layout: default
permalink: /dev/
title: Developers
has_children: true
has_toc: false
audience: dev
---
# {{page.title}}

{% assign file1 = site.data.stylerules.grammar %}
{% assign section1 = "Grammar" %}
{% capture link1 %}{{site.baseurl}}{{page.permalink}}grammar/{% endcapture %}
{% assign file2 = site.data.stylerules.tone_and_content %}
{% assign section2 = "Tone and content" %}
{% capture link2 %}{{site.baseurl}}{{page.permalink}}tone-and-content/{% endcapture %}
{% assign aud = page.audience %}

## Quick tips
{% include get_featured_rules_for_audience.md filename=file1 audience=aud sectionname=section1 sectionlink=link1 %}
{% include get_featured_rules_for_audience.md filename=file2 audience=aud sectionname=section2 sectionlink=link2 %}