---
title: "News"
layout: textlay
excerpt: "Groeblacher Lab at Delft University of Technology."
sitemap: false
permalink: /allnews.html
---

# News

{% for article in site.data.news %}
<p><b>{{ article.date }}</b><br>
<em>{{ article.headline }}</em></p>
{% endfor %}
