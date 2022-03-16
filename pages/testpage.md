---
layout: default
permalink: /testpage/
title: Test Page Yay!
testVar: |
    {{ page.title }}
testVar2: hi
---

beep beep ribby ribby

{% include testinclude.md x="zombo" %}

{% include testinclude.md x=zombo %}

The title of this page is {{ page.testVar | liquify }}