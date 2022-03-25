{% for sect in include.filename %}
    {% for stylerule in sect.topics %}
        {% if stylerule.audience contains include.audience and stylerule.featured == true %}
### [{{ include.sectionname }}]({{ include.sectionlink }})
{% break %}
        {% endif %}
    {% endfor %}
    {% for stylerule in sect.topics %}
        {% if stylerule.audience contains include.audience and stylerule.featured == true %}
* {{ stylerule.featured_text }}
        {% endif %}
    {% endfor %}
{% endfor %}
