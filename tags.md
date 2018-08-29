---
layout: default
permalink: /tags/
title: Tags
---
<div id="archives">
{% for tag in site.tags %}
  <div class="archive-group">
    {% capture tag_name %}{{ tag | first }}{% endcapture %}
    <h6 id="#{{ tag_name | slugize }}">{{ tag_name }}</h6>
    <a name="{{ tag_name | slugize }}"></a>
    {% for post in site.tags[tag_name] %}
    <article class="archive-item">
      <h6><a href="{{ root_url }}{{ post.url }}">{{post.title}}</a></h6>
    </article>
    {% endfor %}
  </div>
{% endfor %}
</div>
