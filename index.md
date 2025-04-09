---
---
## Welcome to the Cognition and Action Lab at the University of California, Berkeley.

Under the direction of Professor Richard Ivry, The
Cognition and Action Lab currently supports
several graduate, undergraduate, and post-doctoral
students. Research projects cover diverse areas of
behavior and cognition, including visual,
auditory, and time perception; language and
speech; and motor coordination.

<div style="float: right; margin: 0 0 10px 20px;">
  <img src="images/cognac_website_photo.png" alt="CognAc Lab Logo" width="300">
</div>

Experiments incorporate a combination of behavioral, perceptual and cognitive tasks with both healthy participants and patient populations. Neuroimaging techniques such as functional magnetic resonance imaging (fMRI), and non-invasive brain stimulation such as transcranial magnetic stimulation (TMS) are also used. Several researchers are invovled in collaborative work with neuroscientsists and/or physicians located at other research and hospital facilities located in the United States and around the world.

---

## Highlights

<!-- Replace the entire feature include with this custom HTML -->
<div class="feature">
  <div class="feature-image">
    <!-- Plain YouTube iframe - Jekyll will handle the thumbnail conversion -->
    <iframe width="100%" height="315" src="https://www.youtube.com/embed/NYpHXUbTKmI?start=153" frameborder="0" allowfullscreen></iframe>
  </div>
  <div class="feature-text">
    <p class="feature-title">Our Research</p>
    <p>Our research focuses on the cognitive neuroscience of action, skilled movement, and cognition. We conduct experiments involving neurologically healthy and impaired individuals, using a range of methods to develop psychological models of how people produce and learn movements. Watch this video to learn more!</p>
    <a href="https://www.youtube.com/watch?v=NYpHXUbTKmI&t=153s" class="button">Watch the video</a>
  </div>
</div>

{% capture text %}
Research projects in the lab involve: motor learning and control, action selection and execution, language and speech, and more. 

{%
  include button.html
  link="projects"
  text="Browse our projects"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/photo.jpg"
  link="projects"
  title="Our Projects"
  flip=true
  style="bare"
  text=text
%}

{% capture text %}

Meet the current members of the CognAc Lab.

{%
  include button.html
  link="team"
  text="Meet our team"
  icon="fa-solid fa-arrow-right"
  flip=true
  style="bare"
%}

{% endcapture %}

{%
  include feature.html
  image="images/lab_photo.jpg"
  link="team"
  title="Our Team"
  text=text
%}

---

If you have any questions, please send us an email to [ivrylab@berkeley.edu](mailto:ivrylab@berkeley.edu).

{% include section.html %}

#### Image Credit
Cerebellum neuroart thumbnail image by [Greg Dunn](https://www.gregadunn.com/self-reflected/self-reflected-gallery/).


{% include section.html %}
