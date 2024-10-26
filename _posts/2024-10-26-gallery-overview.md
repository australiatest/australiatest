---
layout: post
categories: info
support: [jquery, gallery]
# tags:
---

## Gallery overview

This page illustrates how to include links to multiple galleries in one row. It is the overview page to navigate to different galleries.

{% assign count = 0 %}
{% assign align = "left" %}
{% for gallery in site.data.galleries.overview %}
{% if count == 0 %}<div class="row">{% endif %}
  <div class="half-width gallery-preview {{ align }}">
    <h3>{{ gallery.title }}</h3>
    <a href="{{ site.url }}{{ site.baseurl }}/gallery/{{ gallery.pagetitle }}.html">
      <img alt="{{ gallery.title }}" src="{{ site.url }}{{ site.baseurl }}/assets/galleries/{% if gallery.picture_path %}{{ gallery.picture_path }}{% else %}{{ gallery.directory }}{% endif %}/{{ gallery.preview.thumbnail }}" />
    </a>
  </div>
{% if count == 1 %}</div>{% endif %}
{% assign count = count | plus: 1 %}
{% assign align = "right" %}
{% if count >= 2 %}
{% assign align = "left" %}
{% assign count = 0 %}
{% endif %}
{% endfor %}

{% if count != 1 %}
</div>
{% endif %}
