---
layout: post
codemirror: true
microblog: true
title: Night at the Museum Learning Blog
permalink: /n@tm/
author: Seonyoo Pak
---

## Night at the Museum

At N@TM, there were many different projects from all of the CS classes, showcasing the work that they had done throughout the trimester. We had a table set up with our RPG game, and we also had a TV in the back where we presented our game to everyone who came by. It was a great opportunity to share our work and get feedback from others.

## Presenting our Game

At N@TM, we had the chance to present our Murder Mystery game to a wide audience. We set up a TV in the back of our table where we showcased our game, allowing visitors to see the gameplay and learn about the features we implemented. It was exciting to share our project with others and receive feedback on our work.

## Gallery of Images from N@TM

<style>
.natm-gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(180px,1fr));
  gap: 10px;
  margin: 1rem 0;
}
.natm-item{ position:relative; overflow:hidden; border-radius:8px; display:block; text-decoration:none; color:inherit;}
.natm-item img{ width:100%; height:100%; object-fit:cover; transition:transform .35s ease, filter .35s ease; display:block;}
.natm-item:hover img{ transform:scale(1.08); filter:brightness(.9) saturate(1.05);}
.natm-caption{ position:absolute; bottom:6px; left:6px; right:6px; color:#fff; font-size:0.85rem; text-shadow:0 2px 6px rgba(0,0,0,.6); background:linear-gradient(transparent, rgba(0,0,0,.25)); padding:6px; border-radius:6px;}
.lightbox{ display:none; position:fixed; inset:0; background:rgba(0,0,0,.85); align-items:center; justify-content:center; z-index:1000; padding:2vh;}
.lightbox img{ max-width:95%; max-height:92%; box-shadow:0 10px 40px rgba(0,0,0,.6); border-radius:6px;}
.lightbox:target{ display:flex;}
</style>

<div class="natm-gallery">
  {% for i in (1..5) %}
    {% if i == 1 %}
      {% assign img_name = 'n@tm.jpg' %}
    {% else %}
      {% assign img_name = 'n@tm' | append: i | append: '.jpg' %}
    {% endif %}
    <a class="natm-item" href="#lightbox-{{ i }}">
      <img src="{{ '/images/n@tm/' | append: img_name | relative_url }}" alt="{{ img_name }}">
      <div class="natm-caption">{{ img_name | split:'.' | first }}</div>
    </a>

    <div id="lightbox-{{ i }}" class="lightbox">
      <a href="#" style="position:absolute;inset:0;"></a>
      <img src="{{ '/images/n@tm/' | append: img_name | relative_url }}" alt="{{ img_name }}">
    </div>
  {% endfor %}
</div>

