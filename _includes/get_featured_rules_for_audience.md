{% for sect in include.filename %}
    {% for stylerule in sect.topics %}
        {% if stylerule.audience contains include.audience and stylerule.featured == true %}
## {{ include.sectionname }}
{% break %}
        {% endif %}
    {% endfor %}
    {% for stylerule in sect.topics %}
        {% if stylerule.audience contains include.audience and stylerule.featured == true %}
* {{ stylerule.featured_rule }}
        {% endif %}
    {% endfor %}
{% endfor %}