---
layout: archive
permalink: /news.html
author_profile: true
---

{% include base_path %}

<!-- <h3 class="archive__subtitle">{{ site.data.ui-text[site.locale].recent_posts | default: "Recent Posts" }}</h3>
 -->

{% for post in site.posts %}
  {% capture date %}{{ post.date | date: '%Y' }}{% endcapture %}
  <h2 id="{{ date | slugify }}" class="archive__subtitle">{{ date }}</h2>
  {% include archive-single.html %}
{% endfor %}

{% include paginator.html %}
