---
title: Exercices d’exploration des connaissances Azure
permalink: index.html
layout: home
---

# Exercices d’exploration des connaissances Azure

Les exercices suivants sont conçus pour prendre en charge les modules sur Microsoft Learn.

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Exercises'" %} {% for activity in labs  %} {% if activity.url contains 'ai-foundry' %} {% continue %} {% endif %}
- [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) {% endfor %}
