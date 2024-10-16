---
title: "pi"
layout: gridlay
sitemap: false
permalink: /pi/  # Change from /about/ to /pi/
---

## PI

{% for member in site.data.pi %}

<div class="jumbotron">
<div class="row">
<div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-8 col-xs-12">
  <h3>{{ member.name }}</h3>
  <h4><i>{{ member.info }}</i></h4>
  {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-3x"></i></a> {% endif %}
  {% if member.linkedin %} <a href="{{ member.linkedin }}" target="_blank"><i class="fa fa-linkedin-square fa-3x"></i></a> {% endif %}
  {% if member.x %} <a href="{{ member.x }}" target="_blank"><i class="fa fa-twitter-square fa-3x"></i></a> {% endif %}
  {% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-3x"></i></a> {% endif %}

  <ul style="overflow: hidden">
    {% for education in member.education %}
      <li>{{ education | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>

</div>
</div>
</div>
{% endfor %}

<div class="jumbotron">
  <h3>Bio</h3>
  <p>I am an investigator, asst prof (started Sep 2024; <a href="https://researchers.mgh.harvard.edu/profile/14495114/Zhi-Yu" target="_blank">page</a>) at <a href="https://www.massgeneral.org/" target="_blank">Massachusetts General Hospital</a> and an affiliate faculty at <a href="https://www.broadinstitute.org/" target="_blank">Broad Institute</a>.</p>
  <p>I was a K99 postdoc at the Broad Institute (mentors: Drs. <a href="https://natarajanlab.mgh.harvard.edu/pradeep-natarajan/" target="_blank">Pradeep Natarajan</a> and Anthony Philippakis). I completed my PhD in Epidemiology and a concurrent Master’s in Biostatistics from 2017 to 2020 at Johns Hopkins Bloomberg School of Public Health (mentors: Drs. <a href="https://med.nyu.edu/faculty/josef-coresh" target="_blank">Josef Coresh</a> and <a href="http://www.nilanjanchatterjee.com/" target="_blank">Nilanjan Chatterjee</a>).  Before these, I received my Master’s from Harvard (mentor: Dr. <a href="https://www.hsph.harvard.edu/profile/edward-giovannucci/" target="_blank">Edward Giovannucci</a>) and a Bachelor of Medicine from Hong Kong Baptist University.</p>
  <p>My research focuses on computational modeling of human multi-omics data to study the mechanisms of cardiovascular and other age-related diseases. I developed strong expertise in (1) clonal hematopoiesis and (2) large-scale proteomics. </p>
  <p>Outside research, things I’m proud of as a medical researcher are: I haven’t caught COVID, I still have natural 20/15 vision, and 50 something LDL-C. Let’s see which one I’ll quietly remove first 😎</p>
  
</div>

{% if site.data.grants %}

<div class="jumbotron">
  <h3>Grants</h3>
  <ul>
    {% for grant in site.data.grants %}
      <li>{{ grant.name }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

{% if site.data.awards %}

<div class="jumbotron">
  <h3>Awards</h3>
  <ul>
    {% for award in site.data.awards %}
      <li>{{ award.name | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

<div class="jumbotron">
  <h4>Thanks</h4>
  <div style='display:block; text-align:center; margin-left:auto; margin-right:auto;'>
  {% for funder in site.data.funders %}<a href="{{ funder.url }}" target="_blank"><img src='{{ site.url }}{{ site.baseurl }}/images/{{ funder.image }}' style='max-height: 80px; max-width: 200px; margin: 1%'/></a>{% endfor %}
  </div>
</div>
