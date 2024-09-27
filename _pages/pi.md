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
  <p>I am an investigator, assistant professor (started Sep 2024; <a href="https://researchers.mgh.harvard.edu/profile/14495114/Zhi-Yu" target="_blank">faculty page</a>) at the <a href="https://www.mghcteu.org/" target="_blank">Clinical and Translational Epidemiology Unit (CTEU)</a>, Department of Medicine, <a href="https://www.massgeneral.org/" target="_blank">Massachusetts General Hospital</a>, a faculty member at <a href="https://hms.harvard.edu/" target="_blank">Harvard Medical School</a>, and an affiliate faculty at <a href="https://www.broadinstitute.org/" target="_blank">Broad Institute of MIT and Harvard</a>.</p>
  <p>I was a K99 postdoctoral fellow under the mentorship of Drs. <a href="https://natarajanlab.mgh.harvard.edu/pradeep-natarajan/" target="_blank">Pradeep Natarajan</a> and Anthony Philippakis at the Broad Institute. I completed my PhD in Epidemiology and a concurrent Master’s in Biostatistics from 2017 to 2020 at <a href="https://publichealth.jhu.edu/" target="_blank">Johns Hopkins Bloomberg School of Public Health</a>, where I was mentored by Drs. <a href="https://med.nyu.edu/faculty/josef-coresh" target="_blank">Josef Coresh</a> and <a href="http://www.nilanjanchatterjee.com/" target="_blank">Nilanjan Chatterjee</a>.  Prior to these, I received my Master’s in Epidemiology from <a href="https://www.hsph.harvard.edu/" target="_blank">Harvard T.H. Chan School of Public Health</a> and a Bachelor of Medicine in Chinese Medicine from Hong Kong Baptist University.</p>
  <p>My research focuses on computational modeling of human multi-omics data to investigate the mechanisms of cardiovascular and age-related diseases, aiming to discover potential therapies. In particular, I developed strong expertise in (1) age-related clonal hematopoiesis (acuqired somatic mutations in the blood-forming system) and its interplay with germline omics and drugs and (2) large-scale plasma proteomics. </p>
  <p>Outside research, things I’m proud of as a medical researcher are: I somehow haven’t caught COVID, I still have naturally 20/15 vision, and my LDL is naturally 50 something. Let’s see which one I’ll quietly remove first 😎</p>
  
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
