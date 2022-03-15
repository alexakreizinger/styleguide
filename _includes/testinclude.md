{% for item in site.data.test %}
{{ item | liquify }}
{% endfor %}

{% for item in site.data.test %}
{{ item | liquify | markdownify}}
{% endfor %}

{% for item in site.data.test %}
{{ item }}
{% endfor %}