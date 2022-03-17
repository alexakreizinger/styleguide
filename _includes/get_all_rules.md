{% for sect in include.filename %}
## {{ sect.section }}
    {% for stylerule in sect.topics %}
* {{ stylerule.rule }}
        {% for ex in stylerule.examples %}
    * {{ ex }}  {::comment} the two trailing spaces at the end are important! (otherwise you can't properly render multiline bullet points) {:/comment}
        {% endfor %}
    {% endfor %}
{% endfor %}