---
layout: page
title: keywords
permalink: /keywords
---

<section class="c-archives">
  <link rel="shortcut icon" href="">

{% for tag in site.tags %}


  <h2 class="c-archives__year" id="{{ tag[0] }}-ref">
    {{ tag[0] }}
  </h2>
  <ul class="c-archives__list">

  {% for post in site.posts %}
  {% if post.tags contains tag[0] %}
  <li class="c-archives__item" >
    <a href="{{ post.url | prepend: site.baseurl }}" style="width: 100%;">
      <div style="display: flex; justify-content: space-evenly; align-items: center; flex-wrap: wrap;">
      <div>
		  <h3> {{ post.categories }} </h3>
	  </div>
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
  {% endif %}
  {% endfor %}

  </ul>

{% endfor %}

</section>

