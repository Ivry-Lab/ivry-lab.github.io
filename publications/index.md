---
title: Publications
nav:
  order: 2
  tooltip: Research publications
---


## Publications

{% assign publications_by_year = site.data.publications | group_by: "published.year" | sort: "name" | reverse %}

{% for year_group in publications_by_year %}
  {% assign year = year_group.name %}
  {% if year == "" or year == nil %}
    {% assign year = "Unknown" %}
  {% endif %}
  
  **{{ year }}**
  
  {% assign sorted_pubs = year_group.items | sort: "title" %}
  {% for pub in sorted_pubs %}
    {% assign pdf_attachment = pub.attachments | where: "article_pdf", 1 | first %}
    {% if pdf_attachment and pdf_attachment.source_filename %}
      [{{ pub.title | default: "Untitled" }}]({{ site.baseurl }}/files/organized_pubs_pdfs/{{ pdf_attachment.source_filename }})
    {% else %}
      {{ pub.title | default: "Untitled" }}
    {% endif %}
    {% if pub.author %}
      - {% for author in pub.author %}{% if author.formatted %}{{ author.formatted }}{% else %}{{ author.first }} {{ author.last }}{% endif %}{% unless forloop.last %}, {% endunless %}{% endfor %}
    {% endif %}
    {% if pub.journal %} - *{{ pub.journal }}*{% endif %}
    {% if pub.doi %} - [DOI](https://doi.org/{{ pub.doi }}){% endif %}

  {% endfor %}

{% endfor %}

{% include section.html %}

### Additional Resources
Keep up to date with Professor Ivry's research and publications on the following platforms:

**[Google Scholar Profile](https://scholar.google.com/citations?user=nicnuy4AAAAJ&hl=en)**  
Complete publication list with citation metrics

**[PubMed Author Search](https://pubmed.ncbi.nlm.nih.gov/?term=Ivry+RB%5BAuthor%5D)**  
Search medical literature database