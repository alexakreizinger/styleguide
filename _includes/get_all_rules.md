{% for sect in include.filename %}
## {{ sect.section }}
    {% for stylerule in sect.topics %}
* {{ stylerule.rule }}
        {% for ex in stylerule.examples %}
    * {{ ex }}
        {% endfor %}
    {% endfor %}
{% endfor %}