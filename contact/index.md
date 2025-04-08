---
title: Contact
nav:
  order: 6
  tooltip: Email, address, and location
---

# {% include icon.html icon="fa-regular fa-envelope" %}Contact

Contact us below:

{%
  include button.html
  type="email"
  text="ivry@berkeley.edu"
  link="ivry@berkeley.edu"
%}
{%
  include button.html
  type="phone"
  text="(510) 642-7146"
  link="+1-510-642-7146"
%}
{%
  include button.html
  type="2121 Berkeley Way West, Berkeley, CA"
  text="Our location on Google Maps for easy navigation"
  link="https://www.google.com/maps"
%}

{% include section.html %}

{% capture col1 %}

{%
  include figure.html
  image="images/photo.jpg"
  caption=""
%}

{% endcapture %}

{% capture col2 %}

{%
  include figure.html
  image="images/photo.jpg"
  caption=""
%}

{% endcapture %}

{% include cols.html col1=col1 col2=col2 %}

{% include section.html dark=true %}

