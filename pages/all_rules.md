---
layout: default
permalink: /all/
title: All Rules
nav_exclude: true
search_exclude: true
# this page is designed to generate all rules for all audiences ON A SINGLE PAGE (no parent/child subpages)
---
All rules for all audiences.

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

# Grammar
{% assign file = site.data.stylerules.grammar %}

{% include get_all_rules.md filename=file %}