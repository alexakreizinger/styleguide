---
layout: default
permalink: /dev/
title: Developers
has_children: true
has_toc: false
search_exclude: true
audience: dev
nav_order: 3
---
# {{page.title}}

{% assign aud = page.audience %}
{% assign file1 = site.data.stylerules.formatting_and_organization %}
{% assign section1 = "Formatting and organization" %}
{% capture link1 %}{{site.baseurl}}{{page.permalink}}formatting-and-organization/{% endcapture %}
{% assign file2 = site.data.stylerules.grammar %}
{% assign section2 = "Grammar" %}
{% capture link2 %}{{site.baseurl}}{{page.permalink}}grammar/{% endcapture %}
{% assign file3 = site.data.stylerules.tone_and_content %}
{% assign section3 = "Tone and content" %}
{% capture link3 %}{{site.baseurl}}{{page.permalink}}tone-and-content/{% endcapture %}

## Quick tips
{% include get_featured_rules_for_audience.md filename=file1 audience=aud sectionname=section1 sectionlink=link1 %}
{% include get_featured_rules_for_audience.md filename=file2 audience=aud sectionname=section2 sectionlink=link2 %}
{% include get_featured_rules_for_audience.md filename=file3 audience=aud sectionname=section3 sectionlink=link3 %}