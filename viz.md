---
layout: page
title: viz
permalink: /viz
---
<section class="c-archives">
  <link rel="shortcut icon" href="">
  <ul class="c-archives__list">
  {% for post in site.categories.viz  %}
    <li class="c-archives__item" >
    <a href="{{ post.url | prepend: site.baseurl }}" style="width: 100%;">
      <div style="display: flex; justify-content: space-evenly; align-items: center; flex-wrap: wrap;">
      <div style="flex-grow: 1; max-width: 25%; min-width: 125px; margin: 1em;">
      <img src="{{ site.url }}{{ site.baseurl }}/assets/{{ post.artist }}/{{ post.sample }}" alt="{{ post.author }}" style="height: 10em; display: block; margin-left: auto; margin-right: auto;">
      </div>
      <div style="flex-grow: 1; max-width: 25%; min-width: 125px; margin: 1em;">
      <img src="{{ site.url }}{{ site.baseurl }}/assets/{{ post.artist }}/artist.jpg" alt="{{ post.author }}" style="height: 10em; display: block; margin-left: auto; margin-right: auto">
      </div>
      <div style="flex-grow: 2; max-width: 50%; min-width: 250px; margin: 1em; padding: 0em 3em;">
      <h3>
       {{ post.title }}
        <br>
        <code>{{ site.data.artists[post.artist].name }}</code>
        <br>
        <small>{{post.description}}</small>
      </h3>
      </div>
    </div>
    </a>
    </li>
  {% endfor %}
  </ul>
</section>
