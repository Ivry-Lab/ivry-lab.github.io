---
title: Team
nav:
  order: 3
  tooltip: About our team
---

<div style="text-align: center; font-size: 1.5rem; margin-bottom: 16px;">
  Meet the members of the CognAc lab!
</div>

{% include section.html %}

{% include list.html data="members" component="portrait" filter="role == 'pi'" %}
{% include list.html data="members" component="portrait" filter="role != 'pi'" %}

{% include section.html background="images/background.jpg" dark=true %}
{% include section.html %}

<div style="text-align: center; font-size: 1.5rem; margin-bottom: 16px;">
Our lab at recent events including the 2025 National Ataxia Foundation Conference, lab dinner at Prof Ivry's house, and a lab retreat in Lake Tahoe last year!
</div>

{% include section.html %}

{% include section.html %}

{% capture content %}

{% include figure.html image="images/NAF.JPG" %}
{% include figure.html image="images/lab_party.jpg" %}
{% include figure.html image="images/tahoe_lab_trip.jpg" %}

{% endcapture %}

{% include grid.html style="square" content=content %}
