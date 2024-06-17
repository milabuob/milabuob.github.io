---
layout: splash
title: "Our Team"
classes: wide
permalink: /people/
---

<p> &nbsp;</p>
<h1>Our Team </h1>

<div class="team-photo">
  <img src="/assets/images/group-photo-2024.jpg" alt="Our Team" class="team-photo">
</div>

We value a diverse group of people who is passionate about our science and love pursuing scientific discovery through a journey of learning. 

## Meet our Team

<div class="team">
  {% for person in site.data.team %}
  <div class="team-member">
    <div class="team-member-photo">
      <img src="{{ person.photo }}" alt="{{ person.name }}">
    </div>
    <div class="team-member-info">
      <h3>{{ person.name }}</h3>
      <p><strong>{{ person.position }}</strong></p>
      <p>{{ person.bio }}</p>
      <p>
        {% if person.website %}
        <a href="{{ person.website }}" target="_blank"><i class="fas fa-globe"></i> Website</a>
        {% endif %}
        {% if person.profile %}
        <a href="{{ person.profile }}" target="_blank"><i class="fas fa-globe"></i> Profile</a>
        {% endif %}
        {% if person.linkedin %}
        <a href="{{ person.linkedin }}" target="_blank"><i class="fab fa-linkedin"></i> LinkedIn</a>
        {% endif %}
        {% if person.github %}
        <a href="{{ person.github }}" target="_blank"><i class="fab fa-github"></i> GitHub</a>
        {% endif %}
        {% if person.twitter %}
        <a href="{{ person.twitter }}" target="_blank"><i class="fab fa-twitter"></i> Twitter</a>
        {% endif %}
      </p>
    </div>
  </div>
  {% endfor %}
</div>

<style>
.team-photo {
  text-align: center;
  margin-bottom: 30px;
}

.team-photo img {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
}

.team {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.team-member {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  border: 0px solid #ddd;
  padding: 15px;
  box-shadow: 2px 2px 5px rgba(0,0,0,0.1);
}

.team-member-photo img {
  width: 150px;
  height: 150px;
  object-fit: cover;
  border-radius: 10px;
  margin-right: 20px;
}

.team-member-info {
  flex: 1;
  max-width: calc(100% - 170px); /* Ensures the text area is wider */
}

.team-member-info h3 {
  margin-top: 0;
}

.team-member-info p {
  margin: 5px 0;
}

.team-member-info a {
  margin-right: 10px;
}
</style>
