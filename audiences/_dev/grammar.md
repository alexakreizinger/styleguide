---
permalink: /dev/grammar
---
## Abbreviations
{% for style in site.data.grammar.abbreviations %}
{{ style.rule }}
{{ style.example }}
{% endfor %}

## Active Voice
{% for style in site.data.grammar.active_voice %}
{{ style.rule }}
{{ style.example }}
{% endfor %}
