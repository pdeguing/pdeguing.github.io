---
layout: page
title: Photos 
permalink: /photos/
---
{% assign image_files = site.static_files | where: "image", true %}
{% for myimage in image_files %}
  {{ myimage.path }}
{% endfor %}
