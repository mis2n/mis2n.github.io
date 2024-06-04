---
title: "Publications"
layout: gridlay
sitemap: false
permalink: /publications/
years: [2021, 2022, 2023, 2024]
---

<style>
.jumbotron{
    padding:3%;
    padding-bottom:10px;
    padding-top:10px;
    margin-top:10px;
    margin-bottom:30px;
}
</style>


<div class="jumbotron">
### Refereed conference proceedings
{% bibliography --query @inproceedings %}
</div>

<div class="jumbotron">
### Refereed journal articles
{% bibliography --query @article %}
</div>
