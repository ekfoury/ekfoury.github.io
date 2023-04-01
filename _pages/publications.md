---
layout: page
permalink: /publications/
title: Publications
description: List of publications over the years
years: [2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

Google Scholar statistics (<a href="https://scholar.google.com/citations?user={{ site.data.scholar.id }}">Link</a>): <br>
<ul>
<li> Citations: {{ site.data.scholar.citations }} </li>
<li> h-index: {{ site.data.scholar.h_index }} </li>
<li> i10-index: {{ site.data.scholar.i10_index }} </li>
</ul>

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
  
{% endfor %}

</div>
