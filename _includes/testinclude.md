---
testDomain: "zombo"
---

{% for item in site.data.test %}
{{ item | liquify }}
{% endfor %}

{% for item in site.data.test %}
{{ item }}
{% endfor %}