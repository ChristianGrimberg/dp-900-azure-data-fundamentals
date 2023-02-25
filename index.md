---
permalink: index.html
layout: home
---

# DP-900: Aspectos básicos de los datos en Microsoft Azure

## Documentación relacionada del sitio de [Microsoft Docs](https://learn.microsoft.com/es-es/certifications/exams/dp-900/)

## Módulos de aprendisaje

{% assign modules = site.pages | where_exp: "page", "page.url contains '/pages/docs'" %}
{% for activity in modules %}{% if activity.document.dp900Title %}* [{{ activity.document.dp900Title }}]({{ site.github.url }}{{ activity.url }})
{% endif %}{% endfor %}