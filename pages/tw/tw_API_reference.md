---
layout: default
permalink: /techdocs/api-reference/
title: API Reference
parent: Technical Writers
audience: tw
nav_order: 7
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
{% assign aud = page.audience %}

{% include get_rules_for_audience.md filename=file audience=aud %}