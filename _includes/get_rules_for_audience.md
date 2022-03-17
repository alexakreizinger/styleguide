{% for sect in include.filename %}
    {% for stylerule in sect.topics %}
        {% if stylerule.audience contains include.audience %}
## {{ sect.section }}
{% break %}
        {% endif %}
    {% endfor %}
    {% for stylerule in sect.topics %}
        {% if stylerule.audience contains include.audience %}
* {{ stylerule.rule }}
            {% for ex in stylerule.examples %}
    * {{ ex }}  {::comment} the two trailing spaces at the end are important! (otherwise you can't properly render multiline bullet points) {:/comment}
            {% endfor %}
        {% endif %}
    {% endfor %}
{% endfor %}