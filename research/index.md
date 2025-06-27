---
title: Research
nav:
  order: 1
  tooltip: Published works
---

# {% include icon.html icon="fa-solid fa-microscope" %}Research

## Recent Publications (2017-Present)
*Automatically updated from ORCID*

{% include search-box.html %}

{% include search-info.html %}

{% include list.html data="citations" component="citation" style="rich" filter="author =~ /Ivry/" %}

---

## Earlier Publications (Pre-2017)

{% assign pdf_files = site.static_files | where: "extname", ".pdf" | where_exp: "file", "file.path contains '/files/publications/'" %}

{% for file in pdf_files %}
  {% assign filename = file.name | remove: ".pdf" %}
  {% assign clean_name = filename | replace: "_", " " | replace: "-", " " | split: "." | first | capitalize %}
  
  **{{ clean_name }}**  
  [PDF]({{ file.path }})  
  
{% endfor %}

---