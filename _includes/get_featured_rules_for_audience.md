{% for x in include.filename %}
    {% if x.topics.audience contains include.audience and x.featured == true %}
### [{{ include.sectionname }}]({{ include.sectionlink }})
        {% break %}
        {% endif %}
{% endfor %}

{% for sect in include.filename %}
    {% for stylerule in sect.topics %}
        {% if stylerule.audience contains include.audience and stylerule.featured == true %}
* {{ stylerule.featured_text | liquify }}
        {% endif %}
    {% endfor %}
{% endfor %}