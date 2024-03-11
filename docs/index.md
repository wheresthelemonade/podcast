---
layout: default
title: Home
nav_order: 1
lang: en
---

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
<div>
<div class="collection" style="border: 0px;">
  <div class="collection-item" style="border: 0px; width:75%; text-align: left;">
<h1>Where's The Lemonade</h1>
<h3> Finding lemonade when life gives you lemons.</h3>
  </div>
  <div class="collection-item" style="border: 0px;">
    <img src='./logo.jpg' width="">
  </div>
</div>

<div 
    style="background-image: url('./DarrenPaige.jpg');
    width:100%; 
    height:150px; 
    background-position:center;">&nbsp;</div>

They say when life gives you lemons you should make lemonade. Making lemonade is not always easy or possible. For us, we found ourselves single in our 40's with kids at home and starting life over again. Luckily we found each other, online no doubt. When we began blending families, schedules, traditions, and laundry, we discovered lots of lemons. Our podcast is a reflection on how we get through the hard times and enjoy the good times on our new journey together, all with ten kids in tow. Sometimes when life gives you lemons, you make lemon squares. Lemonade might come later.

<div>
<div class="collection">
  <div class="collection-item">
    <a href="./travel.html">
      <img src="./travel.jpg" width="128" height="128" alt="Travel">
    </a>
    Travel
  </div>
  <div class="collection-item">
    <a href="./blended.html">
      <img src="./blending.jpg" width="128" height="128" alt="Blending Families">
    </a>
    Blending Families
  </div>
  <div class="collection-item">
    <a href="./relationships.html">
      <img src="./relationships.jpg" width="175" height="128" alt="Relationships">
    </a>
    Relationships
  </div>
  <div class="collection-item">
    <a href="./news.html">
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
{% include subscribe.html %}
{% assign sortedEpisodes = site.pages | sort: 'nav_order' | reverse | where: 'layout', 'posts' | where: 'lang', 'en' |
limit: 10 %}

<h1>Episodes</h1>
{% for page in sortedEpisodes %}
{% if page.number %}
<div style="display:flex;">
<p class="episode">
    <img class="thumbnail" src="../{{ page.path | remove: page.name }}/{{ page.img }}" width="128" height="128">
    <a href="{{ page.url }}">{{ page.title }}</a><br>
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
