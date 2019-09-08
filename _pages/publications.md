---
title: "Publications"
layout: gridlay
excerpt: "Martin Pinzger - Publications"
sitemap: false
permalink: /publications/
---


# Publications

We include the publications on this page to ensure timely dissemination on a noncommercial basis. Copyright and all rights therein are maintained by the authors or by other copyright holders, notwithstanding that they have offered their publications here electronically. It is understood that all persons copying this information will adhere to the terms and constraints invoked by the copyrights. These publications may not be reposted without the explicit permission of the copyright holder.

## Recent Publications
For the [full list of publications](#full-list) see below or check my profile on [DBLP](http://dblp.uni-trier.de/pers/hd/p/Pinzger_0001:Martin) and [Google Scholar](http://scholar.google.com/citations?user=MTZ0l60AAAAJ&hl=en)

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
  {% if publi.image != %} <img src="{{ site.url }}{{ site.baseurl }}/images/pubpics/{{ publi.image }}" class="img-responsive" width="50%" style="float: left" /> {% endif %}
  <p>{{ publi.description }}</p>
  <p>{{ publi.authors }} {% if publi.link.url != %}(<a href="{{ publi.link.url }}">{{ publi.link.display }}</a>){% endif %}</p>
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


## Full List ##

{% for publi in site.data.publist %}

  <strong>{{ publi.title }} </strong> {% if publi.link.url != %} (<a href="{{ publi.link.url }}">{{ publi.link.display }}</a>) {% endif %} <br /> 
  {{ publi.authors }}. {{ publi.proceedings }}, {{ publi.pages }}, {{ publi.publisher }}, {{ publi.year }}. {% if publi.award != %} <strong>{{ publi.award }}</strong> {% endif %}


{% endfor %}

## Theses
<strong>ArchView - Analyzing Evolutionary Aspects of Complex Software Systems</strong> (<a href="../papers/Pinzger2005-phdthesis.pdf">pdf</a>) <br />
M. Pinzger. Doctoral Thesis, Vienna University of Technology, 2005.

<strong>Reengineering von Flugplanungssoftware</strong> (in German) <br />
M. Pinzger. Master’s Thesis, EADS Dornier GmbH and Vienna University of Technology, 2001.
