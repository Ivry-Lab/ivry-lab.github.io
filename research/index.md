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

<div id="publications-container">
  <div class="loading-message">Loading publications...</div>
</div>

<script>
async function loadPublications() {
  try {
    // Fetch the Paperpile JSON file
    const response = await fetch('{{ site.baseurl }}/data/publications.json');
    const publications = await response.json();
    
    // Group publications by year
    const publicationsByYear = {};
    
    publications.forEach(pub => {
      const year = pub.published?.year || 'Unknown';
      if (!publicationsByYear[year]) {
        publicationsByYear[year] = [];
      }
      publicationsByYear[year].push(pub);
    });
    
    // Sort years in descending order
    const sortedYears = Object.keys(publicationsByYear).sort((a, b) => {
      if (a === 'Unknown') return 1;
      if (b === 'Unknown') return -1;
      return parseInt(b) - parseInt(a);
    });
    
    // Generate HTML
    let html = '';
    
    sortedYears.forEach(year => {
      html += `<div class="year-section">
        <h3 class="year-header">${year}</h3>
        <div class="publications-list">`;
      
      // Sort publications within year by title
      const yearPubs = publicationsByYear[year].sort((a, b) => 
        (a.title || '').localeCompare(b.title || '')
      );
      
      yearPubs.forEach(pub => {
        // Format authors
        const authors = pub.author ? pub.author.map(a => a.formatted || `${a.first} ${a.last}`).join(', ') : '';
        
        // Get PDF attachment
        const pdfAttachment = pub.attachments ? pub.attachments.find(att => att.article_pdf === 1) : null;
        const pdfLink = pdfAttachment ? `{{ site.baseurl }}/files/organized_pubs_pdfs/${pdfAttachment.filename.split('/').pop()}` : null;
        
        // Build publication HTML
        html += `<div class="publication-item">
          <div class="publication-title">
            ${pdfLink ? `<a href="${pdfLink}" target="_blank" class="pdf-link">` : ''}
            ${pub.title || 'Untitled'}
            ${pdfLink ? ' <i class="fa-solid fa-file-pdf pdf-icon"></i></a>' : ''}
          </div>`;
        
        if (authors) {
          html += `<div class="publication-authors">${authors}</div>`;
        }
        
        if (pub.journal) {
          html += `<div class="publication-journal"><em>${pub.journal}</em></div>`;
        }
        
        // Add DOI link if available
        if (pub.doi) {
          html += `<div class="publication-links">
            <a href="https://doi.org/${pub.doi}" target="_blank" class="doi-link">DOI</a>
          </div>`;
        }
        
        html += '</div>';
      });
      
      html += '</div></div>';
    });
    
    // Update the container
    document.getElementById('publications-container').innerHTML = html;
    
  } catch (error) {
    console.error('Error loading publications:', error);
    document.getElementById('publications-container').innerHTML = 
      '<div class="error-message">Error loading publications. Please check that the publications.json file is available.</div>';
  }
}

// Load publications when page loads
document.addEventListener('DOMContentLoaded', loadPublications);
</script>

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

.loading-message, .error-message {
  text-align: center;
  padding: 2rem;
  color: #666;
  font-style: italic;
}

.error-message {
  color: #dc3545;
  background-color: #f8f9fa;
  border: 1px solid #dc3545;
  border-radius: 5px;
}
</style>

{% include section.html %}

### Additional Resources
Keep up to date with Professor Ivry's research and publications on the following platforms:

**[Google Scholar Profile](https://scholar.google.com/citations?user=nicnuy4AAAAJ&hl=en)**  
Complete publication list with citation metrics

**[PubMed Author Search](https://pubmed.ncbi.nlm.nih.gov/?term=Ivry+RB%5BAuthor%5D)**  
Search medical literature database