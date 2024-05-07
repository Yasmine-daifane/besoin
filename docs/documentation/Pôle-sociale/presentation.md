---
layout: presentation
order: 1
---

{% assign pages = site.pages | sort: "order" %}
{% for page in pages %}
  {% if page.presentation or page.presentationPackage == "Pôle-sociale" %}
    {{- page.content | markdownify -}}
  {% endif %}
{% endfor %}