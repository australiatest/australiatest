---
layout: post
categories: info
support: [jquery, gallery]
# tags:
---

## Two galleries post

This example shows how to include several galleries into one page. Also notice that some captions have been set.

{% include gallery-tiles.html gallery=site.data.galleries.ghent-light-festival-1 id_number=1 %}

The pictures from part two:

{% include gallery-tiles.html gallery=site.data.galleries.ghent-light-festival-2 id_number=2 %}