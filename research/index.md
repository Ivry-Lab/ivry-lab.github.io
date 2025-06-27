---
title: Research
nav:
  order: 1
  tooltip: Research projects and publications
---

# {% include icon.html icon="fa-solid fa-microscope" %} Research

Our research focuses on the cognitive neuroscience of action, skilled movement, and cognition. Experiments involve healthy participants and patient populations, using a combination of behavioral and neuroimaging methods to develop models of human behavior and cognition.

{% include section.html %}
## Publications

### Recent Publications (2017 - Present)
{% include search-box.html %}
{% include search-info.html %}

{% include list.html data="citations" component="citation" style="rich" %}

## Earlier Publications (Pre-2017)

{% assign older_pdfs = site.static_files | where: "extname", ".pdf" | where_exp: "file", "file.path contains '/files/pre2017_publications/'" %}

**[Browse {{ older_pdfs.size }} Earlier Publications (PDF Archive)]({{ site.baseurl }}/files/pre2017_publications/)**

*Click the link above to access the complete archive of Ivry Lab publications from before 2017. You can browse and download individual PDFs from the archive.*

