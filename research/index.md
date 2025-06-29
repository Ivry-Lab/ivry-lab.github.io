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

{% assign publications_by_year = site.data.publications | group_by: "published.year" | sort: "name" | reverse %}

{% for year_group in publications_by_year %}
  {% assign year = year_group.name %}
  {% if year == "" or year == nil %}
    {% assign year = "Unknown" %}
  {% endif %}
  
  <div class="year-section">
    <h3 class="year-header">{{ year }}</h3>
    <div class="publications-list">
      {% assign sorted_pubs = year_group.items | sort: "title" %}
      {% for pub in sorted_pubs %}
        <div class="publication-item">
          <div class="publication-title">
            {% assign pdf_attachment = pub.attachments | where: "article_pdf", 1 | first %}
            {% if pdf_attachment and pdf_attachment.source_filename %}
              <a href="{{ site.baseurl }}/files/organized_pubs_pdfs/{{ pdf_attachment.source_filename }}" target="_blank" class="pdf-link">
                {{ pub.title | default: "Untitled" }}
                <i class="fa-solid fa-file-pdf pdf-icon"></i>
              </a>
            {% else %}
              {{ pub.title | default: "Untitled" }}
            {% endif %}
          </div>
          
          {% if pub.author %}
            <div class="publication-authors">
              {% for author in pub.author %}
                {% if author.formatted %}
                  {{ author.formatted }}
                {% else %}
                  {{ author.first }} {{ author.last }}
                {% endif %}
                {% unless forloop.last %}, {% endunless %}
              {% endfor %}
            </div>
          {% endif %}
          
          {% if pub.journal %}
            <div class="publication-journal"><em>{{ pub.journal }}</em></div>
          {% endif %}
          
          {% if pub.doi %}
            <div class="publication-links">
              <a href="https://doi.org/{{ pub.doi }}" target="_blank" class="doi-link">DOI</a>
            </div>
          {% endif %}
        </div>
      {% endfor %}
    </div>
  </div>
{% endfor %}

<style>
.year-section {
  margin-bottom: 2rem;
}

.year-header {
  color: #007cba;
  border-bottom: 2px solid #007cba;
  padding-bottom: 0.5rem;
  margin-bottom: 1rem;
  font-size: 1.5rem;
}

.publications-list {
  margin-left: 1rem;
}

.publication-item {
  margin-bottom: 1.5rem;
  padding: 1rem;
  background-color: #f8f9fa;
  border-radius: 5px;
  border-left: 4px solid #007cba;
}

.publication-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  line-height: 1.3;
}

.publication-title a.pdf-link {
  color: #007cba;
  text-decoration: none;
}

.publication-title a.pdf-link:hover {
  color: #005a8b;
  text-decoration: underline;
}

.pdf-icon {
  color: #dc3545;
  margin-left: 0.3rem;
  font-size: 0.9rem;
}

.publication-authors {
  color: #666;
  margin-bottom: 0.3rem;
  font-size: 0.95rem;
}

.publication-journal {
  color: #555;
  margin-bottom: 0.5rem;
  font-size: 0.9rem;
}

.publication-links {
  margin-top: 0.5rem;
}

.doi-link {
  background-color: #007cba;
  color: white;
  padding: 0.2rem 0.5rem;
  border-radius: 3px;
  text-decoration: none;
  font-size: 0.8rem;
  font-weight: 500;
}

.doi-link:hover {
  background-color: #005a8b;
  color: white;
}
</style>

{% include section.html %}

### Additional Resources
Keep up to date with Professor Ivry's research and publications on the following platforms:

**[Google Scholar Profile](https://scholar.google.com/citations?user=nicnuy4AAAAJ&hl=en)**  
Complete publication list with citation metrics

**[PubMed Author Search](https://pubmed.ncbi.nlm.nih.gov/?term=Ivry+RB%5BAuthor%5D)**  
Search medical literature database