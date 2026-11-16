---
layout: page
title: Leyes
permalink: /leyes/
---

| Ley | Informe | Publicación en el BO |
|---|---|---|
{% for p in site.categories.leyes %}| {{ p.ley }} | [{{ p.title }}]({{ p.url | relative_url }}) | {{ p.date | date: "%d/%m/%Y" }} |
{% endfor %}
