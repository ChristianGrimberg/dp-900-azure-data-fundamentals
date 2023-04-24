---
permalink: index.html
layout: home
---

# DP-900: Aspectos básicos de los datos en Microsoft Azure

* [Exámen de certificación DP-900](https://learn.microsoft.com/es-es/certifications/exams/dp-900/)
* [Guía de estudio para el exámen DP-900](https://learn.microsoft.com/es-es/certifications/resources/study-guides/dp-900)
* [Evaluaciones de prácticas para certificaciones de Microsoft](https://learn.microsoft.com/es-es/certifications/practice-assessments-for-microsoft-certifications)
* [Poster de certificaciones de Microsoft](https://aka.ms/traincertposter)

## Módulos de aprendisaje

{% assign modules = site.pages | where_exp: "page", "page.url contains '/pages/docs'" %}
| Sección | Unidad | Descripción |
| ------- | ------ | ----------- |
{% for activity in modules %}{% if activity.document.dp900Title %}| {{ activity.document.dp900Module }} | {{ activity.document.dp900Unit }} | [{{ activity.document.dp900Title }}]({{ site.github.url }}{{ activity.url }}) |
{% endif %}{% endfor %}
