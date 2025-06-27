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

## Earlier Publications (Pre-2017)

{% assign older_pdfs = site.static_files | where: "extname", ".pdf" | where_exp: "file", "file.path contains '/files/pre2017_publications/'" %}

**[Browse {{ older_pdfs.size }} Earlier Publications (PDF Archive)]({{ site.baseurl }}/files/pre2017_publications/)**

*Click the link above to access the complete archive of Ivry Lab publications from before 2017. You can browse and download individual PDFs from the archive.*

