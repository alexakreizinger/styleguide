---
layout: default
permalink: /dev/tone_and_content/
title: Tone and Content
parent: Developers
audience: dev
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

{% assign file = site.data.stylerules.tone_and_content %}
{% assign aud = page.audience %}

{% include get_rules_for_audience.md filename=file audience=aud %}