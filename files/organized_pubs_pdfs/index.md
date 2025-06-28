---
title: Publications Archive
layout: default
permalink: /files/organized_pubs_pdfs/
---

# Publications Archive

{% assign older_pdfs = site.static_files | where: "extname", ".pdf" | where_exp: "file", "file.path contains '/files/organized_pubs_pdfs/'" %}

{% if older_pdfs.size > 0 %}
{% assign sorted_pdfs = older_pdfs | sort: "name" %}

**{{ older_pdfs.size }} publications available for download:**

<ul>
{% for file in sorted_pdfs %}
{% assign filename = file.name | remove: ".pdf" %}
{% assign clean_name = filename | replace: "_", " " | replace: "-", " " %}
<li><a href="{{ site.baseurl }}{{ file.path }}">{{ clean_name }}</a></li>
{% endfor %}
</ul>

{% else %}
No publications found.
{% endif %}

---

[← Back to Research]({{ site.baseurl }}/research/)