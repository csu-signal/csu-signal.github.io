---
layout: page
title: People
comments: false
permalink: /people/
---

<head>
<style> 
img {
}
  .left {
    float: left;
    padding: 0 10px 0 0;
  }
</style>
</head>

<div id="people">
  <h2>Faculty</h2>
  {% for person in site.data.faculty %}
  <h3 id="{{ username }}">{{ person[1].name }}</h3>
  <p align="left">
    {% if person[1].assets != null %}
      <img src="{{ site.baseurl }}{{ person[1].assets }}" width="160" height="150" class="left" />
    {% else %}
      <img src="http://www.signallab.ai/assets/images/anonymous.png" width="160" height="150" class="left" />
    {% endif %}
    {{ person[1].bio }}<br />
    {% if person[1].email != null %}<strong>Email:</strong> {{ person[1].email }}<br />{% endif %}
    {% if person[1].location != null %}<strong>Location:</strong> {{ person[1].location }}<br />{% endif %}
    {% if person[1].url_full != null %}<strong>Website:</strong> <a href="{{ person[1].url_full }}">{{ person[1].url_full }}</a>{% endif %}
  </p>
  {% endfor %}
  <hr>
  
  <h2>Ph.D. Researchers</h2>
  {% for person in site.data.phds %}
  <h3 id="{{ username }}">{{ person[1].name }}</h3>
  <p align="left">
    {% if person[1].assets != null %}
      <img src="{{ site.baseurl }}{{ person[1].assets }}" width="160" height="150" class="left" />
    {% else %}
      <img src="http://www.signallab.ai/assets/images/anonymous.png" width="160" height="150" class="left" />
    {% endif %}
    {{ person[1].bio }}<br />
    {% if person[1].email != null %}<strong>Email:</strong> {{ person[1].email }}<br />{% endif %}
    {% if person[1].location != null %}<strong>Location:</strong> {{ person[1].location }}<br />{% endif %}
    {% if person[1].url_full != null %}<strong>Website:</strong> <a href="{{ person[1].url_full }}">{{ person[1].url_full }}</a>{% endif %}
  </p>
  {% endfor %}
  <hr>
  
  <h2>Master's Researchers</h2>
  {% for person in site.data.masters %}
  <h3 id="{{ username }}">{{ person[1].name }}</h3>
  <p align="left">
    {% if person[1].assets != null %}
      <img src="{{ site.baseurl }}{{ person[1].assets }}" width="160" height="150" class="left" />
    {% else %}
      <img src="http://www.signallab.ai/assets/images/anonymous.png" width="160" height="150" class="left" />
    {% endif %}
    {{ person[1].bio }}<br />
    {% if person[1].email != null %}<strong>Email:</strong> {{ person[1].email }}<br />{% endif %}
    {% if person[1].location != null %}<strong>Location:</strong> {{ person[1].location }}<br />{% endif %}
    {% if person[1].url_full != null %}<strong>Website:</strong> <a href="{{ person[1].url_full }}">{{ person[1].url_full }}</a>{% endif %}
  </p>
  {% endfor %}
  <hr>
  
  <h2>Alumni</h2>
  <p align="left">
  {% for person in site.data.alumni %}
    <strong>{{ person[1].name }}</strong> ({{ person[1].degree }}, {{ person[1].year }}) {% if person[1].next != null %} - {{ person[1].next }}{% endif %}
  {% endfor %}
  </p>
  <hr>
  
  <h2>Honorary</h2>
  <p align="left">
  (people who I never signed a piece of paper for but who I worked with closely)
  {% for person in site.data.honorary %}
    <strong>{{ person[1].name }}</strong> ({{ person[1].degree }}, {{ person[1].year }}) - {{ person[1].next }}
  {% endfor %}
  </p>
  <hr>
</div>
