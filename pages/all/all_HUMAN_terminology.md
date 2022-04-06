---
layout: default
permalink: /all/human-terminology/
title: HUMAN Terminology
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

![construction pikachu]({{ site.url }}{{ site.baseurl }}/assets/images/construction.gif)

{% assign file = site.data.stylerules.HUMAN_terminology %}

{% include get_all_rules.md filename=file %}
