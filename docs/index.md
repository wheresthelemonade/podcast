---
layout: default
title: English
nav_order: 2
has_children: true
lang: en
---

# Where's The Lemonade

<style>
.collection {
  display: flex;
  justify-content: space-between;
  margin: 20px;
}

.collection-item {
  width: 30%;
  padding: 10px;
  border: 1px solid #ccc;
  margin: 10px;
  text-align: center;
}

.collection-item a {
  text-decoration: none;
  color: #333;
}

.collection-item img {
  width: 100%;
  height: auto;
}
</style>

![mainimage](./DarrenPaige.jpg)

They say when life gives you lemons you should make lemonade. Making lemonade is not always easy or possible. For us, we found ourselves single in our 40's with kids at home and starting life over again. Luckily we found each other, online no doubt. When we began blending families, schedules, traditions, and laundry, we discovered lots of lemons. Our podcast is a reflection on how we get through the hard times and enjoy the good times on our new journey together, all with ten kids in tow. Sometimes when life gives you lemons, you make lemon squares. Lemonade might come later.

<div>
<div class="collection">
  <div class="collection-item">
    <a href="https://www.embracingdigital.org/travel.html">
      <img src="./travel.jpg" width="128" height="128" alt="Travel">
    </a>
    Travel
  </div>
  <div class="collection-item">
    <a href="https://www.embracingdigital.org/blending.html">
      <img src="./blending.jpg" width="128" height="128" alt="Blending Families">
    </a>
    Blending Families
  </div>
  <div class="collection-item">
    <a href="https://www.embracingdigital.org/relationships.html">
      <img src="./relationships.jpg" width="175" height="128" alt="Relationships">
    </a>
    Relationships
  </div>
  <div class="collection-item">
    <a href="https://www.embracingdigital.org/collections/news.html">
      <img src="./news.jpg" width="175" height="128" alt="Curren Events">
    </a>
    Current Events
  </div>
</div>
</div>

<style>
.topcolumn {
float: left;
padding: 10px;
}

.topleft {
width: 65%;
}

.topright {
width: 35%;
}

/* Clear floats after the columns */
.toprow:after {
content: "";
display: table;
clear: both;
}
</style>
{% assign sortedEpisodes = site.pages | sort: 'nav_order' | reverse | where: 'layout', 'posts' | where: 'lang', 'en' |
limit: 10 %}

<h1>Episodes</h1>
{% for page in sortedEpisodes %}
{% if page.number %}
<div style="display:flex;">
<p class="episode">
    <img class="thumbnail" src="../{{ page.path | remove: page.name }}/{{ page.img }}" width="128" height="128">
    <a href="{{ page.url }}">{{ page.number}} - {{ page.title }}</a><br>
    {{ page.summary }}
</p>
</div>
{% endif %}
{% endfor %}

<style>
.thumbnail {
    float: left;
    margin: 0 15px 0 0;
}
.episode {
    margin: 10px 0;
}
.episode:hover {
    background-color: #cceeff;
}
</style>
