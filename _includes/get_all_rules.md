{% for style in include.filename %}
## {{ style.section }}
{% for rule in style.topics.rule %}
* {{ rule }}
{% for example in style.topics.rule.example %}
> {{ example }}
{% endfor %}
{% endfor %}
{% endfor %}