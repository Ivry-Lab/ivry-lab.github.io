---
title: Research
nav:
  order: 1
  tooltip: Published works
---

# {% include icon.html icon="fa-solid fa-microscope" %}Research

## Publications

{% include search-box.html %}

{% include search-info.html %}

<!-- First, let's see ALL publications to debug -->
{% include list.html data="citations" component="citation" style="rich" %}

<!-- Commented out the filter temporarily to see if publications show up at all
{% include list.html data="citations" component="citation" style="rich" filter="author =~ /Ivry/" %}
-->

{% assign older_pdfs = site.static_files | where: "extname", ".pdf" | where_exp: "file", "file.path contains '/files/pre2017_publications/'" %}

{% if older_pdfs.size > 0 %}
  {% assign sorted_pdfs = older_pdfs | sort: "name" %}
  
  {% for file in sorted_pdfs %}
    {% assign filename = file.name | remove: ".pdf" %}
    {% assign clean_name = filename | replace: "_", " " | replace: "-", " " | replace: "ivry", "Ivry" %}
    
    **{{ clean_name }}**  
    [PDF]({{ file.path }})  
    
  {% endfor %}
  
  <p><em>{{ older_pdfs.size }} earlier publications available</em></p>
{% else %}
  <p><em>Loading older publications...</em></p>
{% endif %}
