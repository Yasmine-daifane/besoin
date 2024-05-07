---
layout: default
order: 1
---
{% assign pages = site.pages | sort: "order" %}
{% for page in pages %}
  {% if  page.package == "Pôle-sociale" %}
    {{- page.content | markdownify -}}
  {% endif %}
{% endfor %}
