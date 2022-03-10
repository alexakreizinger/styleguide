---
permalink: /all/grammar/
---
## Abbreviations
{% for style in site.data.grammar.abbreviations %}
  {{ style.rule }}
  {% for example in style.examples %}
    - {{ example }}
  {% endfor %}
{% endfor %}

## Active Voice
{% for style in site.data.grammar.active_voice %}
  {{ style.rule }}
  {% for example in style %}
  - {{ style.example }}
  {% endfor %}
{% endfor %}

## Capitalization
{% for style in site.data.grammar.capitalization %}
  {{ style.rule }}
  {% for example in style %}
  - {{ style.example }}
  {% endfor %}
{% endfor %}
