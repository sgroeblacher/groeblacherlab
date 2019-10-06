---
title: "Groeblacher Lab - Publications"
layout: gridlay
excerpt: "Groeblacher Lab -- Publications."
sitemap: false
permalink: /publications/
---


# Publications

## Highlights

(For a full list see [below](#list-of-publications) or go to [Google Scholar](https://scholar.google.com/citations?user=3FNLMXkAAAAJ) or [arXiv](https://arxiv.org/a/groblacher_s_1))

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


## List of publications
\* <em>indicates equal contribution</em>

{% for publi in site.data.publist %}

{% if publi.newyear == 1 %}
#### {{ publi.year }} 
{% endif %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>{% if publi.arxiv == 1 %} [<a href="{{ publi.eprint }}">e-print</a>]{% endif %}<br/>
  {{ publi.news2 }}

{% endfor %}

