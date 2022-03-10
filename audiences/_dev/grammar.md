---
permalink: /dev/grammar/
---
## Abbreviations
{% for item in site.data.grammar.abbreviations %}
  "{ abbreviation.rule }}
  {{ abbreviation.example }}
{% endfor %}

## Active Voice
{% for voice in site.data.grammar.active_voice %}
  {{ voice.rule }}
  {{ voice.example }}
{% endfor %}
