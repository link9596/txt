---
layout: page
title: Links
tagline: My friends.
permalink: /links.html
---


{% for f in site.data.friends %}
<div class="friends">
    <a class="a-friend" target="_blank" style="background-color:white;color:black" href="{{f.url}}">
        <img class="blog-avatar" src="{{f.image}}">
        <div class="text-container">
            <div class="name">{{f.name}}</div>
            <div class="description">{{f.describe}}</div>
        </div>
    </a>
</div>
{% endfor %}

  {% if site.data.social.valine_comment.enable  == true %}
  <script src="/comment/av-min.js"></script>
  <script src="/comment/Valine.min.js"></script>
  <div id="comments"></div>
  {% include comments.html %}
  {% endif %}
  {% include scripts.html %}