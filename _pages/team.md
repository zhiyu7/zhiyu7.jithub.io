---
title: "Team"
layout: gridlay
sitemap: false
permalink: /team/
---

## Team

<!-- Remove PI section entirely -->
<!-- Removed the PI section as requested -->

## Students

<div class='jumbotron'>
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-2">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-4 col-xs-12">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br></i>

  <!-- Remove email and homepage links -->
  <!-- Remove: {% if member.website %}<a href="{{ member.website }}" target="_blank"><i class="fa fa-home fa-2x"></i></a> {% endif %} -->
  <!-- Remove: {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-2x"></i></a> {% endif %} -->

  <p><strong>Current:</strong> {{ member.current_degree }}</p>
  <p><strong>Previously:</strong> {{ member.previously_degree }}</p> <!-- Corrected this line -->
  
</div>
<!-- </div> -->

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
</div>

## Other <!-- Change "Alumni" to "Thesis Committee" -->

<div class='jumbotron'>
{% assign number_printed = 0 %}
{% for member in site.data.alumni %} <!-- Adjusted to use alumni data, can rename as needed -->

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-2">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-4 col-xs-12">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br></i>
  
  <p><strong>Current:</strong> {{ member.current_degree }}</p>

  <!-- Email and homepage links removed as in the "Current Students" section -->
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
</div>
