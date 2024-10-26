---
layout: post
title: A More Complex Example
support: [jquery, gallery]
---

This example shows how to include several galleries into one page. Also notice that some captions have been set.

{% include gallery-tiles.html gallery=site.data.galleries.ghent-light-festival-1 id_number=1 %}

The pictures from part two:

{% include gallery-tiles.html gallery=site.data.galleries.ghent-light-festival-2 id_number=2 %}

This is an example gallery. All images licensed under [CC-BY-NC-SA license][license]. Check the [Git Repo][repo] for a copy of this license.

[license]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[repo]: https://github.com/opieters/jekyll-gallery-example