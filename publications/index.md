---
layout: page
current: publications
title: Publications
navigation: true
logo: 'assets/images/ghost.png'
class: page-template
subclass: 'post page'
---
{% for year in site.data.papers %}
## {{ year[0] }}
{% for paper in year[1] %}
{% if paper.link %}
[{{paper.title}}]({{paper.link}})
{%else%}
{{paper.title}}
{%endif%}<small> at {{ paper.venue }}</small><br />
<small>{{paper.authors | join: ', ' }}</small>
{% endfor %}

{% endfor %}