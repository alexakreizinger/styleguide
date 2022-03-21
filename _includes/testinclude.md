{% for item in site.data.test %}
{{ item | liquify }}
{% endfor %}