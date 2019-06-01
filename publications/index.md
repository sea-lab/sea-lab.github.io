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

{% if paper.link %}[<img src="/assets/images/fulltext.svg" alt="Full Text" style="display: inline; width:32px; height:32px;" />]({{paper.link}}){% endif %} {% if paper.poster %}[<img src="/assets/images/poster.svg" alt="Poster" style="display: inline; width:32px; height:32px;" />]({{ paper.poster }}){% endif %} {% if paper.presentation %}[<img src="/assets/images/presentation.svg" alt="Slides"  style="display: inline; width:32px; height:32px;" />]({{ paper.presentation }}){% endif %}
{% endfor %}

{% endfor %}