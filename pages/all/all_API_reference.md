---
layout: default
permalink: /all/api-reference/
title: API Reference
parent: All
nav_exclude: true
search_exclude: true
---
# {{page.title}} 
{: .no_toc }
<details markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

{% assign file = site.data.stylerules.API_reference %}

{% include get_all_rules.md filename=file %}