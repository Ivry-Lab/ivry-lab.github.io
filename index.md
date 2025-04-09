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

![CognAc Lab Logo](images/cognac_website_photo.png)

Experiments incorporate a combination of behavioral, perceptual and cognitive tasks with both healthy participants and patient populations. Neuroimaging techniques such as functional magnetic resonance imaging (fMRI), and non-invasive brain stimulation such as transcranial magnetic stimulation (TMS) are also used. Several researchers are invovled in collaborative work with neuroscientsists and/or physicians located at other research and hospital facilities located in the United States and around the world.

---

## Highlights

<!-- Replace the entire feature include with this custom HTML -->
<div class="feature">
  <a href="https://www.youtube.com/watch?v=NYpHXUbTKmI&t=153s" class="feature-image">
    <!-- YouTube thumbnail with play button overlay -->
    <div style="position: relative; width: 100%;">
      <img 
        src="https://img.youtube.com/vi/NYpHXUbTKmI/maxresdefault.jpg" 
        loading="lazy" 
        alt="Cognition and Action Lab Research Video" 
        style="width: 100%; height: auto;"
      >
      <div style="position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%);">
        <svg height="68px" width="68px" viewBox="0 0 68 48">
          <path d="M66.52,7.74c-0.78-2.93-2.49-5.41-5.42-6.19C55.79,.13,34,0,34,0S12.21,.13,6.9,1.55 C3.97,2.33,2.27,4.81,1.48,7.74C0.06,13.05,0,24,0,24s0.06,10.95,1.48,16.26c0.78,2.93,2.49,5.41,5.42,6.19 C12.21,47.87,34,48,34,48s21.79-0.13,27.1-1.55c2.93-0.78,4.64-3.26,5.42-6.19C67.94,34.95,68,24,68,24S67.94,13.05,66.52,7.74z" fill="#f00"></path>
          <path d="M45,24 L27,14 L27,34 L45,24 Z" fill="#fff"></path>
        </svg>
      </div>
    </div>
  </a>
  <div class="feature-text">
    <p class="feature-title">Our Research</p>
    <p>Our research focuses on the cognitive neuroscience of action, skilled movement, and cognition. We conduct experiments involving neurologically healthy and impaired individuals, using a range of methods to develop psychological models of how people produce and learn movements. Watch this video to learn more! </p>
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
