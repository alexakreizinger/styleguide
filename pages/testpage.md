---
layout: default
permalink: /testpage/
title: Test Page Yay!
testVar: {{ page.title }}
testDomain: zombo
---

beep beep ribby ribby
{% include testinclude.md %}

The title of this page is {{ page.testVar | liquify }}