{% for style in include.filename %}
## {{ style.section }}
{% for rule in style.topics.rule %}
{% if rule.audience contains include.audience %}
* {{ rule }}
{% for example in style.topics.rule.example %}
> {{ example }}
{% endfor %}
{% endif }
{% endfor %}
{% endfor %}