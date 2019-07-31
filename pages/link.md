---
layout: page
title: Links
tagline: My friends.
permalink: /links.html
---


{% for f in site.data.friends %}
<div class="link-col">
    <a class="k-friend" href="{{f.url}}" target="_blank">
        <div class="link-card link-hoverable">
            <div class="link-header">
                <img class="link-header-avatar" src="{{f.image}}">
                <div class="link-header-title">{{f.name}}</div>
                <div class="link-header-subtitle">{{f.describe}}</div>
            </div>
        </div>
    </a>
    <br>
</div>
{% endfor %}

  {% if site.data.social.valine_comment.enable  == true %}
  <script src="/comment/av-min.js"></script>
  <script src="/comment/Valine.min.js"></script>
  <div id="comments"></div>
  {% include comments.html %}
  {% endif %}
  {% include scripts.html %}