---
layout: default
permalink: /all/
title: All Rules
nav_exclude: true
search_exclude: true
---
All rules for all audiences. 

# Grammar
{% assign file = site.data.stylerules.grammar %}

{% include get_all_rules.md filename=file %}