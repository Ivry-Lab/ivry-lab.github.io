---
title: News
nav:
  order: 4
  tooltip: Lab updates and announcements
---

# {% include icon.html icon="fa-solid fa-newspaper" %}News

Lab updates, announcements, and newsletters from the Cognition and Action Lab.

{% include section.html %}

## Featured

{%- assign featured_news = site.data.news | where: "group", "featured" -%}
<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 2rem;">
  <div>
    {% include list.html data="news" component="card" filter="group == 'featured'" %}
  </div>
  <div>
    <iframe width="100%" height="315" src="https://www.youtube.com/embed/SkA7tu0KaTk" frameborder="0" allowfullscreen></iframe>
  </div>
</div>

{% include section.html %}

## Newsletters

<div style="display: flex; gap: 1rem; flex-wrap: wrap;">
{% include list.html data="news" component="card" filter="group == 'newsletter'" %}
</div>

{% include section.html %}