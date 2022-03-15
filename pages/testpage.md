---
layout: default
permalink: /testpage/
---

beep beep ribby ribby

{% for item in site.data.test %}
{{ item | liquify }}
{% endfor %}

{% for item in site.data.test %}
{{ item }}
{% endfor %}