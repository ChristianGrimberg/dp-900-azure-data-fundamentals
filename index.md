---
permalink: index.html
layout: home
---

# DP-900: Aspectos básicos de los datos en Microsoft Azure

* [Exámen de certificación DP-900](https://learn.microsoft.com/es-es/certifications/exams/dp-900/)
* [Guía de estudio para el exámen DP-900](https://learn.microsoft.com/es-es/certifications/resources/study-guides/dp-900)

## Módulos de aprendisaje

{% assign modules = site.pages | where_exp: "page", "page.url contains '/pages/docs'" %}
| Módulo | Unidad |
| ------ | ------ |
{% for activity in modules %}{% if activity.document.dp900Title %}| {{ activity.document.dp900Module }} | [{{ activity.document.dp900Title }}]({{ site.github.url }}{{ activity.url }}) |
{% endif %}{% endfor %}
