---
layout: page
permalink: /about/index.html
title: Anchal Rani
tags: [Anchal Rani]
imagefeature: fourseasons.jpg
chart: true
---
<figure>
  <img src="{{ site.url }}/images/avatar.jpg" alt="Anchal Rani">
  <figcaption>Anchal Rani</figcaption>
</figure>

{% assign total_words = 0 %}
{% assign total_readtime = 0 %}
{% assign featuredcount = 0 %}
{% assign statuscount = 0 %}

{% for post in site.posts %}
    {% assign post_words = post.content | strip_html | number_of_words %}
    {% assign readtime = post_words | append: '.0' | divided_by:200 %}
    {% assign total_words = total_words | plus: post_words %}
    {% assign total_readtime = total_readtime | plus: readtime %}
    {% if post.featured %}
    {% assign featuredcount = featuredcount | plus: 1 %}
    {% endif %}
{% endfor %}


My name is **Anchal Rani**, and this is my personal blog. It currently has {{ site.posts | size }} posts in {{ site.categories | size }} categories. In further writing I would like to enhance ur knowledge on Machine learning and speech recognition.

I am currently working as a Project Engineer at CDAC Mumbai.

