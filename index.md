---
layout: single    # change to page to get rid of the blog
title: "The Medical Imaging Lab"
classes: wide
excerpt: "Revolutionizing Neuroscience and Medicine through Innovative Optical Imaging"
header:
  overlay_color: "#333"
  #overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  #overlay_image: /assets/images/unsplash-image-1.jpg
  #actions:
  #  - label: "Learn more"
  #  - url: "/about/"
  #caption: "Photo credit: "
  feature_row:
  - image_path: /assets/images/group-photo-2024.jpg
    alt: "Group Photo"
    title: "Group Photo 2024"
    excerpt: "Let's see what happens here"
    btn_label: "Read More"
    btn_class: "btn--primary"
---


We are a research lab focused on developing optical imaging technologies and methods that can be applied in Neuroscience and Medicine.

## Latest News

{% assign news_posts = site.posts | where: "categories", "news" | sort: "date" | reverse %}
<ul>
  {% for post in news_posts limit: 5 %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a> <br>
      <small>{{ post.date | date: "%B %-d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>


## Latest Publications from our Lab
- Kazazian, K., Abdalmalak, A., Novi, S. L., Norton, L., Moulavi-Ardakani, R., Kolisnyk, M., Gofton, T. E., Mesquita, R. C., Owen, A. M. & Debicki, D. B. (2024). *Functional near-infrared spectroscopy: A novel tool for detecting consciousness after acute severe brain injury.* PNAS, 121(36), e2402723121. [Link](https://doi.org/10.1073/pnas.2402723121){:target="_blank"}
  
- Cao, J., Gorecki, J., Dale, R., Redwood-Sawyerr, C., Kontoravdi, C., Polizzi, K., Rowlands, C.J. & Dehghani, H. (2024) *Fluorescence diffuse optical monitoring of bioreactors: a hybrid deep learning and model-based approach for tomography.* Biomed. Opt. Express, 15(9), 5009-5024 [Link](https://doi.org/10.1364/BOE.529884){:target="_blank"}

- Qin, Y., Wu, J., Bulger, E., Cao, J., Dehghani, H., Shinn-Cunningham, B. & Kainerstorfer, J.M. (2024) *Optimizing spatial accuracy in electroencephalography reconstruction through diffuse optical tomography priors in the auditory cortex.* Biomed. Opt. Express, 15(8), 4859-4876 [Link](https://doi.org/10.1364/BOE.531576){:target="_blank"}

[See More](/publications/)


## Opportunities
- **PhD studentship.**  Causal Models for Brain Connectivity Analysis in fNIRS. [Description](https://www.findaphd.com/phds/project/causal-models-for-brain-connectivity-analysis-in-fnirs/?p174706){:target="_blank"}

- **PhD studentship.** Building a Portable Blood Flow Monitor with Near-Infrared Light for ICU Patients. [Description](https://www.findaphd.com/phds/project/building-a-portable-blood-flow-monitor-with-near-infrared-light-for-icu-patients/?p168155){:target="_blank"}

- **PhD studentship.** Disentangling functional subnetworks in the resting state with fNIRS. [Description](https://www.findaphd.com/phds/project/disentangling-functional-subnetworks-in-the-resting-state-with-fnirs/?p168974){:target="_blank"}


## Where are we?
The Medical Imaging lab is part of the School of Computer Science at the University of Birmingham, located in Birmingham, the UK’s second-largest city. Known for its rich cultural heritage, green spaces, and important role in the Industrial Revolution, Birmingham offers a thriving environment for innovation. The city boasts over 8,000 acres of parks, making it one of the greenest cities in the UK. The University of Birmingham, established in 1900, is a leading global institution renowned and has a long history of pioneering research that addresses the complex challenges of the modern world. The School of Computer Science of the University is one of the oldest computer science departments in the UK and has a proud tradition of advancing the frontiers of knowledge in the field, with renowned research in areas such as artificial intelligence, cybersecurity, data science, and robotics.

<!--
<div id="map"></div>

<style>
#map {
  height: 400px;
  width: 100%;
  margin-top: 20px;
}

h4 {
  color: #2c3e50; /* Dark blue */
}

</style>

<script>
  function initMap() {
    var schoolLocation = {lat: 52.4508, lng: -1.9305};
    var map = new google.maps.Map(document.getElementById('map'), {
      zoom: 15,
      center: schoolLocation
    });
    var marker = new google.maps.Marker({
      position: schoolLocation,
      map: map
    });
  }
</script>
<script async defer
src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap">
</script>
-->