---
layout: default
permalink: /testpage/
title: Test Page Yay!
testVar: {{ page.title }}
---

beep beep ribby ribby
{% include testinclude.md x="zombo" %}

The title of this page is {{ testVar | liquify }}