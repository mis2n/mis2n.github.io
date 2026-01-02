---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---

## About

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
  {% if member.cv %} <a href="{{ site.url }}{{ site.baseurl }}/{{ member.cv }}" target="_blank"><i class="ai ai-cv-square ai-3x"></i></a> {% endif %}
  {% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-3x"></i></a> {% endif %}
  {% if member.github %} <a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-3x"></i></a> {% endif %}
  {% if member.researchgate %} <a href="{{ member.researchgate }}" target="_blank"><i class="ai ai-researchgate-square ai-3x"></i></a> {% endif %}

  <ul style="overflow: hidden">
    {% for education in member.education %}
      <li>{{ education | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>

</div>
</div>
</div>
{% endfor %}

{% if site.data.skills %}

<div class="jumbotron">
  <h3>Skills</h3>
  <ul>
    {% for grant in site.data.skills %}
      <li>{{ grant.name }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

{% if site.data.certifications %}

<div class="jumbotron">
  <h3>Certifications</h3>
  <ul>
    <li><b>Neo4j Graph Database</b> - Certified Professional</li>
    <!-- {% for certifications in site.data.ccertifications %}
      <li>{{ certifications.name | replace: "-","&#8211;" }}</li>
    {% endfor %} -->
  </ul>
</div>
{% endif %}

{% if site.data.certifications %}

<div class="jumbotron">
  <h3>Academic & Community Service</h3>
  <ul>
    <li><b>Engagement Officer</b> - Postdoctoral Society of Argonne, 2026</li>
    <li><b>Committee Member</b> - Postdoctoral Research and Career Symposium, Postdoctoral Society of Argonne, 2025</li>
    <li><b>Committee Member</b> - National Postdoc Awareness Week, Postdoctoral Society of Argonne, 2025</li>
    <li><b>Member at Large (Strategic Security Sciences)</b> - Postdoctoral Society of Argonne, 2025</li>
    <li><b>Program Committee</b> - Machine Learning for Ancient Langauges (ML4AL) Workshop at The 62nd Annual Meeting of the Association for Computational Linguistics, 2024</li>
    <li><b>Reviewer</b> - ACM SIGMIS Computers and People Research Conference, 2024 </li>
    <!-- {% for certifications in site.data.ccertifications %}
      <li>{{ certifications.name | replace: "-","&#8211;" }}</li>
    {% endfor %} -->
  </ul>
</div>
{% endif %}

{% if site.data.awards %}

<div class="jumbotron">
  <h3>Internships & Honors</h3>
  <ul>
    {% for award in site.data.awards %}
      <li>{{ award.name | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

<!-- {% if site.data.people %} -->

<!-- <div class="jumbotron">
  <h3>Students and Mentoring</h3>
  <ul>
    {% for student in site.data.people %}
      <li>{{ student.name }}, {{ student.location }} ({{ student.degree }}, {{ student.year }})</li>
    {% endfor %}
  </ul>
</div> -->
<!-- {% endif %} -->

<!-- <div class="jumbotron">
  <h4>Sponsors</h4>
  <div style='display:block; text-align:center; margin-left:auto; margin-right:auto;'>
  {% for funder in site.data.funders %}<a href="{{ funder.url }}" target="_blank"><img src='{{ site.url }}{{ site.baseurl }}/images/{{ funder.image }}' style='max-height: 80px; max-width: 200px; margin: 1%'/></a>{% endfor %}
  </div>
</div> -->
