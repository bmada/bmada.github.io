---
layout: page
title: Glossary
permalink: /glossary/
---

Welcome. Here is an evolving glossary for mathematical terms.

{% assign groups = site.glossary | group_by: "category" | sort: "name" %}
{% for group in groups %}
<h1>{{ group.name }}</h1>

 {% for item in group.items %}
 - [{{ item.title }}]({{ item.url }})
 {%endfor%}
{%endfor%}